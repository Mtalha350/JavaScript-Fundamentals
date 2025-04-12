# Understanding Functions in JavaScript

## Overview

In this lesson, we explore different types of functions in JavaScript, starting with rewriting the `years until retirement` function. We discuss how to convert an arrow function to a regular function expression, export functionality to another function, and manage parameter names in separate functions.

## Key Concepts

### Converting Arrow Functions to Regular Functions

- **Arrow Function**: A concise syntax for writing functions.
- **Function Expression**: A function assigned to a variable using the `function` keyword.

### Function Expressions

- Functions in expressions are stored in variables and can be called like regular functions.
- Example:
  javascript
  const calcAge = function (birthYear) {
    return 2037 - birthYear;
  };
  


### Function Parameters

- Function parameters are local to that function, even if different functions share the same parameter name.

### Refactoring Code

- Rewriting functions for clarity or reusability, such as using `calcAge` in another function to calculate years until retirement.

### Handling Special Cases

- Using `if-else` statements to handle special cases, such as negative retirement years (for someone already retired).
  ```javascript
  if (retirement > 0) {
    return retirement;
  } else {
    return -1;
  }
  ```

### `return` Keyword

- The `return` statement immediately exits the function and returns a value.
- If there is code after the `return` in a function, it will be ignored because the function has already terminated.

### Function Syntax

- Functions have three main components: a **name**, **parameters**, and a **body**.
- Functions process data and return a value. The `return` statement outputs the result and ends the function execution.

### Calling a Function

- Functions are invoked by writing the function name followed by parentheses.
  ```javascript
  calcAge(1991);
  ```
- Parameters are passed as arguments in the parentheses.

### Console Logging vs. Return

- `console.log()` is used to display messages in the console but does not affect the function's return value.
- `return` outputs the result of a function and is crucial for processing the result elsewhere in your code.

### Recap of Types of Functions

1. **Function Declarations**: Can be used before declared.
2. **Function Expressions**: Functions stored in variables.
3. **Arrow Functions**: A shorthand for function expressions.

### Conclusion

Understanding the structure and usage of functions is fundamental in JavaScript. By mastering functions, you'll be able to write more reusable and maintainable code.
