# JavaScript Data Types

## Values and Variables

In JavaScript, values can have different types depending on the type of data they hold. Every value is either an **object** or a **primitive value**. Primitive values are not objects, and we will focus on them for now.

## Primitive Data Types

JavaScript has **seven primitive data types**:

1. **Number**: Always stored as floating point numbers (e.g., `23` is the same as `23.0`). Unlike some other languages, JavaScript does not distinguish between integers and decimals.
2. **String**: A sequence of characters used for text. Strings must be enclosed in quotes (single or double).
3. **Boolean**: A logical type that can have values `true` or `false`. These are commonly used for decision-making in code.
4. **Undefined**: A value assigned to a variable that has been declared but not initialized.
5. **Null**: Similar to `undefined`, but used in different circumstances to explicitly indicate an empty value.
6. **Symbol**: Introduced in ES2015, it defines a unique and immutable value.
7. **BigInt**: Introduced in ES2020, used for integers that are too large to be represented by the `Number` type.

## Dynamic Typing in JavaScript

JavaScript has **dynamic typing**, meaning:

- You do not need to specify the type of a variable when declaring it.
- The type of a variable is determined automatically by JavaScript.
- A variable can hold values of different types at different times.
- This is different from statically typed languages, where variables have fixed types.

### Example of Dynamic Typing:

```javascript
let x = 23; // x is a number
x = "Hello"; // x is now a string
```

This flexibility can be useful but can also lead to hard-to-find bugs.

## The `typeof` Operator

The `typeof` operator is used to determine the type of a value.

### Example:

```javascript
console.log(typeof 23); // "number"
console.log(typeof "Hello"); // "string"
console.log(typeof true); // "boolean"
console.log(typeof undefined); // "undefined"
console.log(typeof null); // "object" (a known JavaScript quirk)
console.log(typeof Symbol("id")); // "symbol"
console.log(typeof 9007199254740991n); // "bigint"
```

## Code Commenting in JavaScript

### Single-line Comments

Use `//` to write a single-line comment.

```javascript
// This is a single-line comment
let name = "JavaScript"; // Variable declaration
```

### Multi-line Comments

Use `/* ... */` to write a multi-line comment.

```javascript
/*
 This is a multi-line comment.
 It spans multiple lines.
*/
```

Comments help document code and can be used to temporarily disable code execution.

---

This summary covers the key concepts of JavaScript data types, dynamic typing, and commenting. Understanding these fundamentals will help you write efficient and error-free JavaScript code.
