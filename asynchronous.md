# Asynchronous JavaScript and APIs

## Promises
```js
const myData = getData() // if this is refactored to return a Promise...

myData.then(function(data){ // .then() tells it to wait until the promise is resolved
  const pieceOfData = data['whatever'] // and THEN run the function inside
})
```
> A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.