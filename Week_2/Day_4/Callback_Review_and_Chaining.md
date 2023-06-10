[Table Of Contents](../../README.md)

# Callback Review and Chaining

## Callbacks

### What is a callback?

A callback is a function passed as an argument to another function. This technique allows a function to call another function. A callback function can run after another function has finished.

Why use callbacks?

For code reusability and modularity, we don't want to write the same code over and over again.

Example: 

```javascript
const forEach = (array, action) => {
  for (const element of array) {
    action(element);
  }
}

const logThatElement = (element) => console.log(element);

const logThatElementWithDescription = (element) => console.log("The number is: " + element);

const someArray = [1, 2, 3, 4, 5];

forEach(someArray, logThatElement);
forEach(someArray, logThatElementWithDescription); 
```

In the example above we dont have to rewrite forEach and can just use a different callback function to specify the display type.

## Callback Chaining

### Why chain callback together?

Sometimes you will have multiple asynchronous functions working together. By chaining them together one can give its result to the next one, and so on.

Example:

```javascript
const boilWater = (action) => {
  console.log("Starting to boil");

  setTimeout(() => {
    console.log("water is boiling");
    action();
  }, 2000);
};

const putPastaInWater = (action) => {
  console.log("Pasta in the water");

  setTimeout(() => {
    console.log("Pasta is ready!");
    action();
  }, 2000);
};

const fetchTomatoesAtGrocery = (action) => {
  console.log("Running to the grocery!");

  setTimeout(() => {
    if (Math.random > 0.5) {
      console.log("Tomatoes are here!");
      return action(false);
    }
    console.log("Oh no :/");
    return action(true);
  }, 2000);
};

//CHAINING THE FUNCTIONS TOGETHER
boilWater(() => {
  putPastaInWater(() => {
    fetchTomatoesAtGrocery((error) => {
      if (error) {
        return console.log("Seems we'll have olive oil pasta");
      }
      return console.log("Meal is ready!")
    });
  });
});
```