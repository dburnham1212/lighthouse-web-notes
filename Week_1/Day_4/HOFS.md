[Table Of Contents](../../README.md)

# Higher Order Functions
Higher order functions are functions that takes in another function as a parameter

A callback function is the function that is being passed to a higher order function.

``` javascript
//Example Higher Order Function
const higherOrder = function(callback){
  callback();// call the callback function
}

//Example Callback function
const callback = function(){
  consol.log("something");
}
```

# Arrow functions

simple arrow functions can be written on one line. It will in the case below return a value multiplied by 5 and does not need curly brackets like so:

``` javascript
((number) => number * 5)();
```
If we want to write an arrow function on multiple lines it can be written like so: 

``` javascript
const weirdMultiplyAction = (number) => {
  if (number % 2 === 0){
    return number * 10;
  } else {
    return number * 100;
  }
}
```