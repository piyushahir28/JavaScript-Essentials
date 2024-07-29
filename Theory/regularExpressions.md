## Regular Expressions:

Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects.

### Creating Regular Expressions:

You construct a regular expression in one of two ways:

- Using a regular expression literal, which consists of a pattern enclosed between slashes, as follows:

```javascript
const re = /ab+c/;
```

- Or calling the constructor function of the RegExp object, as follows:

```javascript
Copy to Clipboard
const re = new RegExp("ab+c");
```
