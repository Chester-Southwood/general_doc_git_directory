# Node Package Manager: NPM

npm is the standard package manager for Node.js.

| Command     | Action |
| ----------- | ----------- |
| npm init    | Creates a package.json file |
| npm ls      | Lists installed packages |
| npm install | Installs packages listed in package.json file |
| npm install packageName | Installs package passed in to install command and adds to package.json file. |
| npm install -g packageName| Installing a package globally allows you to use the code in the package as a set of tools on your local computer. |
| npm uninstall | Uninstalls packages listed in package.json file |
| npm update | Updates specified package if passed in, if not it updates all packages listed in package.json file |
| npm start | Runs command specified in start property of package.json file, if none exists it will run "node server.js" |
| process.env.NODE_ENV | Environment variable populaized by NodeJS, used when set to run code as production or development logic. |

# Package.json

The package.json file is a key element in lots of app codebases based on the Node.js ecosystem. Enables npm to start your project, run scripts, install dependencies, publish to the NPM registry, and many other useful tasks.

| Property     | Purpose |
| -----------  | ----------- |
| Main         | An indicator of the entry point for your project that is used to load you module when you're building a module/library to be used in other projects. `NOT NEEDED IF BUILDING LIBRARY`            |
| Script       | A command used to run script. `npm start dev1` |
| Dependencies | List of Dependency Modules needed for project that are downloaded via npm |
| DevDependencies | List of Dependency Modules needed for project that are downloaded via npm FOR DEV only if Prod flag is not passed in or set |
| private | If set to true, prevents app/package to be published to npm |

`Example package.json`
```json
{
  "name": "project",
  "version": "1.0.0",
  "description": "project descripton",
  "private": true,
  "scripts": {
    "start": "npm run dev",
    "dev": "nodemon site_ts/app.ts",
    "build": "tsc -p ."
  },
  "author": "Bob the Tomato",
  "license": "ISC",
  "dependencies": {
    "express": "^4.16.2",
    "jsonwebtoken": "^8.5.1"
  },
  "devDependencies": {
    "@types/express": "^4.17.13",
    "@types/jsonwebtoken": "^8.5.8",
    "@types/node": "^18.0.0",
    "nodemon": "^2.0.18",
    "ts-node": "^10.8.1",
    "typescript": "^4.7.4"
  }
}
```