# Functions Calling Functions

In this section, we learned about **calling one function from inside another function**, a concept frequently used in JavaScript.

### Example: Fruit Processor

We started with the `fruitProcessor` function, which initially processed fruit to make juice. However, to make juice, we added a new function to **cut the fruit** into smaller pieces before processing. This new function is called `cutFruitPieces`, which takes a fruit quantity and returns it cut into four pieces.

### Key Concepts:

1. **Calling Functions Inside Another:**

   - The `fruitProcessor` function calls `cutFruitPieces` for both apples and oranges to slice them before processing.
   - The results are captured in `applePieces` and `orangePieces` variables and used to prepare juice.

2. **Data Flow Between Functions:**

   - When `fruitProcessor(2, 3)` is called, it passes `2` for apples and `3` for oranges.
   - Inside the `fruitProcessor`, `cutFruitPieces` is called with these values. The `cutFruitPieces` function returns the number of pieces (e.g., 8 for apples and 12 for oranges), and these are used to make the juice.

3. **Code Refactoring and DRY Principle:**

   - Instead of multiplying the fruit quantity directly inside `fruitProcessor`, we use a separate function to follow the **Don't Repeat Yourself (DRY)** principle. This allows for easier updates if the cutting process changes (e.g., cutting fruit into three pieces instead of four).
   - By centralizing the logic in `cutFruitPieces`, we avoid repetitive code and reduce the chance of errors.

4. **Why Not Just Multiply?**
   - While we could directly multiply the number of apples and oranges by four, using functions makes the code more modular, readable, and maintainable, especially when the logic might change in the future.

### Example Code:

```javascript
// Function that cuts fruit into pieces
function cutFruitPieces(fruit) {
  return fruit * 4;
}

// Function that processes fruit into juice
function fruitProcessor(apples, oranges) {
  // Cutting the fruits into pieces
  const applePieces = cutFruitPieces(apples);
  const orangePieces = cutFruitPieces(oranges);

  // Making juice
  const juice = `Juice with ${applePieces} pieces of apple and ${orangePieces} pieces of orange.`;
  return juice;
}

// Calling fruitProcessor with 2 apples and 3 oranges
console.log(fruitProcessor(2, 3));
```

### Output:

```
Juice with 8 pieces of apple and 12 pieces of orange.
```

### Conclusion

By calling functions inside other functions, we can create cleaner, more modular, and reusable code. This approach helps with easier maintenance and improves code readability. The next lesson will review the fundamental principles of functions.
