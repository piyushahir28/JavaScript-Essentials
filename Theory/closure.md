## Closure

A closure in JavaScript is a function that retains access to its outer lexical environment, even after the outer function has finished executing. This concept allows inner functions to access variables and parameters of outer functions even after those functions have returned.

- Lexical Scoping: JavaScript uses lexical scoping, meaning that the accessibility of variables is determined by their physical location in the code
- Inner Function: A function defined inside another function.
- Outer Function: The function within which the inner function is defined.

```javascript
function outerFunction(outerVariable) {
  return function innerFunction(innerVariable) {
    console.log("Outer Variable:", outerVariable);
    console.log("Inner Variable:", innerVariable);
  };
}

const newFunction = outerFunction("outside");
newFunction("inside");
```

### How Closures Work:

- Persistence of Variables: The innerFunction retains access to outerVariable even after outerFunction has finished executing. This is because innerFunction forms a closure around outerVariable.
- Encapsulation: Closures allow for data encapsulation. The outerVariable is private to outerFunction but is accessible within innerFunction.

### Practical Uses of Closures:

**Data Privacy:** Creating private variables.

```javascript
function createCounter() {
  let count = 0;
  return function () {
    count += 1;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
console.log(counter()); // 3
```

**Function Factories:** Generating functions with preset configurations.

```javascript
function greetingGenerator(greeting) {
  return function (name) {
    console.log(greeting + ", " + name);
  };
}

const sayHello = greetingGenerator("Hello");
sayHello("Alice"); // Hello, Alice
sayHello("Bob"); // Hello, Bob

const sayHi = greetingGenerator("Hi");
sayHi("Charlie"); // Hi, Charlie
```

### In Simpler Terms:

A closure in JavaScript is when a function can remember and use variables from outside its own scope, even after the outer function has finished running.
