## Various Loops in JavaScript

## for...in

The `for...in` statement iterates over all enumerable string properties of an object (ignoring properties keyed by symbols), including inherited enumerable properties.

**Syntax**

```javascript
for (variable in object) {
  statement;
}
```

Example:

```javascript
const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// Expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```
