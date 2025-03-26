# Type Conversion and Type Coercion in JavaScript

## Introduction

In this video, we revisit value types in JavaScript, focusing on type conversion and type coercion. Understanding these concepts is essential for handling data in JavaScript, which often behaves unpredictably when dealing with types.

## Type Conversion

Type conversion refers to manually changing a value from one type to another. This is done explicitly using JavaScript functions.

### Example: String to Number Conversion

```javascript
const inputYear = "1991";
console.log(Number(inputYear) + 18); // Output: 2009
```

Here, the `Number()` function converts a string to a number before performing arithmetic.

### Example: Number to String Conversion

```javascript
const age = 23;
console.log(String(age)); // Output: "23"
```

The `String()` function explicitly converts a number into a string.

### NaN (Not a Number)

If a non-numeric string is converted to a number, JavaScript returns `NaN` (Not a Number), which means an invalid number.

```javascript
console.log(Number("Jonas")); // Output: NaN
console.log(typeof NaN); // Output: "number"
```

## Type Coercion

Type coercion happens when JavaScript automatically converts one type to another during an operation.

### Example: String Concatenation with Numbers

```javascript
console.log("I am " + 23 + " years old"); // Output: "I am 23 years old"
```

The `+` operator triggers type coercion, converting numbers into strings when concatenated with a string.

### Example: Arithmetic Operations Triggering Coercion to Numbers

```javascript
console.log("23" - "10" - 3); // Output: 10
console.log("23" * "2"); // Output: 46
console.log("23" / "2"); // Output: 11.5
```

Here, the `-`, `*`, and `/` operators convert strings into numbers to perform arithmetic.

### Guess the Output Game

```javascript
let n = "1" + 1; // "11" (string concatenation)
n = n - 1; // "11" (string) - 1 = 10 (number subtraction)
console.log(n); // Output: 10
```

This example demonstrates how JavaScript first performs string concatenation and then arithmetic subtraction due to type coercion.

## Conclusion

Understanding type conversion and type coercion helps avoid unexpected JavaScript behaviors and improves debugging efficiency. JavaScript can only convert values to **numbers, strings, and Booleans**, but not to `null` or `undefined`. Mastering these concepts is crucial for effective programming in JavaScript.
