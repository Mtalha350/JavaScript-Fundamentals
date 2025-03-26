# Logical Operators in JavaScript

## Introduction

This summary covers the usage of logical operators in JavaScript. We will use Boolean variables from the previous lecture, including `hasDriversLicense` and `hasGoodVision`, to demonstrate how logical operators work.

## Boolean Variables

We define two Boolean variables:

```javascript
let hasDriversLicense = true; // Variable A
let hasGoodVision = true; // Variable B
```

These variables will be used in logical operations.

## Logical Operators

### AND (`&&`) Operator

The `&&` operator returns `true` only if both operands are `true`:

```javascript
console.log(hasDriversLicense && hasGoodVision); // true
```

If one operand is `false`, the result is `false`:

```javascript
hasGoodVision = false;
console.log(hasDriversLicense && hasGoodVision); // false
```

### OR (`||`) Operator

The `||` operator returns `true` if at least one operand is `true`:

```javascript
console.log(hasDriversLicense || hasGoodVision); // true
```

### NOT (`!`) Operator

The `!` operator inverts the Boolean value:

```javascript
console.log(!hasDriversLicense); // false
```

## Decision Making Using Logical Operators

Using the logical operators, we can determine whether Sarah should drive:

```javascript
let shouldDrive = hasDriversLicense && hasGoodVision;
if (shouldDrive) {
  console.log("Sarah is able to drive");
} else {
  console.log("Someone else should drive");
}
```

Since `hasGoodVision` is `false`, the output will be:

```
Someone else should drive
```

## Adding Another Boolean Variable

Introducing `isTired`:

```javascript
let isTired = true; // Variable C
```

Modifying the decision condition:

```javascript
shouldDrive = hasDriversLicense && hasGoodVision && !isTired;
```

If `isTired` is `true`, then `!isTired` is `false`, leading to:

```
Someone else should drive
```

Setting `isTired` to `false` allows Sarah to drive.

## Conclusion

Logical operators help in decision-making by combining multiple conditions. Understanding AND, OR, and NOT operators is crucial for modeling real-world logic in JavaScript.
