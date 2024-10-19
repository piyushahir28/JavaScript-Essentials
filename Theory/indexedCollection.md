## Indexed Collection:

These are collections of data which are ordered by an index value. This includes arrays and array-like constructs such as Array objects and TypedArray objects.

### Creating an array:

```javascript
const arr1 = new Array(element0, element1, /* …, */ elementN);
const arr2 = Array(element0, element1, /* …, */ elementN);
const arr3 = [element0, element1, /* …, */ elementN];
```

If you wish to initialize an array with a single element, and the element happens to be a Number, you must use the bracket syntax. When a single Number value is passed to the Array() constructor or function, it is interpreted as an arrayLength, not as a single element.

```javascript
// This...
const arr1 = new Array(arrayLength);

// ...results in the same array as this
const arr2 = Array(arrayLength);

// This has exactly the same effect
const arr3 = [];
arr3.length = arrayLength;
```

### Array Methods:

- **forEach():** The forEach() method of Array instances executes a provided function once for each array element.
  The function passed to forEach is executed once for every item in the array, with the array item passed as the argument to the function. Unassigned values are not iterated in a forEach loop.

```javascript
const colors = ["red", "green", "blue"];
colors.forEach((color) => console.log(color));
// red
// green
// blue
```

### Few things about array we generally don't even no:

- If we supply a non-integer value to the array operator in the code below, a property will be created in the object representing the array, instead of an array element.

```javascript
const arr = [];
arr[3.4] = "Oranges";
console.log(arr.length); // 0
console.log(Object.hasOwn(arr, 3.4)); // true
```

- Since JavaScript array elements are saved as standard object properties, it is not advisable to iterate through JavaScript arrays using for...in loops, because normal elements and all enumerable properties will be listed.

- The elements of an array that are omitted when the array is defined are not listed when iterating by forEach, but are listed when undefined has been manually assigned to the element:

```javascript
const sparseArray = ["first", "second", , "fourth"];

sparseArray.forEach((element) => {
  console.log(element);
});
// Logs:
// first
// second
// fourth

if (sparseArray[2] === undefined) {
  console.log("sparseArray[2] is undefined"); // true
}

const nonsparseArray = ["first", "second", undefined, "fourth"];

nonsparseArray.forEach((element) => {
  console.log(element);
});
// Logs:
// first
// second
// undefined
// fourth
```
