## Data Types Conversion

JavaScript is a dynamically typed language. This means you don't have to specify the data type of a variable when you declare it. It also means that data types are automatically converted as-needed during script execution.

### Numbers and the '+' operator

In expressions involving numeric and string values with the + operator, JavaScript converts numeric values to strings. For example, consider the following statements:

```javascript
x = "The answer is " + 42; // "The answer is 42"
```

With all other operators, JavaScript does not convert numeric values to strings. For example:

```javascript
"37" - 7; // 30
"37" * 7; // 259
```

### Converting strings to numbers

In the case that a value representing a number is in memory as a string, there are methods for conversion.

- parseInt()
- parseFloat()
