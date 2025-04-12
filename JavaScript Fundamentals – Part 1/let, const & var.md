# Variable Declarations in JavaScript

JavaScript provides three ways to declare variables: `let`, `const`, and `var`. Each has distinct behaviors and use cases.

## 1. `let` Keyword

- Introduced in ES6 (modern JavaScript).
- Used for variables that can change during program execution.
- Allows reassignment (mutation) of values.
- Suitable for cases where variable values need to be updated.
- Example:
  ```js
  let age = 30;
  age = 31; // Allowed
  ```

## 2. `const` Keyword

- Introduced in ES6.
- Used for variables that should not change after initialization.
- Immutable: values cannot be reassigned after declaration.
- Cannot be declared without an initial value.
- Example:
  ```js
  const birthYear = 1991;
  birthYear = 1990; // Error: Assignment to constant variable
  ```
- Best practice: Use `const` by default unless reassignment is necessary.

## 3. `var` Keyword (Legacy)

- Used in older JavaScript (before ES6).
- Allows reassignment similar to `let`.
- Should be avoided due to issues with scoping and hoisting.
- Example:
  ```js
  var job = "programmer";
  job = "developer"; // Allowed
  ```

## Avoiding Undeclared Variables

- Declaring variables without `let`, `const`, or `var` creates a property on the global object, which is a bad practice.
- Example:
  ```js
  lastName = "Smith"; // Avoid this
  console.log(lastName);
  ```

## Best Practices

- Use `const` by default.
- Use `let` only when a variable needs to be reassigned.
- Avoid `var` due to scoping issues.
- Always declare variables properly.

In the next section, we will explore operators in JavaScript.
