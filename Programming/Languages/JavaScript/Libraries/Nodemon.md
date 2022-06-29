# Nodemon

* [Nodemon](https://www.npmjs.com/package/nodemon): JS Package used as a [Supervisor Program](https://en.wikipedia.org/wiki/Supervisory_program#:~:text=A%20supervisory%20program%20or%20supervisor,in%20a%20data%20processing%20system.) to make development easier by restarting program each time it crashes or a file is modified.

| Command     | Action |
| ----------- | ----------- |
| npm install -g nodemon      | Install package globally (Recommended so all applications can use)       |
| npm install --save-dev nodemon   | Instal package for development only, can be ran only through calling npm script (npm start) instead of being able to use it from command line.        |
| nodemon [appname].js        | Starts app using nodemon              |