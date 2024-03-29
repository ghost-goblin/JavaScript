# JavaScript - [OOP Principles](https://www.theodinproject.com/paths/full-stack-javascript/courses/javascript/lessons/oop-principles)

## Explain the *Single Responsibility Principle*
A class or object or module should only have _one_ responsibility. 
## Briefly explain the additional SOLID principles
**SOLID** is a _mnemonic_ acronym referring to a collection of design principles. JavaScript is a prototype-based, dynamically typed language, blending concepts from object-oriented and functional programming paradigms.
### The Single Responsibility Principle

> “Do one thing and do it well”

Every function that you write should do exactly *one* thing and have a clearly defined goal.
```js
// Set up the circle and square factory functions to create new objects

const circle = (radius) => {
  const proto = {
    type: 'Circle'
  };
  return Object.assign(Object.create(proto), {radius});
};

const square = (length) => {
  const proto = {
    type: 'Square'
  };
  return Object.assign(Object.create(proto), {length});
};

console.log(circle(13));
console.log(square(7));

const shapes = [
  circle(2),
  circle(8),
  square(5)
]


const areaCalculator = (s) => {
  const proto = {
    sum() { //logic to sum
    },
    output() {
      console.log(this.sum);

    }
  };
  return Object.assign(Object.create(proto), {shapes: s})

};

console.log(areaCalculator(shapes));
```

### The Open/Closed Principle
JavaScript modules should be open to extension but closed to modification. If you want to extend a modules behaviour, you don't need to modify the existing code.
There is one easy test to follow, if you have to open up your JS module and make a modification in order to extend it, you have failed the test.

### The Liskov Substitution Principle
Sometimes something that sounds right in natural language doesn't quite work in code. For example, in mathematics, a `square` is a `rectangle`, and makes you want to model this based on inheritance. However, in your code, if you are deriving your square from your rectangle, using the `setHeight` and `setWidth` properties, the reference point of `rectangle` doesn't make any sense.

### The Interface Segregation Principle
Do not create bloated interfaces ... meaning whenever you expose a module for outside use, make sure only the bare essentials are required and the rest are optional.

### The Dependency Inversion Principle
Your code needs to receive the relevent methods for every function. High level modules shouldn't depend on low level modules, and should depend on abstractions.

## Explain what “tightly coupled” objects are and why we want to avoid them
Tight coupling is when a group of classes are highly dependent on one another. When a class assumes too many responsibilities or gets spread out over many classes.
Loose coupling is a paradigm that promotes single responsibility and seperation of concern. A loosely couples class can be tested independently of other classes.
