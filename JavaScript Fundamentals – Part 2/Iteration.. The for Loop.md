# JavaScript Fundamentals: Loops

## Introduction

Previously, we discussed the `if-else` statement as a **control structure**. In this section, we’ll explore another crucial control structure: **loops**.

Loops allow us to **automate repetitive tasks**—those we’d otherwise perform multiple times manually.

---

## 🏋️‍♂️ Loop Analogy: The Gym

Imagine going to the gym and performing an exercise, like lifting weights, 10 times. Manually writing the log 10 times in code would look like:

```javascript
console.log("Lifting weights repetition 1 🏋️‍♂️");
console.log("Lifting weights repetition 2 🏋️‍♂️");
// ...
console.log("Lifting weights repetition 10 🏋️‍♂️");
```

This approach violates the **Don't Repeat Yourself (DRY)** principle.

---

## 🔁 The `for` Loop

To avoid repetition, we use a **loop** to run the same block of code multiple times.

### Basic Syntax:

```javascript
for (let rep = 1; rep <= 10; rep++) {
  console.log(`Lifting weights repetition ${rep} 🏋️‍♂️`);
}
```

### Breakdown:

1. **Initialization**: `let rep = 1`
   - Create a counter variable.
2. **Condition**: `rep <= 10`
   - Loop runs **while** this is true.
3. **Final Expression**: `rep++`
   - Increments the counter after each iteration.

### Note:

```markdown
💡 The loop continues to run WHILE the condition is true.
```

---

## ✅ Why This Works

- Starts at `rep = 1`.
- As long as `rep <= 10`, the loop continues.
- After printing each string, `rep` is incremented.
- Once `rep` becomes `11`, the loop stops.

---

## 📈 Dynamic Output with Template Literals

Instead of hardcoding the number:

```javascript
console.log(`Lifting weights repetition ${rep} 🏋️‍♂️`);
```

This uses a **template string** to insert the current repetition dynamically.

---

## 🧠 Recap

- Loops help avoid code repetition.
- A `for` loop is perfect when you know how many times to repeat.
- You can customize:
  - **Start point** (e.g., `rep = 5`)
  - **End condition** (e.g., `rep <= 30`)
- Each loop:
  - Logs the string with the current count.
  - Increments `rep` by 1.
  - Stops when the condition becomes false.

---

## 🛠 Try It Out

Experiment with:

- Changing the **starting repetition**.
- Modifying the **end condition**.
- Customizing the **output message**.
