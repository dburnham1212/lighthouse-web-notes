### Template Literals

Consider the following example which uses string concatenation to greet Alice.

``` javascript
const name = 'Alice';
console.log('Hello, ' + name + '!'); // logs: Hello, Alice!
```

This works – it concatenates (adds) the strings 'Hello, ', 'Alice' and '!' together. However, this can become cumbersome, especially when working with more and/or longer strings.

Template literals (aka template strings) allow us to simplify this process while simultaneously being faster and using up less computer memory!

The next example greets Alice using the template literals syntax.

``` javascript
const name = 'Alice';
console.log(`Hello, ${name}!`); // logs: Hello, Alice!
```

The main difference here are that the string assigned to the variable name (that is, 'Alice') is interpolated (injected) directly into the final string.

Since template strings are a special type of string, instead of using single or double quotes to declare them, we need to use back-ticks (`).