[Table Of Contents](../../README.md)

# Mocha & Chai Initializaion

Create a new folder and cd into it. First, run npm init in your terminal. Feel free to just hit Enter for all the fields and use the default values to answer the questions that pop up.

``` javascript
npm init
```

Now that we have our package.json file, we can install mocha and chai with one handy command:

```javascript
npm install mocha@9.2.2 chai --save-dev
```
After running this command, you should see the node_modules folder and a package-lock.json file appear. Now update our package.json file to use mocha for our testing.

Open the package.json file (note: not the lock version!). Under “scripts”, there should be a “test” key. Replace the value with “mocha”, as shown in the code snippet below.

``` javascript
 "scripts": {
    "test": "./node_modules/mocha/bin/mocha"
  },
```
Save and close your package.json file. You can now run the command npm test in your terminal and npm will automatically call mocha to do its job.

To finish our setup, inside your folder, create two more folders: javascript and test. One is for our code, and the other is for our test files. This is a common pattern for repositories that use unit testing: one folder for the code, another to make sure it’s doing its job correctly.