# JavaScript Basics: Values and Variables

## Introduction

Welcome back! In this section, we will start learning the JavaScript language by understanding values and variables.

## Values

A **value** is a piece of data and the most fundamental unit of information in programming. Examples:

```javascript
console.log("Jonas"); // Output: Jonas
console.log(23); // Output: 23
console.log(40 + 8 + 23 + 10); // Output: 61
```

## Variables

A **variable** allows storing values for reuse. We declare a variable using `let`:

```javascript
let firstName = "Jonas";
console.log(firstName); // Output: Jonas
```

If we change the value:

```javascript
firstName = "Matilda";
console.log(firstName); // Output: Matilda
```

Using variables prevents repetitive changes and makes code more maintainable.

## Naming Conventions

### 1. camelCase (Preferred in JavaScript)

```javascript
let firstNamePerson = "Jonas";
```

### 2. Underscore notation (Popular in other languages like Ruby)

```javascript
let first_name = "Jonas";
```

### 3. Invalid Variable Names

- Cannot start with a number:
  ```javascript
  let 3years = 3; // ❌ Syntax Error
  ```
- Cannot contain symbols other than `_` or `$`:
  ```javascript
  let jonas&matilda = "JM"; // ❌ Syntax Error
  ```
- Cannot use reserved keywords:
  ```javascript
  let new = 27; // ❌ Syntax Error
  let function = "test"; // ❌ Syntax Error
  ```
- Avoid using `name` as a variable:
  ```javascript
  let name = "Jonas"; // ⚠️ Not recommended
  ```

## Best Practices

- **Use meaningful names**: `firstName` is better than `x`.
- **Start with a lowercase letter**: Avoid `Person = "Jonas";`
- **Use UPPERCASE for constants**:
  ```javascript
  const PI = 3.1415;
  ```
- **Follow JavaScript conventions**: Use `camelCase` for variables.

## Summary

- Values are the fundamental units of data.
- Variables store values for reuse.
- Use `let` for variables and follow proper naming conventions.
- Avoid reserved keywords and incorrect naming formats.
- Follow best practices for maintainable and readable code.

By following these principles, you can write clean and efficient JavaScript code!
