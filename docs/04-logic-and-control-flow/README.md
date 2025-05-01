# 🔁 Logic and Control Flow

Mastering control flow in JavaScript means learning how your code makes decisions and repeats actions. This chapter covers essential tools like conditionals (`if`, `else`, `switch`), logical operators (`&&`, `||`, `!`), and loops (`for`, `while`). These are the building blocks of real-world apps — from form validation to navigation logic, recommendation engines, and more.

> 📄 **For more details, refer to the following documents:** [logic-and-control-flow.md](./logic-and-control-flow.md)

---

## 🧠 Understanding `if` Statements in JavaScript

Conditional logic is a core part of programming. The `if` statement allows your code to "decide" what to do based on whether a condition is true or false.

### 🛠️ What is an `if` statement?

An `if` statement checks a condition, and if it's `true`, runs a block of code. If not, it skips that block.

```js
const age = 20;

if (age >= 18) {
  console.log("Welcome to the club!");
}
```

> ✅ This will print “Welcome to the club!” because the condition `age >= 18` is `true`.

### 📦 The Full Structure: `if`, `else if`, `else`

```js
const age = 16;

if (age >= 18) {
  console.log("Access granted");
} else if (age >= 13) {
  console.log("Teen access");
} else {
  console.log("Access denied");
}
```

### 🧩 How it works:

- JavaScript checks each condition from top to bottom.
- The first `true` condition runs its block — then **stops** checking.
- If none match, the `else` block runs as a fallback.

### 🔍 Common Use Case: Age Checks, Login States, Feature Flags

```js
const isLoggedIn = false;

if (isLoggedIn) {
  console.log("Show dashboard");
} else {
  console.log("Show login page");
}
```

### ⚠️ Dev Tip: Be careful with condition order!

```js
const score = 95;

if (score > 50) {
  console.log("Passed");
} else if (score > 90) {
  console.log("Top performer");
}
```

> ❌ This prints “Passed” even for 95 — because the `> 50` check comes first and passes.

---

## ✅ Key Takeaways

- `if` lets your program react to conditions.
- Use `else if` for multiple options.
- Use `else` for the default case.
- Only the first matched condition runs.
- Always watch your condition order to avoid logic bugs.

---

> **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
