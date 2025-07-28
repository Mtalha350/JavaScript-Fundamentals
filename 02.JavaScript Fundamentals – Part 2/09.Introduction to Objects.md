# JavaScript Objects

## 🧠 Recap: Why Not Just Use Arrays?

Arrays are great for grouping related data. For example:

```javascript
const jonasArray = [
  "Jonas",
  "Schmedtmann",
  2037 - 1991,
  "teacher",
  ["Michael", "Peter", "Steven"],
];
```

But the problem is:  
❌ We can't access values by _name_ (only by index).  
✅ We intuitively know what each item _represents_, but arrays don’t let us label them.

---

## 🆕 Introducing Objects

JavaScript **Objects** solve this problem by allowing us to label values using **key-value pairs**.

### ✅ Object Syntax: Object Literal

```javascript
const jonas = {
  firstName: "Jonas",
  lastName: "Schmedtmann",
  age: 2037 - 1991,
  job: "teacher",
  friends: ["Michael", "Peter", "Steven"],
};
```

### 🔑 Terminology

- Each key is called a **property**
- The entire thing is called an **object**
- `jonas` has 5 properties in the example above

---

## ✅ Benefits of Objects

| Feature       | Arrays       | Objects                   |
| ------------- | ------------ | ------------------------- |
| Named values  | ❌ No        | ✅ Yes                    |
| Order matters | ✅ Yes       | ❌ No                     |
| Best used for | Ordered data | Unstructured / named data |
| Access method | Index-based  | Key-based                 |

---

## 🎯 When to Use What?

- Use **arrays** when data is ordered and position matters (e.g., list of scores)
- Use **objects** when data is descriptive or grouped (e.g., a person's details)

---

## ✅ Key Takeaways

- Objects use `{}` (curly braces) and are defined using **key: value** pairs
- This syntax is called **object literal syntax**
- Objects allow easy access to values by _name_, not just index
- Properties can store any type of data: strings, numbers, booleans, arrays, or even other objects
