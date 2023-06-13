[Table Of Contents](../../README.md)

# Classes

In OOP, classes are blueprints (templates) that we use to create isntances of objects. A class describes what the object is going to be and we can create new objects using a class.

Example: 

```javascript
// Example of a parent class
class ExampleParent {
  // Example of a constructor
  constructor(value) {
    // Underscores are used to represent private values in a constructor
    this._value = value;
  }

  // Example of a getter
  get value() {
    return this._value;
  }

  // Example of a setter
  set value(value) {
    this._value = value;
  }

  // Example of a simple method
  addToValue(valueToAdd){
    this._value += valueToAdd;
    return this._value;
  }
}

// Example of a child class 
class ExampleChild extends ExampleParent {
  constructor(value, value2) {
    // How to use the super keyword
    super(value);
    // Underscores are used to represent private values in a constructor
    this._value2 = value2;
  }

  // Example of a simple method
  sum() {
    return this._value + this._value2; 
  }
}

// Example of how to instantiate a class
let exampleParent = new ExampleParent(42);

// How to use getters, setters and methods
console.log(exampleParent.value); // 42
console.log(exampleParent.addToValue(5)); // 47
exampleParent.value = 69;
console.log(exampleParent.value); // 69
console.log(exampleParent.addToValue(5)); // 74


// Example of a child of example parent class
let exampleChild = new ExampleChild(12, 13);

// How to use getters, setters and methods in a child class
console.log(exampleChild.value); // 12
console.log(exampleChild.sum()); // 25
exampleChild.value = 11;
console.log(exampleChild.value); // 11
console.log(exampleChild.sum()); // 24
```