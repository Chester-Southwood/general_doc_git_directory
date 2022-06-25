# Asynchronous JavaScript

**Callbacks:** Functions that are called inside other functions at the end.

```javascript
const posts = [
	{ title: 'Post One', body: 'This is post one'},
  	{ title: 'Post Two', body: 'This is post two'}
];

function getPosts() {
	setTimeout(() => {
  	let output = '';
    posts.forEach((post, index) => {
    	output += `<li>${post.title}</li>`
    })
    
    document.body.innerHTML = output;
  }, 2000);
}

function createPost(post, callback) {
	setTimeout(() => {
  	posts.push(post);
    callback();
  }, 2000);
}

createPost({ title: 'Post Three', body: 'This is post three'}, getPosts);
```

**Promises:** Alternative way for callback functionality within a object that is either resolved or rejected based on outcome.

```javascript
const posts = [
	{ title: 'Post One', body: 'This is post one'},
  	{ title: 'Post Two', body: 'This is post two'}
];

function getPosts() {
	setTimeout(() => {
  	let output = '';
    posts.forEach((post, index) => {
    	output += `<li>${post.title}</li>`
    })
    
    document.body.innerHTML = output;
  }, 2000);
}

function createPost(post) {
	return new Promise((resolve, reject) => {
  	setTimeout(() => {
  		posts.push(post);
    	const error = false;
      
      if (!error) {
      	resolve();
      } else {
      	reject('Error, something went wrong');
      }
  	}, 2000);
  });
}

	//Example of promise chaining with then, and catching errors
/* createPost({ title: 'Post Three', body: 'This is post three'})
  .then(getPosts)
  .catch(err => console.log("The error " + err)); */
  
	//Types of "Promises"
  	const promise1 = Promise.resolve('hello world 1');
	const promise2 = 10;//Promise.resolve('hello world 1');
	const promise3 = new Promise((resolve, reject) => {
  		setTimeout(resolve, 2000, 'goodbye');
  	});
	const promise4 = new Promise((resolve, reject) => {
  		setTimeout(resolve, 4000, 'hello');
  	});
	//Case of 3rd party function that returns a promise
  	const promise5 = fetch('https://jsonplaceholder.typicode.com/users')
    	.then(res => res.json());
  
	//Example of running all promises asynchronously, the function will complete when the last promise does
  	Promise.all([promise1, promise2, promise3, promise4, promise5]).then((values) => {
  		console.log(values);
  	});
```

**Async/Await**: More elegant way of handling promises

```javascript
function createPost(post) {
	return new Promise((resolve, reject) => {
  	setTimeout(() => {
  		posts.push(post);
    	const error = false;
      
      if (!error) {
      	resolve();
      } else {
      	reject('Error, something went wrong');
      }
  	}, 2000);
  });
}

async function init() {
    //Await till this function is finished, and then run the remainder of the code
    await createPost({ title: 'Post Three', body: 'This is post three'});
    
    getPosts();
}

init();
```

Promise Practice

```javascript
async function getPokemonName(pokemonIndex) {

	return new Promise ( async (resolve, reject) => {
    	const res = await fetch('https://pokeapi.co/api/v2/pokemon/' + pokemonIndex);
    	
    	const data = await res.json(); //can't do res.json().name since function hasn't awaited when it attempts to access name property

    	resolve(data.name); //access name property after json promise is resolved
  });
} 

const p1 = getPokemonName(1);
const p2 = getPokemonName(4);
const p3 = getPokemonName(7);

Promise.all([p1, p2, p3]).then((values) => {
	console.log(values);
})

console.log("This will run first")
```

Promise Practice 2

```javascript
//Example of getting results from promise.all to outside function
async function getPokemonName(pokemonIndex) {
	return new Promise ( async (resolve, reject) => {
    const res = await fetch('https://pokeapi.co/api/v2/pokemon/' + pokemonIndex);
    const data = await res.json();
    resolve(data.name);
  });
} 

async function listPokemon() {
	return new Promise(async (resolve, reject) => {
    const p1 = getPokemonName(1);
  	const p2 = getPokemonName(4);
  	const p3 = getPokemonName(7);

  	const pokemon = await Promise.all([p1, p2, p3]);
  
  	resolve(pokemon);
  });
}

listPokemon().then((pokemonList) => {
	pokemonList.forEach(pokemon => console.log(pokemon));
  }
);
```

**Promise.Any vs Promise.Race**: 

* Promise.Any(Promise[]): Takes an array of promises, and resolves with the first unrejected promise or AggregateError if all promises are rejected.
* Promise.Race(Promise[]): Takes an array of promises, and resolves with the first unrejected promise, or first rejection. It will return the first rejection even if the other promises were to succeed after.

# Sources: 

[Async JS Crash Course - Callbacks, Promises, Async Await - Traversy Media](https://youtu.be/PoRJizFvM7s)

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/any

