# Truthy and Falsy Values in JavaScript

## Type Conversion and Coercion
- JavaScript automatically converts values to different types in various contexts.
- Type conversion to booleans involves the concepts of **truthy** and **falsy** values.

## Falsy Values
Falsy values are values that, when converted to a boolean, become `false`. JavaScript has only **five** falsy values:

1. `0`
2. `""` (empty string)
3. `undefined`
4. `null`
5. `NaN`

Note: `false` itself is already a boolean and is naturally falsy.

## Truthy Values
Any value that is **not** in the list of falsy values is considered **truthy**. 
Examples of truthy values:
- Any number **other than** `0`
- Any **non-empty** string
- Objects (including empty objects `{}`)
- Arrays (including empty arrays `[]`)

## Checking Truthy and Falsy Values
We can check the truthiness of values using the `Boolean()` function:

```javascript
console.log(Boolean(0));         // false
console.log(Boolean(undefined)); // false
console.log(Boolean("Jonas"));  // true
console.log(Boolean({}));        // true
console.log(Boolean(""));       // false
```

## Implicit Type Coercion to Boolean
In JavaScript, type coercion to boolean happens **implicitly** in two main scenarios:
1. **Using logical operators** (e.g., `&&`, `||`, `!`)
2. **In a logical context** like an `if` statement

Example:

```javascript
let money = 0;
if (money) {
    console.log("Don't spend it all");
} else {
    console.log("You should get a job");
}
```

Since `money` is `0`, which is falsy, the `else` block executes, printing **"You should get a job"**.

Now, if we change `money` to a truthy value:

```javascript
money = 100;
if (money) {
    console.log("Don't spend it all");
} else {
    console.log("You should get a job");
}
```

Since `100` is truthy, the `if` block executes, printing **"Don't spend it all"**.

## Checking If a Variable is Defined
Truthy and falsy values help in checking if a variable has been assigned a value:

```javascript
let height;
if (height) {
    console.log("YAY! Height is defined");
} else {
    console.log("Height is undefined");
}
```

Since `height` is `undefined` (a falsy value), the `else` block executes.

However, there is a **potential issue**:

```javascript
height = 0;
if (height) {
    console.log("YAY! Height is defined");
} else {
    console.log("Height is undefined");
}
```

Output:
```
Height is undefined
```

This happens because `0` is falsy, even though `height` is technically defined. This can be **problematic** in certain cases.

## Fixing the Issue
Logical operators can help address such issues, which will be discussed in the next section.

## Next Topic: Equality Operators
In the next section, we will explore **equality operators** in JavaScript.
