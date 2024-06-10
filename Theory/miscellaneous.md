### This file contains miscellaneous things, which I encounter while learning JavaScript.

- **First-Class Function:** A programming language is said to have First-class functions when functions in that language are treated like any other variable. For example, in such a language, a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable.
- **Prototype-based Programming:** Prototype-based programming is a style of object-oriented programming in which classes are not explicitly defined, but rather derived by adding properties and methods to an instance of another class or, less frequently, adding them to an empty object. In simple words: this type of style allows the creation of an object without first defining its class.
- **Lexical Scope:** Lexical scope in JavaScript refers to the scope resolution of variables based on the physical structure of the code. In simpler terms, lexical scope is determined by where variables and blocks of scope are authored in the code.
  When you define a variable or a function inside another function or block of code, the inner function/block has access to the variables declared in its outer function/block. This access is possible because of lexical scoping.
- **Arrow functions in JavaScript do not have their own `this`** - Arrow functions, unlike regular functions, do not have their own `this`, `arguments`, `super`, or `new`.target bindings. Instead, they inherit these bindings from the enclosing lexical scope.
- **Iterator in JavaScript** - An iterator is an object that defines a sequence and potentially a return value upon its termination. It is a protocol that allows objects to define their iteration behavior, such as what values are looped over in a `for...of` loop.

Below is how we can create an Iterator:

```javascript
let iterableObj = {
  data: [1, 2, 3],
  [Symbol.iterator]: function () {
    let index = 0;
    return {
      next: () => {
        if (index < this.data.length) {
          return { value: this.data[index++], done: false };
        } else {
          return { value: undefined, done: true };
        }
      },
    };
  },
};

let iterator = iterableObj[Symbol.iterator]();

console.log(iterator.next()); // Logs: { value: 1, done: false }
console.log(iterator.next()); // Logs: { value: 2, done: false }
console.log(iterator.next()); // Logs: { value: 3, done: false }
console.log(iterator.next()); // Logs: { value: undefined, done: true }
```
