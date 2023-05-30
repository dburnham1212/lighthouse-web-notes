### Truthy and Falsey Values

Comparing two values in JavaScript will return either true or false. But there are some situations in JavaScript, especially when using ==, that the correct response will be the opposite of what you might expect.

Consider the following example:

``` javascript
0 == false
```

We know that a double equal == will try to force a type coercion, and therefore will... what? Try to convert a Boolean into a Number? But they're still not the same values, right? It may seem counter-intuitive, but in JavaScript, everything has an inherent Boolean value, which is commonly referred to as a Truthy or Falsey value. In this case, even though 0 is a Number, it also holds a Falsey value.

In the future, we're going to encounter several weird cases of truthy and falsey values, but for now we just have to remember that most things in JavaScript are considered Truthy, except for the following:

``` javascript
// All of the following are inherently falsey:

False
// False is False. Makes sense, right?

0
// 0 is the only falsey Number

""
// an empty string is falsey

null
// a null, or empty value, is falsey.

undefined
// an object that has not been defined is considered falsey.

NaN
// Not a Number. You'll learn more about NaN as we go on.
```

#### Truthy and Falsey Values

Truthy values are a fast and easy way to check conditions in our code. For example, maybe we want to save the users name to a String, but only if we don't already have something saved to username.

``` javascript
username = '';

if (!username) {
  username = 'Siobhan';
}
```

Since we haven't yet saved anything to username, it's an empty String, and therefore returns falsey, which we account for with the bang !username, allowing the rest of our code to run.

The same concept can be applied to Arrays. Invoking the Array.length property will return 0 for an empty Array, which is also a falsey value.

``` javascript
shoppingList = [];

if (!shoppingList.length) {
  shoppingList.push('coconut milk');
}
```

This is a simple way to check if our Shopping List is empty, and if it is we can add some delicious coconut milk to it!