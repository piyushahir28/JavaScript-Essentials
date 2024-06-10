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
