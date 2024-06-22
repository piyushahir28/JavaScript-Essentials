## Arrow Functions

An arrow function expression has a shorter syntax compared to function expressions and does not have its own this, arguments, super, or new.target. Arrow functions are always anonymous.

```javascript
(param1, param2, ..., paramN) => {
    // function body
}
```

### Differences from Traditional Functions

- **Shorter Syntax:** Arrow functions provide a concise syntax.
- **No this Binding:** Arrow functions do not have their own this. Instead, they inherit this from the enclosing scope. This is particularly useful in scenarios like event handlers or when dealing with methods in classes.
- **Cannot be used as constructors:** Arrow functions cannot be used with the new keyword. They do not have a prototype property.
- **No arguments object:** Arrow functions do not have their own arguments object. If you need the arguments object, you should use a regular function or the rest parameters.
