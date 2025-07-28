# Exploring More Features of the For Loop in JavaScript

## Looping Through Arrays

Let's now explore some more features of the `for` loop and create a somewhat more useful example. One of the most used applications of `for` loops is to loop through an array.

### Example: Looping Through Jonas Array

Consider the following array, which was previously discussed:

```javascript
const Jonas = ["Jonas", "Schmedtmann", 1991, "teacher", true];
```

Now, we want to loop through this array and log every element to the console. We can do this using a `for` loop.

### Code Implementation

```javascript
const Jonas = ["Jonas", "Schmedtmann", 1991, "teacher", true];

// Loop through the array
for (let i = 0; i < Jonas.length; i++) {
  console.log(Jonas[i]);
}
```

### Explanation:

- We initialize a counter `i` at 0 because arrays are zero-based in JavaScript.
- The loop continues as long as `i` is less than the length of the array.
- We log each element of the array using `Jonas[i]`.

### Adding Elements to the Array

If we add another element to the array, like `true`, we would need to update the loop to dynamically handle the length of the array:

```javascript
Jonas.push(true);

// Loop through the array again
for (let i = 0; i < Jonas.length; i++) {
  console.log(Jonas[i]);
}
```

By replacing the hardcoded length with `Jonas.length`, we ensure that the loop adapts to changes in the array's size.

### Type of Each Element

We can also log the type of each element in the array using `typeof`:

```javascript
for (let i = 0; i < Jonas.length; i++) {
  console.log(typeof Jonas[i]);
}
```

### Creating a New Array Based on the Original Array

Let's say we want to create a new array that contains the types of each element in the original array:

```javascript
let types = [];

for (let i = 0; i < Jonas.length; i++) {
  types.push(typeof Jonas[i]);
}

console.log(types);
```

This will log an array with the types of the elements in `Jonas`.

---

## Practical Example: Calculating Ages from Birth Years

Let's now work with an array of birth years and calculate the ages for each year.

### Example: Birth Years to Ages

```javascript
const years = [1991, 2007, 1969, 2020];
let ages = [];
const currentYear = 2037;

for (let i = 0; i < years.length; i++) {
  ages.push(currentYear - years[i]);
}

console.log(ages);
```

This code calculates the age for each birth year and stores it in the `ages` array.

---

## Special Looping Statements: `continue` and `break`

JavaScript's `for` loop also has two important control statements: `continue` and `break`.

### `continue` Statement

The `continue` statement is used to skip the current iteration of the loop and continue to the next iteration.

Example:

```javascript
for (let i = 0; i < Jonas.length; i++) {
  if (typeof Jonas[i] !== "string") continue;
  console.log(Jonas[i]);
}
```

This will only log elements that are strings, skipping others like numbers or booleans.

### `break` Statement

The `break` statement is used to exit the entire loop, not just the current iteration.

Example:

```javascript
for (let i = 0; i < Jonas.length; i++) {
  if (typeof Jonas[i] === "number") break;
  console.log(Jonas[i]);
}
```

This will log the elements until a number is encountered, after which the loop will terminate.

---

## Conclusion

This exploration of the `for` loop in JavaScript covered:

- Looping through arrays and logging elements.
- Dynamically handling array lengths.
- Creating new arrays based on existing data.
- Calculating ages from an array of birth years.
- Using `continue` and `break` to control the flow of loops.
