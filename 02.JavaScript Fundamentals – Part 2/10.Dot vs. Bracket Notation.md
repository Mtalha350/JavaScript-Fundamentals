## 📘 Object Property Access & Manipulation in JavaScript

### 🔍 **Accessing Properties**

JavaScript provides two ways to **retrieve data from objects**:

#### 1. **Dot Notation**

Simple and clean:

```js
console.log(jonas.lastName); // 'Schmedtmann'
```

#### 2. **Bracket Notation**

Allows dynamic property access:

```js
console.log(jonas["lastName"]); // 'Schmedtmann'
```

##### ✔ Use Case for Bracket Notation:

When you **compute property names dynamically**:

```js
const nameKey = "Name";
console.log(jonas["first" + nameKey]); // 'Jonas'
console.log(jonas["last" + nameKey]); // 'Schmedtmann'
```

---

### 🧠 **Dynamic Property Access via User Input**

Use `prompt()` to ask the user what property to display:

```js
const interestedIn = prompt(
  "What do you want to know about Jonas? Choose between firstName, lastName, age, job, and friends"
);

if (jonas[interestedIn]) {
  console.log(jonas[interestedIn]);
} else {
  console.log(
    "Wrong request! Choose between firstName, lastName, age, job, and friends."
  );
}
```

> ❗ Dot notation won't work for dynamic input like `jonas.interestedIn`

---

### ➕ **Adding New Properties**

#### Using Dot Notation:

```js
jonas.location = "Portugal";
```

#### Using Bracket Notation:

```js
jonas["twitter"] = "@JonasSchmedtman";
```

---

### 🧩 **Mini Challenge**

Print this sentence **dynamically**:

```
"Jonas has 3 friends, and his best friend is called Michael."
```

#### ✅ Solution:

```js
console.log(
  `${jonas.firstName} has ${jonas.friends.length} friends, and his best friend is called ${jonas.friends[0]}.`
);
```

---

### ✅ **Recap: When to Use Which**

- Use **dot notation** when you know the exact property name.
- Use **bracket notation** when the property name is **computed** or **dynamic**.
