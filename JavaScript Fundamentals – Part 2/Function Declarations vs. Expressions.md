# 📘 JavaScript Functions Summary

## 🔹 Function Declarations

- Defined using the `function` keyword.
- Can be **called before they are defined** (due to hoisting).
- Syntax:

```js
function calcAge1(birthYear) {
  return 2037 - birthYear;
}

const age1 = calcAge1(1991); // 46
console.log(age1);
```

## 🔹 Function Expressions

- An **anonymous function** assigned to a variable.
- **Cannot** be called before it's defined.
- Syntax:

```js
const calcAge2 = function (birthYear) {
  return 2037 - birthYear;
};

const age2 = calcAge2(1991); // 46
console.log(age2);
```

## 🔹 Key Differences

| Feature                      | Function Declaration | Function Expression |
| ---------------------------- | -------------------- | ------------------- |
| Can be called before defined | ✅ Yes (hoisted)     | ❌ No (not hoisted) |
| Has a name                   | ✅ Yes               | ❌ No (anonymous)   |
| Stored in variable           | ❌ Optional          | ✅ Required         |

## 🧠 Notes

- **Parameter**: Placeholder used in function definition.
- **Argument**: Actual value passed when calling the function.
- In JavaScript, **functions are values** — just like strings or numbers — and can be stored in variables.

## 🔸 Which Should You Use?

- Depends on your **coding style or team conventions**.
- Many developers prefer **function expressions** for more structured code.
- Still, you must know **both types**, as both are widely used in JavaScript development.

---

> “Understand both function declarations and expressions — use what fits best, but never forget their differences.”
