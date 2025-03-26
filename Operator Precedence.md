# JavaScript Operator Precedence

## What is Operator Precedence?

Operator precedence determines the order in which different operators are executed in JavaScript.

### Example:

```javascript
const ageJonas = 2025 - 1991;
const ageSarah = 2025 - 2018;
console.log(ageJonas > ageSarah); // true
```

**Why?**

- The subtraction (`-`) happens before the comparison (`>`).
- This follows JavaScript's predefined precedence rules.

## Operator Precedence Table (MDN Reference)

JavaScript follows a well-defined precedence order, as documented in MDN's [Operator Precedence Table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence).

### Key Precedence Levels:

1. **Parentheses `()`** – Highest precedence (21).
2. **Arithmetic Operators** – `* / % + -` (14-15).
3. **Comparison Operators** – `> < >= <=` (12).
4. **Equality Operators** – `== === != !==` (10).
5. **Logical Operators** – `&&` (6) and `||` (5).
6. **Assignment `=`** – Lowest precedence (3).

### Execution Order Example:

```javascript
console.log(25 - 10 - 5); // 10
```

- `25 - 10 - 5` executes **left to right**, following precedence.

## Left-to-Right vs Right-to-Left Execution

Most operators execute **left-to-right**, except for **assignment (`=`) and exponentiation (`**`)**, which execute **right-to-left\*\*.

### Example:

```javascript
let x, y;
x = y = 25 - 10 - 5;
console.log(x, y); // 10, 10
```

- `25 - 10 - 5` evaluates to `10`.
- `y = 10` executes first.
- `x = 10` executes next.
- Since assignment works **right to left**, both `x` and `y` hold `10`.

## Using Parentheses for Clarity

Parentheses `()` help control precedence, just like in mathematics.

### Incorrect Calculation:

```javascript
const averageAge = ageJonas + ageSarah / 2;
console.log(averageAge); // Incorrect result
```

- The division happens **before** addition due to higher precedence.

### Correct Calculation:

```javascript
const averageAge = (ageJonas + ageSarah) / 2;
console.log(averageAge); // Correct result
```

- Parentheses force addition **before** division.

## Summary

- JavaScript follows a **precedence table** for execution order.
- **Parentheses** have the highest precedence.
- **Math operators** execute before **comparison** and **logical** operators.
- **Assignment (`=`) executes right-to-left**, unlike most operators.
- **Use parentheses** to clarify complex expressions and avoid unexpected results.

For a complete reference, check out MDN’s [Operator Precedence Table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence).
