# 🔥 Best Practices for Naming Functions in JavaScript

Function names are one of the most overlooked tools in your developer toolkit—but they can make or break the readability of your code.

In this lesson, you'll learn practical best practices for naming functions in JavaScript, so your code is clean, readable, and easy to maintain in both solo and team projects.

---

## 🚨 Why Function Names Matter

A well-named function is like a good variable: self-explanatory, easy to understand, and doesn't require you to dig through its implementation. It tells a story—what the function does and why it exists.

In JavaScript, your function names should:

- Clearly describe what the function does
- Follow a consistent naming convention
- Be easy to read and reason about at a glance

Let’s break down the best practices that’ll level up your naming game. 🚀

---

## 1. ✅ Use Action Verbs

Functions perform actions—so name them like they do.

**✅ Good Examples:**

```js
function getUserData() {} // Retrieves user data
function sendEmail() {} // Sends an email
function calculateTotal() {} // Computes total amount
function fetchPosts() {} // Loads posts from an API
```

**❌ Bad Examples:**

```js
function userData() {} // Too vague – returns it? modifies it?
function email() {} // Ambiguous – send, receive, or validate?
function total() {} // What about it? Calculate or display?
```

> 💡 **Tip:** Think of the function name as a sentence: “This function _does X_.”

---

## 2. 🐫 Use `camelCase` for Function Names

In JavaScript, the convention for function names is `camelCase`. Other styles like `snake_case` or `PascalCase` are used for different purposes.

**✅ Do this:**

```js
function getUserInfo() {}
function calculatePrice() {}
function sendNotification() {}
```

**❌ Don’t do this:**

```js
function GetUserInfo() {} // PascalCase → use only for class names
function calculate_price() {} // snake_case → non-idiomatic in JS
function sendnotification() {} // No casing → hard to read
```

> 💡 **Tip:** Reserve `PascalCase` (`UpperCamelCase`) for class names and constructors.

---

## 3. ✂️ Keep Names Short _but_ Descriptive

Strike a balance between brevity and clarity. The name should say exactly what the function does, without extra fluff.

**✅ Good Examples:**

```js
function fetchOrders() {} // Clear and concise
function validateInput() {} // Clear purpose
function startGame() {} // Self-explanatory
```

**❌ Bad Examples:**

```js
function fetchAllUserOrdersFromDatabaseTable() {} // Way too long
function doStuff() {} // Too vague
function handleClick() {} // Too generic
```

> 💡 **Tip:** 3–5 words is a sweet spot. Skip unnecessary nouns or prepositions unless they add clarity.

---

## 4. 🧩 Prefix Functions Based on Purpose

Using clear, consistent prefixes boosts readability—especially when working in teams or large codebases.

| Purpose             | Suggested Prefixes           | Example              |
| ------------------- | ---------------------------- | -------------------- |
| Fetching data       | `get`, `fetch`, `retrieve`   | `fetchUserProfile()` |
| Updating/modifying  | `update`, `set`, `modify`    | `updateCart()`       |
| Checking conditions | `is`, `has`, `can`, `should` | `isUserLoggedIn()`   |
| Handling events     | `handle`, `on`               | `handleFormSubmit()` |

> 💡 **Tip:** These patterns are everywhere in real-world codebases, from React apps to Express servers.

---

## 5. 🚫 Avoid Generic Function Names

Generic function names like `doSomething()`, `processData()`, or `handleStuff()` are red flags—they force other developers (and future you) to dig through code to understand what’s going on.

**❌ Don’t do this:**

```js
function processInfo() {} // What info? What kind of processing?
function handleStuff() {} // What "stuff"?
```

**✅ Do this:**

```js
function processUserLogin() {} // Specific and clear
function handleFileUpload() {} // Clear intent
```

> 💡 **Tip:** If the function name doesn’t tell you what it _does_, rewrite it.

---

## 6. 🔁 Use Boolean Prefixes for Yes/No Functions

Functions that return a boolean (true/false) should read like a question—starting with `is`, `has`, `can`, or `should`.

**✅ Good Examples:**

```js
function isUserAdmin() {
  return true;
}
function hasValidToken() {
  return false;
}
function canAccessDashboard() {
  return true;
}
```

**❌ Bad Examples:**

```js
function userAdmin() {} // Not clear it returns a boolean
function checkToken() {} // Ambiguous return value
function editProfile() {} // Sounds like it performs an action
```

> 💡 **Tip:** Boolean-returning function names should make it obvious you’re checking something.

---

## 7. 📦 Be Consistent Across Your Project

Inconsistent naming conventions are confusing. If you use `fetchUsers()`, don’t suddenly switch to `getPosts()` or `loadComments()`.

**✅ Consistent:**

```js
function fetchUsers() {}
function fetchPosts() {}
function fetchComments() {}
```

**❌ Inconsistent:**

```js
function getUsers() {}
function retrievePosts() {}
function loadComments() {}
```

> 💡 **Tip:** Pick a verb (e.g. `fetch`, `get`) and stick with it for similar functions.

---

## 8. 🧠 Avoid Abbreviations and Cryptic Names

Code should be written for _humans_, not just the compiler. Avoid shortening names unless they’re extremely common (like `id` or `url`).

**❌ Bad Examples:**

```js
function calcPr() {} // “Pr” → Price? Probability? Pressure?
function getUdt() {} // No clue what this does
```

**✅ Good Examples:**

```js
function calculatePrice() {}
function getUserData() {}
```

> 💡 **Tip:** Being concise is good—but _clarity_ is non-negotiable.

---

## 🧵 Summary

Let’s quickly recap:

✅ Use **action verbs**
🐫 Follow **camelCase**
✂️ Keep names **short but descriptive**
🔖 Use **prefixes** to indicate function type
📛 Avoid **generic** or **cryptic** names
🔍 Use `is`, `has`, `can`, `should` for **boolean checks**
🔁 Be **consistent** across your codebase
📢 Write code for **humans**, not just machines

---

## 🧠 Final Thoughts

Naming functions isn’t just a “nice to have”—it’s one of the easiest and most impactful ways to write clean, readable, and maintainable code.

> Think of it like this: **“Can I understand what this function does without reading the body?”**
> If yes → you nailed it.

---

> **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
