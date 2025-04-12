# Let's Keep Exploring Objects

This lecture will bring us to **object methods**.

We learned that objects, just like arrays, can hold different types of data. They can even hold arrays and other objects inside them. But we can take this even further.

Remember: **functions are just another type of value**. That means we can create a key-value pair in which the value is a function. And so we can add functions to objects!

## Adding a Function to an Object

Let’s revisit an object and update it. We'll simplify it to just include:

```js
const jonas = {
  birthYear: 1991,
  hasDriversLicense: true,
  calcAge: function (birthYear) {
    return 2037 - birthYear;
  },
};
```

This is very similar to how we create function expressions. The difference is that `calcAge` is now a property of the `jonas` object, not a standalone variable.

> 🔹 A function attached to an object is called a **method**.

Using a function **declaration** inside an object won’t work:

```js
// ❌ This won't work
const jonas = {
  function calcAge(birthYear) {
    return 2037 - birthYear;
  }
};
```

Instead, we must use a **function expression**.

## Accessing Methods

You can call the method just like any other function:

```js
console.log(jonas.calcAge(1991)); // 46
```

Or using bracket notation:

```js
console.log(jonas); // 46
```

## Avoiding Repetition: Using `this`

If `birthYear` is already defined in the object, why pass it in manually?

We can use the special `this` keyword:

```js
const jonas = {
  birthYear: 1991,
  hasDriversLicense: true,
  calcAge: function () {
    return 2037 - this.birthYear;
  },
};
```

Now:

```js
console.log(jonas.calcAge()); // 46
```

The keyword `this` refers to the object **calling** the method — in this case, `jonas`.

If you used `jonas.birthYear` inside `calcAge`, and later changed the object name to `jonas2`, you’d also need to update the method. But with `this`, the code remains flexible.

## Caching a Computed Value

If we need to use the age multiple times, calculating it again and again is inefficient. Instead, we can **store** it after the first calculation:

```js
const jonas = {
  birthYear: 1991,
  hasDriversLicense: true,
  calcAge: function () {
    this.age = 2037 - this.birthYear;
    return this.age;
  },
};
```

Now:

```js
jonas.calcAge();
console.log(jonas.age); // 46
```

We’ve added a new property `age` dynamically to the object.

> ✅ This is a great example of using methods to not only compute but also **store** useful information for later use.

## Summary

- Objects can hold **functions** as values — these are called **methods**.
- Use **function expressions** inside objects, not declarations.
- Use `this` to refer to the object calling the method.
- Storing computed values like `age` as properties can improve efficiency.
