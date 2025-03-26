# Decision Making in Code with `if-else`

## Introduction

In programming, making decisions with code enhances interactivity and realism. This summary covers how to implement an `if-else` statement in JavaScript to determine if a person is eligible for a driver's license.

## Implementing `if-else`

1. Define a variable `age` and assign it a value (e.g., `19`).
2. Use a Boolean variable `isOldEnough` to check if `age` is at least `18`.
3. Implement an `if-else` statement:
   - If `isOldEnough` is `true`, print a message confirming eligibility.
   - If `false`, calculate and display the number of years left until eligibility.

```javascript
const age = 19;
const isOldEnough = age >= 18;

if (isOldEnough) {
  console.log("Sarah can start her driving license 🚗");
} else {
  const yearsLeft = 18 - age;
  console.log(`Sarah is too young. Wait another ${yearsLeft} years.`);
}
```

## Optimizing the Code

- Instead of using a separate Boolean variable, place the condition directly inside the `if` statement.
- Example:

```javascript
if (age >= 18) {
  console.log("Sarah can start her driving license 🚗");
} else {
  console.log(`Sarah is too young. Wait another ${18 - age} years.`);
}
```

## Understanding `if-else` Blocks

- The `else` block is optional; if omitted, no action occurs when the condition is `false`.
- JavaScript does **not** execute the entire script linearly; `if-else` allows control over execution flow.
- `if-else` is a **control structure**, giving control over which blocks execute based on conditions.

## Additional Example: Determining Century

A program to determine the century based on the birth year:

```javascript
const birthYear = 1998;
let century;

if (birthYear <= 2000) {
  century = 20;
} else {
  century = 21;
}

console.log(`Born in the ${century}th century.`);
```

### Key Takeaways

- The variable `century` is declared **outside** the `if-else` blocks to maintain accessibility.
- This structure enables controlled execution of code based on conditions.

## Recap

- Use `if-else` to control decision-making in code.
- Conditions inside `if` must return `true` or `false`.
- The `else` block runs only if the `if` condition is `false`.
- This structure is powerful and widely used in programming.

Now that you understand `if-else`, you are ready for more complex challenges!

---

**Note:** This summary is based on JavaScript but applies to other programming languages with similar `if-else` structures.
