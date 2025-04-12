# Expressions vs. Statements in JavaScript

## Overview

As we get more comfortable with JavaScript, it is important to understand the theoretical difference between **expressions** and **statements**. This concept is essential to understanding how JavaScript code is structured and executed.

## Expressions

An **expression** is a piece of code that **produces a value**. It can be a simple value or a combination of values and operators. Here are some examples:

- `3 + 4` (This evaluates to `7`)
- `"Hello" + " World"` (Produces the string "Hello World")
- `true && false` (Evaluates to `false`)
- `2025 - 2000` (Evaluates to `25`)
- A single number like `42` (Which is itself an expression)

### Key Points about Expressions:

- Always produce a value.
- Can be used inside template literals.
- Can be assigned to a variable: `let sum = 3 + 4;`

## Statements

A **statement** is a larger piece of code that **performs an action** but does not return a value directly. Examples of statements include:

- `if-else` statement:
  ```js
  if (10 > 5) {
    console.log("10 is greater than 5");
  }
  ```
- `switch` statement:
  ```js
  switch (fruit) {
    case "apple":
      console.log("You chose an apple");
      break;
    case "banana":
      console.log("You chose a banana");
      break;
  }
  ```
- Variable declaration:
  ```js
  let age = 30;
  ```
  (This declares a variable but does not immediately produce a value)

### Key Points about Statements:

- Perform actions but do not produce values.
- Can contain expressions.
- Usually end with a semicolon (`;`).

## Importance of Understanding the Difference

The distinction between expressions and statements is crucial because **JavaScript expects expressions and statements in different places**.

For example, in template literals:

```js
console.log(`I am ${2025 - 2000} years old.`);
```

- The placeholder inside `${}` must contain an **expression** because it needs to produce a value.
- A **statement** like an `if-else` block **cannot** be placed inside `${}` as it does not return a value.

### Example of Incorrect Usage:

```js
console.log(`I am ${if (age > 18) { "Adult" } else { "Minor" }}`);
```

- This will cause an error because `if-else` is a **statement** and cannot be evaluated as a value inside a template literal.

## Summary

- **Expressions** produce values and can be used inside template literals.
- **Statements** perform actions but do not return values.
- JavaScript expects **expressions** in certain places, such as inside template literals.
- Understanding this distinction helps in writing better JavaScript code.

By keeping these concepts in mind, you will have a clearer understanding of JavaScript execution flow and structure.
