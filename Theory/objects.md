### JavaScript Objects

An object is a collection of related data and/or functionality. These usually consist of several variables and functions (which are called properties and methods when they are inside objects).

```javascript
const person = {
  name: ["Bob", "Smith"],
  age: 32,
  bio() {
    console.log(`${this.name[0]} ${this.name[1]} is ${this.age} years old.`);
  },
  introduceSelf() {
    console.log(`Hi! I'm ${this.name[0]}.`);
  },
};
```

Object can be accessed in two ways:

- Dot Notation `(person.age)`
- Bracket Notation `(person["age"])`

#### Object Prototypes:

Every object in JavaScript has a built-in property, which is called its prototype. The prototype is itself an object, so the prototype will have its own prototype, making what's called a prototype chain. The chain ends when we reach a prototype that has null for its own prototype.

- Shadowing Properties

#### Constructor Function

Constructor functions are special functions used for creating objects and initializing their properties. They serve as blueprints for creating multiple instances of similar objects.
