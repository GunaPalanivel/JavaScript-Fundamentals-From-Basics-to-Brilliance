# 🧠 Understanding `return` in JavaScript Functions

The `return` statement is a core part of how functions work in JavaScript. It controls two things:

1. **What value the function gives back**
2. **When the function stops executing**

This is key not just for getting output, but for understanding the **flow of logic** inside your functions.

---

## 🔁 Default Return: `undefined`

In JavaScript, **every function returns `undefined` by default** — unless you tell it to return something else.

```js
function greet() {
  console.log("Hello!");
}

const result = greet();
console.log(result); // undefined
```

📝 Since we didn’t return anything, JavaScript assumes we meant to return `undefined`.

---

## ➕ Example: Return a Sum

Let’s write a simple function that returns a sum.

```js
// Adds two numbers together and returns the result
function add(a, b) {
  return a + b;
}

const sum = add(2, 2);
console.log(sum); // 4
```

### 🔍 Why it works:

- The `return` keyword sends the result of `a + b` back to whoever called the function.
- We store that result in `sum`, then log it.

---

## ⛔ Return Ends Execution

Here’s something most beginners miss:

> **As soon as a function hits a `return` statement, it exits immediately.**
> Anything after `return` is skipped completely.

### ❌ Example: Only the first return matters

```js
function test() {
  return true;
  return false; // ❌ never reached
}

console.log(test()); // true
```

Even though there are two `return`s, only the first one is ever run. The second is **unreachable**.

---

## 🧪 Add Logs to See It in Action

```js
function test() {
  console.log(1); // ✅ This runs
  return true; // ✅ This runs
  console.log(2); // ❌ Never runs
  return false; // ❌ Never runs
  console.log(3); // ❌ Never runs
}

test(); // Only logs 1, then exits
```

This proves that **`return` stops the function cold**. It's like saying: "My job here is done."

---

## 📁 Function Storage vs Execution

When you define a function like this:

```js
function greet() {
  console.log("Hello");
}
```

JavaScript **stores it** in memory. But it **doesn’t run** it until you **call it**:

```js
greet(); // Now it runs
```

This is why we say JavaScript runs **top to bottom**, but skips function bodies unless called.

---

## 🔄 Arrow Functions & Return

Let’s revisit arrow functions quickly. You saw this earlier:

```js
// Arrow function that returns the square of a number
const square = (num) => {
  return num * num;
};
```

This is totally valid — but we can make it shorter.

### 🧪 If there's only a `return`, write it like this:

```js
// One-liner arrow function using implicit return
const square = (num) => num * num;
```

- ✅ No curly braces
- ✅ No `return` keyword
- ✅ Cleaner and more readable

Just remember: **This only works when your function has one expression to return.**

---

## ✅ Summary

Here's what you’ve learned:

- Every function returns `undefined` by default unless you use `return`.
- `return` sends a value out and immediately stops the function.
- Only the first `return` runs — everything after is skipped.
- You can store return values in variables.
- Arrow functions with a single `return` can be written in one line (implicit return).

> ➜ Next up: 🔍 [**Arrow Function**](./04-arrow-functions.md) — coming into play!

---

> 🔙 **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
