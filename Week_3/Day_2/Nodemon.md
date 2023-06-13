[Table Of Contents](../../README.md)

# Nodemon

Nodemon is a utility that will monitor for any changes in our source code and automatically restart a server.

To install nodemon as a development dependency, use this command.

```
npm install --save-dev nodemon
```

To run an application with nodemon use the following command, But replace express_server.js with the name of your server file.

```
./node_modules/.bin/nodemon -L express_server.js
```

If dont correctly our application will be wrapped with nodemon, which will detect any changes to the server and restart it automatically.

We can also update the package.json file to run this command as a script. Edit your package.json file to include the line above as such.

```
"scripts": {
  "start": "./node_modules/.bin/nodemon -L express_server.js",
  "test": "echo \"Error: no test specified\" && exit 1"
}
```

From now on the server can be started by running npm start.