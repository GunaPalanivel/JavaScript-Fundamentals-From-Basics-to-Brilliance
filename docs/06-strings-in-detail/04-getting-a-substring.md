# 🔍 Searching for a Substring in JavaScript

Whether you're validating user input, parsing data from an API, or building a search feature, **substring detection** is a core string operation in JavaScript.

This lesson covers different methods to:

- Search for **presence** or **position** of text inside strings
- Understand **case sensitivity** and **search direction**
- Choose the right tool for the job based on your use case

---

## ⚙️ Setup: Use Any JavaScript Runtime

You can try these examples in:

- Browser DevTools Console
- Node.js environment
- Online sandboxes like [CodeSandbox](https://codesandbox.io/), [Replit](https://replit.com/), or [JSFiddle](https://jsfiddle.net/)

---

## 📦 Core String Search Methods

Here are the **most common and useful** substring methods:

| Method          | Returns          | Use Case                                 |
| --------------- | ---------------- | ---------------------------------------- |
| `indexOf()`     | Index (or -1)    | Find **first match** from the start      |
| `lastIndexOf()` | Index (or -1)    | Find **last match** from the end         |
| `includes()`    | `true` / `false` | Check **presence only**                  |
| `startsWith()`  | `true` / `false` | Check if string starts with a given text |
| `endsWith()`    | `true` / `false` | Check if string ends with a given text   |

---

## 🧪 Usage Examples

### 🔎 `indexOf()` – Find First Occurrence

```javascript
const exampleString = "I love ducks, he said, ducks are great!";

// Find index of the first occurrence of 'ducks'
console.log(exampleString.indexOf("ducks")); // 7

// Case-sensitive: 'Ducks' (capital D) is not the same as 'ducks'
console.log(exampleString.indexOf("Ducks")); // -1
```

```javascript
/*
 .indexOf returns the position of the first match.
 If no match is found, it returns -1.
 It's case-sensitive — so watch out for mismatched capitalization!
*/
```

### 🧭 `indexOf(substr, fromIndex)` – Start Search After a Given Index

```javascript
// Start searching from position 8 to find the next occurrence of 'ducks'
console.log(exampleString.indexOf("ducks", 8)); // 23
```

```javascript
// This helps you loop through multiple matches in a large string.
```

---

### 🔁 `lastIndexOf()` – Find Last Occurrence from End

```javascript
// Find last occurrence of 'ducks' by searching from the end
console.log(exampleString.lastIndexOf("ducks")); // 23
```

```javascript
/*
 lastIndexOf searches *backward* from the end.
 Useful when you care about the last instance — e.g. in logs or version strings.
*/
```

---

### ✅ `includes()` – Check If Substring Exists

```javascript
// Check if 'ducks' is in the string (boolean result)
console.log(exampleString.includes("ducks")); // true
```

```javascript
/*
 .includes is clean and semantic when you only need a true/false answer.
 Ideal for conditionals and validations.
*/
```

You can also specify a start position:

```javascript
console.log(exampleString.includes("ducks", 24)); // false
```

---

### 🚀 `startsWith()` & `endsWith()` – Exact Start or End Matching

```javascript
console.log(exampleString.startsWith("I")); // true
console.log(exampleString.endsWith("ducks")); // false
```

```javascript
/*
 .startsWith checks if the string begins with a given substring
 .endsWith checks if the string ends with a given substring
 Useful for parsing commands, file names, or input validation
*/
```

---

## 📌 Real-World Use Case: Case-Insensitive Keyword Filter

```javascript
const userInput = "Quack";
const sourceText = "I love ducks, he said, ducks are great!";

// Normalize case before search for consistent matching
const found = sourceText.toLowerCase().includes(userInput.toLowerCase());

console.log(found); // true
```

```javascript
/*
 Normalize both strings to lowercase before comparison
 Ensures match regardless of input capitalization (UX-friendly!)
*/
```

---

## ⚙️ Performance & Optimization Tips

| Method        | Time Complexity | Notes                                  |
| ------------- | --------------- | -------------------------------------- |
| `indexOf`     | O(n)            | Stops early when match found           |
| `includes`    | O(n)            | Internally uses indexOf under the hood |
| `lastIndexOf` | O(n)            | Starts from the end                    |
| `startsWith`  | O(k)            | k = length of prefix                   |
| `endsWith`    | O(k)            | k = length of suffix                   |

> 💡 If you're scanning large strings or files, use `startsWith/endsWith` for faster prefix/suffix checks rather than regex or full scans.

---

## 🚨 Edge Case Considerations

```javascript
const value = null;

// Always validate before using string methods
if (typeof value === "string") {
  console.log(value.includes("test"));
} else {
  console.warn("Expected a string, but got:", typeof value);
}
```

```javascript
/*
 Avoid runtime errors by ensuring the input is a string
 Defensive programming saves time debugging crashes in production
*/
```

---

## ✅ Recap

You just learned how to:

- Use `indexOf()` and `lastIndexOf()` to find positions of substrings
- Use `includes()`, `startsWith()`, and `endsWith()` for boolean checks
- Handle casing issues and input validation like a pro

> 🔍 These string search tools are foundational in everything from search engines to form validation to building filters for dashboards.

> Next up: 🔍 [**Split a String**](./05-split-a-string.md) — coming into play!

---

> **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
