# Equality Operators in JavaScript

## Introduction

In JavaScript, we often use comparison operators to make decisions with `if-else` statements. However, when checking if two values are exactly equal, we use equality operators.

## Equality Operators

There are two main types of equality operators in JavaScript:

1. **Strict Equality (`===`)**

   - Compares both value and type.
   - Does **not** perform type coercion.
   - Example:
     ```js
     console.log(18 === 18); // true
     console.log(18 === "18"); // false
     ```

2. **Loose Equality (`==`)**
   - Compares values but allows type coercion.
   - Example:
     ```js
     console.log(18 == "18"); // true (string "18" is converted to number 18)
     ```

## Best Practice: Use Strict Equality (`===`)

- Loose equality (`==`) can introduce unexpected bugs due to type coercion.
- JavaScript developers recommend using strict equality (`===`) for predictable behavior.
- If type conversion is needed, explicitly convert values before comparison:
  ```js
  let userInput = prompt("Enter a number:");
  let favoriteNumber = Number(userInput);
  if (favoriteNumber === 23) {
    console.log("Cool! 23 is an amazing number.");
  }
  ```

## Using `if-else` Statements with Equality Operators

Example of using `if-else` with equality operators:

```js
let favoriteNumber = Number(prompt("What's your favorite number?"));

if (favoriteNumber === 23) {
  console.log("Cool! 23 is an amazing number.");
} else if (favoriteNumber === 7) {
  console.log("7 is also a cool number.");
} else if (favoriteNumber === 9) {
  console.log("9 is also a cool number.");
} else {
  console.log("Number is not 23, 7, or 9.");
}
```

## The Inequality Operators

Besides equality, JavaScript also provides inequality operators:

1. **Strict Inequality (`!==`)**

   - Checks if values are not equal and of different types.
   - Example:
     ```js
     console.log(18 !== "18"); // true
     console.log(18 !== 18); // false
     ```

2. **Loose Inequality (`!=`)**
   - Checks if values are not equal but allows type coercion.
   - Example:
     ```js
     console.log(18 != "18"); // false (because "18" is converted to 18)
     ```

## Conclusion

- Use **strict equality (`===`)** and **strict inequality (`!==`)** instead of loose comparisons.
- Convert user input explicitly before comparison.
- Use `if-else` statements to handle multiple conditions effectively.

By following these best practices, you can write cleaner and more reliable JavaScript code!
