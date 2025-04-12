# Summary: Introduction to Arrays in JavaScript

### What are Arrays?

Arrays in JavaScript are used to store multiple values in a single variable. They are particularly useful when you have multiple related values that you want to keep together.

### Creating Arrays

Arrays can be created in two ways:

1. **Using brackets (Literal Syntax)**:
   ```javascript
   const friends = ["Michael", "Steven", "Peter"];
   ```

2. **Using the `new Array()` constructor**:
   ```javascript
   const years = new Array(1991, 1984, 2008, 2020);
   ```

While both methods work, the bracket syntax is more commonly used due to its simplicity.

### Accessing Array Elements

Array elements are accessed using square brackets and zero-based indexing:

```javascript
console.log(friends[0]); // Michael
console.log(friends[2]); // Peter
```

### Array Length

The `length` property returns the number of elements in the array:

```javascript
console.log(friends.length); // 3
```

### Accessing the Last Element

To access the last element of an array, subtract one from the array's length:

```javascript
console.log(friends[friends.length - 1]); // Peter
```

### Modifying Array Elements

You can modify elements in an array using the square bracket notation:

```javascript
friends[2] = "Jay"; // Replace Peter with Jay
```

### Mutability of Arrays

Even if an array is declared with `const`, its elements can be modified:

```javascript
const friends = ["Michael", "Steven", "Peter"];
friends[2] = "Jay"; // Allowed
```

However, replacing the entire array will result in an error:

```javascript
friends = ["Bob", "Ellis"]; // Error: Assignment to constant variable
```

### Arrays with Mixed Data Types

Arrays can hold values of different types (e.g., strings, numbers, other arrays):

```javascript
const jonas = ["Jonas", "Doe", 30, [1, 2, 3]];
```

### Practical Example: Calculating Ages

If you want to calculate ages for a list of birth years, you can use an array and a function to process the values:

```javascript
const years = [1990, 1967, 2002, 2010, 2018];
const ages = years.map((year) => calcAge(year)); // Using the map method to apply calcAge on all elements
```

### Conclusion

Arrays are a powerful data structure in JavaScript that allow you to store and manipulate multiple related values. They can hold values of different types and can be accessed or modified using index notation. Arrays are essential for efficiently working with groups of data.

