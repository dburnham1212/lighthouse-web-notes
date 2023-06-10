[Table Of Contents](../../README.md)

# Promises

A promise in Javascript works like a promise in real life, somebody will promise you something and eventually you will know if they kept their promise or not.

For example if you want a bag of chips from a vending machine. While the bag of chips is coming out of its spot the promise is pending. if the bag of chips gets stuck then the promise is rejected. If the bag of chips falls down then the promise of having chips is fulfilled.

When dealing with asynchronous functions promises are a better way to work than callbacks.

A promise has 3 potential states: Pending, Rejected, or Fulfilled

Example in code:

```javascript
const boilWater = () =>{
  return new Promise((resolve, reject) => {
    if(Math.random() > 0.5){
      return resolve();
    }
    return reject("Oven Broke");
  })
};

const putPastaInWater = () => {
  return new Promies(resolve, reject) => {
    if(Math.random() > 0.5){
      return resolve();
    }
    return reject("Pasta fell on the floor");
  }
}

boilWater()
  .then(() => putThePastaInTheWater())
  .then(() => console.log("Pasta boiling was a success"))
  .catch((error) => console.log(error));
```