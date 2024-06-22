## Hoisting

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their containing scope during the compilation phase. This means that regardless of where variables are declared in your code, they are moved to the top of their scope, making them accessible before they are actually declared.

However, it's important to understand that hoisting behaves differently for var, let, and const:

### var:

Variables declared with var are hoisted to the top of their function scope or global scope, but their assignments are not hoisted.

```javascript
console.log(x); // Outputs: undefined
var x = 10;
console.log(x); // Outputs: 10
```

### let and const:

Variables declared with let and const are also hoisted to the top of their block scope, but unlike var, they are not initialized. This means accessing them before the actual declaration will result in a ReferenceError.

```javascript
console.log(x); // ReferenceError: Cannot access 'x' before initialization
let x = 10;
console.log(x); // Outputs: 10
```

Similarly, with const:

```javascript
console.log(x); // ReferenceError: Cannot access 'x' before initialization
const x = 10;
console.log(x); // Outputs: 10
```

---

### In Simpler Terms:

Hoisting is like a magic trick JavaScript does when it reads your code. Imagine it's moving all variable declarations and function declarations to the top of their respective scope, like they're lifted up. But, there's a twist depending on the type of variable.

Function hoisting only works with function declarations — not with function expressions. The following code will not work:

```javascript
console.log(square(5)); // ReferenceError: Cannot access 'square' before initialization
const square = function (n) {
  return n * n;
};
```
