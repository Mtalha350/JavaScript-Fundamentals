# Equality Operators and Boolean Logic in JavaScript

## Equality Operators

### Introduction

In JavaScript, we often use comparison operators to make decisions with `if-else` statements. However, when checking if two values are exactly equal, we use equality operators.

### Types of Equality Operators

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

### Best Practice: Use Strict Equality (`===`)

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

### Using `if-else` Statements with Equality Operators

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

### The Inequality Operators

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

### Conclusion

- Use **strict equality (`===`)** and **strict inequality (`!==`)** instead of loose comparisons.
- Convert user input explicitly before comparison.
- Use `if-else` statements to handle multiple conditions effectively.

## Boolean Logic and Logical Operators

### Introduction to Boolean Logic

Boolean logic is a fundamental concept in computer science that uses `true` and `false` values to solve logical problems. It relies on logical operators to combine and manipulate Boolean values.

### Logical Operators

JavaScript provides three main logical operators:

1. **AND (`&&`) Operator**

   - Returns `true` if **both** operands are `true`.
   - Example:
     ```js
     let hasLicense = true;
     let hasGoodVision = false;
     console.log(hasLicense && hasGoodVision); // false
     ```

2. **OR (`||`) Operator**

   - Returns `true` if **at least one** operand is `true`.
   - Example:
     ```js
     let isTired = false;
     console.log(hasLicense || isTired); // true
     ```

3. **NOT (`!`) Operator**
   - Inverts the Boolean value.
   - Example:
     ```js
     console.log(!hasGoodVision); // true
     ```

### Truth Table for AND and OR Operators

| A     | B     | A && B | A     |     | B   |
| ----- | ----- | ------ | ----- | --- | --- |
| true  | true  | true   | true  |
| true  | false | false  | true  |
| false | true  | false  | true  |
| false | false | false  | false |

### Example Usage in `if-else` Statements

```js
let age = 16;
let isAdult = age >= 18;
let hasParentalConsent = true;

if (isAdult || hasParentalConsent) {
  console.log("Allowed to enter.");
} else {
  console.log("Not allowed to enter.");
}
```

### Conclusion

- **AND (`&&`)** requires all conditions to be `true`.
- **OR (`||`)** requires at least one condition to be `true`.
- **NOT (`!`)** inverts a Boolean value.
- Boolean logic is essential in decision-making structures like `if-else` statements.
