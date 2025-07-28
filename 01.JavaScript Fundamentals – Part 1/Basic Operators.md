# JavaScript Fundamentals: Operators

## Introduction to Operators

Operators allow us to transform values, combine multiple values, and perform various operations in JavaScript. They are categorized into different types:

- **Mathematical (Arithmetic) Operators**
- **Comparison Operators**
- **Logical Operators**
- **Assignment Operators**

---

## 1. Mathematical (Arithmetic) Operators

Mathematical operators are used to perform calculations.

### Common Arithmetic Operators:

- `+` (Addition)
- `-` (Subtraction)
- `*` (Multiplication)
- `/` (Division)
- `%` (Modulus - remainder after division)
- `**` (Exponentiation)

Example:

```js
const now = 2037;
const ageJonas = now - 1991; // 46
const ageSarah = now - 2018; // 19
console.log(ageJonas, ageSarah);
```

### Using Variables for Efficiency:

Instead of repeating values, use variables to store reusable values.

```js
const now = 2037;
const birthYearJonas = 1991;
const birthYearSarah = 2018;
const ageJonas = now - birthYearJonas;
const ageSarah = now - birthYearSarah;
console.log(ageJonas, ageSarah);
```

### Additional Arithmetic Operations:

```js
console.log(ageJonas * 2, ageJonas / 10, 2 ** 3);
// 92, 4.6, 8 (2 to the power of 3)
```

---

## 2. String Concatenation

The `+` operator can also be used to join (concatenate) strings.

```js
const firstName = "Jonas";
const lastName = "Schmedtmann";
console.log(firstName + " " + lastName);
// Output: Jonas Schmedtmann
```

---

## 3. Assignment Operators

Assignment operators store values in variables.

- `=` (Assign value)
- `+=` (Addition assignment)
- `-=` (Subtraction assignment)
- `*=` (Multiplication assignment)
- `/=` (Division assignment)
- `++` (Increment by 1)
- `--` (Decrement by 1)

Example:

```js
let x = 10 + 5; // 15
x += 10; // x = x + 10 (25)
x *= 4; // x = x * 4 (100)
x++; // x = x + 1 (101)
x--; // x = x - 1 (100)
console.log(x);
```

---

## 4. Comparison Operators

Comparison operators return Boolean values (`true` or `false`).

- `>` (Greater than)
- `<` (Less than)
- `>=` (Greater than or equal to)
- `<=` (Less than or equal to)

Example:

```js
console.log(ageJonas > ageSarah); // true
console.log(ageJonas >= 18); // true
console.log(ageSarah <= 18); // true
```

Checking if a person is of full age:

```js
const isFullAge = ageSarah >= 18;
console.log(isFullAge); // true
```

---

## Conclusion

Operators are fundamental in JavaScript for performing calculations, assigning values, and making comparisons. Using them effectively allows for more efficient and readable code.
