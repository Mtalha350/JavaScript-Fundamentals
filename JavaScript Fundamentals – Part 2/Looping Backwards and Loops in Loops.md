# Exploring Loops in JavaScript

In this lecture, we're gonna do two interesting things.

First, we will loop over an array backwards, and then second, we will also create a loop inside another loop.

## Looping Over an Array Backwards

Let's have some more fun with arrays now. We'll start by using the `Jonas` array again and forget about one of the elements.

So, in the previous lecture, we looped over the array from the beginning, starting with index `0`, then `1`, all the way to `4`.

Now, we want to loop over the array starting from the last index (4) and go backwards. So, we'll start at index `4`, then move to `3`, then `2`, and so on, all the way back to `0`.

### Code Implementation

```javascript
const Jonas = ["Jonas", "Schmedtmann", 1991, "teacher", true];

// Looping backwards through the array
for (let i = Jonas.length - 1; i >= 0; i--) {
  console.log(Jonas[i]);
}
```

### Explanation:

- We set the counter `i` to `Jonas.length - 1` (the last index of the array).
- The loop condition ensures that we loop until `i` is greater than or equal to `0`.
- We decrement the counter (`i--`) to move backwards through the array.

This method prints the elements of the array in reverse order, from the last element to the first.

---

## Creating a Loop Inside Another Loop

Now, let's move to a more advanced concept: creating a loop inside another loop. This is commonly known as a "nested loop."

### Scenario: Repetitions for Multiple Exercises

Consider the example of performing weightlifting exercises. Suppose we have three different exercises, and for each exercise, we want to repeat it five times. This gives a total of 15 repetitions, with each exercise being repeated five times.

To achieve this, we need a loop inside another loop.

### Code Implementation

```javascript
// Outer loop for exercises
for (let exercise = 1; exercise <= 3; exercise++) {
  console.log(`Exercise ${exercise}:`);

  // Inner loop for repetitions
  for (let rep = 1; rep <= 5; rep++) {
    console.log(`  Lifting weight repetition ${rep}`);
  }
}
```

### Explanation:

- The outer loop handles the three exercises (`exercise 1`, `exercise 2`, `exercise 3`).
- The inner loop repeats each exercise five times (one for each repetition).
- After each inner loop finishes (i.e., after all repetitions for one exercise are completed), the outer loop moves to the next exercise.

### Output:

```text
Exercise 1:
  Lifting weight repetition 1
  Lifting weight repetition 2
  Lifting weight repetition 3
  Lifting weight repetition 4
  Lifting weight repetition 5
Exercise 2:
  Lifting weight repetition 1
  Lifting weight repetition 2
  Lifting weight repetition 3
  Lifting weight repetition 4
  Lifting weight repetition 5
Exercise 3:
  Lifting weight repetition 1
  Lifting weight repetition 2
  Lifting weight repetition 3
  Lifting weight repetition 4
  Lifting weight repetition 5
```

Here, the outer loop handles the exercises, and the inner loop manages the repetitions for each exercise. The result is 15 repetitions in total.

---

## Conclusion

These exercises demonstrate two key concepts:

1. **Looping backwards through an array**: By adjusting the loop's start, condition, and update, we can loop through an array in reverse order.
2. **Nested loops**: A loop inside another loop allows us to repeat tasks multiple times within a single iteration, like performing several exercises with multiple repetitions.

Although these patterns may not be used every day, they are valuable for more complex problems and demonstrate the power and flexibility of loops in JavaScript.
