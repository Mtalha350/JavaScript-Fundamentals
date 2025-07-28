# JavaScript Conditional (Ternary) Operator

## Introduction

We have already seen two ways of writing conditionals in JavaScript:

1. The `if/else` statement
2. The `switch` statement

Now, we introduce another approach: the **conditional (ternary) operator**.

## What is the Conditional Operator?

The conditional operator is a concise way to write an `if/else` statement on a single line.

### Syntax:

```javascript
condition ? expressionIfTrue : expressionIfFalse;
```

### Example:

```javascript
const age = 23;
console.log(age >= 18 ? "I like to drink wine 🍷" : "I like to drink water 💧");
```

Output:

```
I like to drink wine 🍷
```

If `age` were 15, the output would be:

```
I like to drink water 💧
```

## Why is it Called the Ternary Operator?

The conditional operator is also called the **ternary operator** because it has three parts:

1. **Condition**: `age >= 18`
2. **If true**: `"I like to drink wine 🍷"`
3. **If false**: `"I like to drink water 💧"`

## Using the Conditional Operator to Assign Values

Since the conditional operator **returns a value**, we can assign it to a variable:

```javascript
const drink = age >= 18 ? "wine 🍷" : "water 💧";
console.log(drink);
```

This is more concise compared to using an `if/else` statement:

```javascript
let drink2;
if (age >= 18) {
  drink2 = "wine 🍷";
} else {
  drink2 = "water 💧";
}
console.log(drink2);
```

## Ternary Operator Inside Template Literals

Since the ternary operator is an **expression**, we can use it inside template literals:

```javascript
console.log(`I like to drink ${age >= 18 ? "wine 🍷" : "water 💧"}`);
```

Output:

```
I like to drink wine 🍷
```

## When to Use the Ternary Operator

✅ **Use it for simple conditional expressions**

- Quick decisions like assigning values or inline logging.

❌ **Do not use it as a replacement for complex `if/else` blocks**

- If you have multiple statements inside `if` or `else`, a regular `if/else` block is more readable.

## Conclusion

The ternary operator is a powerful tool that makes code more concise and readable when used appropriately. Make sure you understand it well, as it will be useful in various coding scenarios!
