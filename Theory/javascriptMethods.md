## Javascript Useful Methods:

### Object.keys()

The Object.keys() static method returns an array of a given object's own enumerable string-keyed property names.

```javascript
const object1 = {
  a: "somestring",
  b: 42,
  c: false,
};

console.log(Object.keys(object1));
// Expected output: Array ["a", "b", "c"]
```

### Object.getOwnPropertyNames()

The Object.getOwnPropertyNames() static method returns an array of all properties (including non-enumerable properties except for those which use Symbol) found directly in a given object.

```javascript
const object1 = {
  a: 1,
  b: 2,
  c: 3,
};

console.log(Object.getOwnPropertyNames(object1));
// Expected output: Array ["a", "b", "c"]
```

### toPrecision()

The toPrecision() method of Number values returns a string representing this number to the specified number of significant digits.

```javascript
let num = 5.123456;

console.log(num.toPrecision()); // '5.123456'
console.log(num.toPrecision(5)); // '5.1235'
console.log(num.toPrecision(2)); // '5.1'
console.log(num.toPrecision(1)); // '5'
```
