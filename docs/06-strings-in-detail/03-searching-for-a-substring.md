# 🔡 Change String Case in JavaScript

Changing string case is one of those simple but super useful things you'll do all the time — whether it's formatting a name before saving it to a database or normalizing user input for comparison.

In this lesson, you’ll learn how to:

- Convert strings to **lowercase** and **uppercase**
- Understand how these methods work internally
- Avoid common pitfalls when dealing with casing in production systems

---

## ⚙️ Setup: No Extra Tools Needed

Just use your browser’s DevTools Console or run in Node.js. You can also play with this in online editors like [CodeSandbox](https://codesandbox.io/) or [JSFiddle](https://jsfiddle.net/).

---

## ✍️ Changing the Case of a String

### 🔍 What Is "Case"?

- **Uppercase** → ALL CAPS
- **Lowercase** → all small letters

These matter when you're doing:

- Case-insensitive comparisons
- Display formatting (e.g. `toUpperCase()` for headings)
- Input validation (`EMAIL@example.com` → `email@example.com`)

---

## 🧰 Built-In Methods

JavaScript gives us two simple and powerful methods:

| Method                 | Description                                               |
| ---------------------- | --------------------------------------------------------- |
| `string.toLowerCase()` | Returns a new string with **all characters in lowercase** |
| `string.toUpperCase()` | Returns a new string with **all characters in uppercase** |

> ⚠️ These **don’t change the original string** — strings in JS are immutable.

---

## 🧪 Usage Example

```javascript
const mixedCaseString = "Hello! How are you, James?";

// Convert entire string to lowercase
console.log(mixedCaseString.toLowerCase()); // "hello! how are you, james?"

// Convert entire string to uppercase
console.log(mixedCaseString.toUpperCase()); // "HELLO! HOW ARE YOU, JAMES?"
```

```javascript
/*
 Explanation:
 - .toLowerCase() returns a new version of the string with all characters in lowercase
 - .toUpperCase() returns a new version of the string with all characters in uppercase
 - The original string (mixedCaseString) stays unchanged
*/
```

---

## 🧠 How It Works (Under the Hood)

These are **string methods** (a type of function that belongs to the String object), so we invoke them using `()`:

```javascript
// Wrong: Missing function call
console.log(mixedCaseString.toLowerCase); // [Function: toLowerCase]

// Correct: Includes parentheses to call the method
console.log(mixedCaseString.toLowerCase()); // "hello! how are you, james?"
```

> 📌 **Immutability**: JS strings are **immutable** — methods like `.toLowerCase()` and `.toUpperCase()` return a **new string** instead of modifying the original. This prevents side effects and bugs in your app.

---

## 🧑‍💻 Real-World Example

Imagine you're building a login system where emails must be case-insensitive:

```javascript
const enteredEmail = "Guna@Example.com";
const storedEmail = "guna@example.com";

// Normalize both to lowercase for a consistent comparison
if (enteredEmail.toLowerCase() === storedEmail.toLowerCase()) {
  console.log("✅ Login successful");
} else {
  console.log("❌ Email does not match");
}
```

> 🔐 **Why it matters:** Email addresses should be compared case-insensitively to avoid login issues due to different capitalization styles.

---

## 💡 Pro Tips

- ❌ **Don’t assume** case-insensitive comparison happens by default — JavaScript is case-sensitive by design.
- ⚙️ **Use case normalization** before storing or comparing strings in:

  - Usernames
  - Emails
  - Search terms

- 📈 These methods run in **O(n)** time — the longer the string, the more characters it needs to scan and convert.

---

## 🧩 Edge Case Handling

```javascript
const value = null;

// Always check if a value is a string before calling string methods
if (typeof value === "string") {
  console.log(value.toLowerCase());
} else {
  console.warn("Expected a string, but got:", typeof value);
}
```

> ✅ Pro-level code always validates inputs before calling string methods to avoid runtime errors like `TypeError: Cannot read properties of null`.

---

## ✅ Recap

In this lesson, you learned:

- How to convert strings to **uppercase** and **lowercase**
- That these methods are **non-mutating** and return new strings
- Why case transformation is essential in **validation**, **search**, and **data normalization**

> Next up: 🔍 [**Getting a Substring**](./04-getting-a-substring.md) — coming into play!

---

> **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
