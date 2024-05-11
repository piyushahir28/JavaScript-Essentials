## `new` Keyword

`new` keyword is used primarily for creating instances of objects that are defined using constructor functions or class declarations.

### When you create an object using new, it does several things:

- Creates a new object: It creates a new empty object.

- Sets the prototype: It sets the prototype of the newly created object to the prototype property of the constructor function.

- Calls the constructor function: It calls the constructor function, passing any arguments provided to the new keyword. Inside the constructor function, this refers to the newly created object.

- Returns the newly created object: If the constructor function doesn't explicitly return anything, new will return the newly created object. However, if the constructor function returns an object explicitly, the newly created object will be replaced by the returned object.
