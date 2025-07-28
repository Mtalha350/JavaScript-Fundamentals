# JavaScript Array Methods

JavaScript provides a range of built-in array methods that allow you to manipulate arrays efficiently. Here are some basic methods you need to know:

## 1. `push()`

- Adds one or more elements to the **end** of an array.
- **Example:**
  ```javascript
  let friends = ["Michael", "Steven", "Peter"];
  friends.push("Jay");
  console.log(friends); // ['Michael', 'Steven', 'Peter', 'Jay']
  ```
- Returns the **new length** of the array:
  ```javascript
  let newLength = friends.push("John");
  console.log(newLength); // 5
  ```

## 2. `unshift()`

- Adds one or more elements to the **beginning** of an array.
- **Example:**
  ```javascript
  let friends = ["Michael", "Steven", "Peter"];
  friends.unshift("John");
  console.log(friends); // ['John', 'Michael', 'Steven', 'Peter']
  ```
- Returns the **new length** of the array:
  ```javascript
  let newLength = friends.unshift("Jake");
  console.log(newLength); // 5
  ```

## 3. `pop()`

- Removes the **last** element from an array.
- **Example:**
  ```javascript
  let friends = ["Michael", "Steven", "Peter", "Jay"];
  let removedElement = friends.pop();
  console.log(friends); // ['Michael', 'Steven', 'Peter']
  console.log(removedElement); // 'Jay'
  ```

## 4. `shift()`

- Removes the **first** element from an array.
- **Example:**
  ```javascript
  let friends = ["Michael", "Steven", "Peter"];
  let removedElement = friends.shift();
  console.log(friends); // ['Steven', 'Peter']
  console.log(removedElement); // 'Michael'
  ```

## 5. `indexOf()`

- Returns the index of the first occurrence of a specified element.
- **Example:**

  ```javascript
  let friends = ["Michael", "Steven", "Peter"];
  let index = friends.indexOf("Steven");
  console.log(index); // 1
  ```

- Returns `-1` if the element is not found:
  ```javascript
  let index = friends.indexOf("John");
  console.log(index); // -1
  ```

## 6. `includes()`

- Checks if an array contains a specified element.
- **Example:**

  ```javascript
  let friends = ["Michael", "Steven", "Peter"];
  let result = friends.includes("Steven");
  console.log(result); // true
  ```

- Returns `false` if the element is not found:

  ```javascript
  let result = friends.includes("John");
  console.log(result); // false
  ```

- Uses **strict equality** for the check:
  ```javascript
  let friends = [23, "Michael", "Steven"];
  console.log(friends.includes(23)); // true
  console.log(friends.includes("23")); // false
  ```

These are some of the most commonly used methods for working with arrays in JavaScript. There are many more, but these form the foundation for basic array manipulation.
