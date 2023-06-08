[Table Of Contents](../../README.md)

# Exporting Functions

To export a singular function you would export the function itself using module.export.

``` javascript
const exampleFunction = () => {
  debug.log("This is an example)
}

module.exports = exampleFunction;
```

You can then include the function in the file using the file name. Assuming the filename is example.js.

``` javascript
const exampleFunction = require('./example.js');
```

To use multiple functions from one file in another firle you can store the functions in an object

``` javascript
const exampleFunction = () => {
  debug.log("This is an example)
}

const secondExampleFunction = () => {
  debug.log("T
  his is an example)
}

module.exports = { exampleFunction, secondExampleFunction };
```

We can then access them in the same sort of way using the require keyword. The only difference is the variable that we reference will contain an object referencing both of the functions instead of a single function. Assuming again that the filename is example.js.

``` javascript
const helper = require('./example.js');

// to call the function
helper.exampleFunction();
helper.secondExampleFunction();
```