# 📘 JavaScript Operators and Equality

JavaScript operators are the unsung heroes of programming—they power everything from basic math to complex condition checks. In this module, we’ll break down the most essential types of operators, showing _how_ and _why_ they’re used in real-world code.

> 📄 **For more details, refer to the following documents:** [Operators and Equality.md](./operators-and-equality.md)

---

## 🧠 Introduction to JavaScript Operators

Operators perform operations on _operands_ (like variables or values) and return results. They’re a fundamental building block in programming logic.

### 📌 What You’ll Learn:

- [Operators Intro](./01-operators-intro.md)
- [Arithmetic Operators](./02-arithmetic-operators.md)
- [Comparison Operators and Equality](./03-comparison-operators-&-equality.md)
- [Strict (`===`) vs Loose (`==`) Equality](./04-strict-vs-loose-equality.md)
- [Logical Operators – `&&`, `||`, `!`](./05-logical-operators.md)
- [Assignment Operators](./06-assignment-operators.md)

> 🎯 You’ll master these with practical examples so you can write clean, bug-free code like a pro.

---

## ➕ Basic Math Operations in JavaScript

These are the bread and butter of any program involving numbers—used in everything from simple counters to complex financial calculations.

### 🔢 Core Arithmetic Operators

```js
// Addition: Adds two numbers
const sum = 10 + 5; // 15

// Subtraction: Subtracts right from left
const diff = 15 - 2; // 13

// Multiplication: Multiplies two numbers
const product = 6 * 4; // 24

// Division: Divides left by right
const quotient = 15 / 3; // 5

// Modulus: Gets the remainder after division
const remainder = 17 % 5; // 2

// Exponentiation: Raises to a power
const cube = 3 ** 3; // 27

// Increment and Decrement
let count = 5;
count++; // 6 (post-increment)
count--; // 5 (post-decrement)
```

### ✅ Why It Matters:

Every app—from to-do lists to stock trading systems—relies on these. They’re also used heavily in loops, data processing, and performance tracking.

---

## 🔍 Understanding Comparison Operators

Comparison operators return a Boolean (`true` or `false`) based on how two values relate to each other.

### 📘 Core Operators:

```js
5 > 3; // true (greater than)
5 < 3; // false (less than)
5 >= 5; // true (greater than or equal)
5 <= 4; // false (less than or equal)
5 == "5"; // true (loose equality: type is ignored)
5 === "5"; // false (strict equality: type must match)
5 != "5"; // false (loose inequality)
5 !== "5"; // true (strict inequality)
```

> 🧠 Tip: Always prefer `===` and `!==` to avoid bugs from type coercion.

---

## 🚧 Strict vs Loose Equality in Depth

Let’s talk about **why** using strict equality (`===`) is best practice.

### 📌 What’s the Difference?

```js
10 == "10"; // true (loose equality, JavaScript converts types)
10 === "10"; // false (strict equality, no conversion)
```

### ⚠️ Real-World Gotcha:

```js
"" == 0; // true 😨
false == 0; // true 😨
null == undefined; // true 😬
```

These cause subtle bugs in form validation, API responses, or condition checks. Stick to `===` and `!==` unless you _really_ know what you’re doing.

---

## 🔗 Logical Operators: Combining Conditions

Logical operators let you build complex conditions in `if` statements, loops, filters, etc.

### ✅ AND (&&)

Returns `true` only if **both** conditions are true.

```js
const loggedIn = true;
const hasAccess = true;

if (loggedIn && hasAccess) {
  console.log("Access granted");
}
```

### 🔁 OR (||)

Returns `true` if **at least one** condition is true.

```js
const isAdmin = false;
const isEditor = true;

if (isAdmin || isEditor) {
  console.log("Edit permission granted");
}
```

### 🚫 NOT (!)

Reverses the truthiness of a value.

```js
const isBlocked = false;

if (!isBlocked) {
  console.log("User can proceed");
}
```

> 🔍 Pro Tip: Use logical operators in short-circuit expressions for defaults:

```js
const username = input || "Guest"; // fallback to "Guest" if input is falsy
```

---

## 📝 Assignment Operators: Shortcuts for Cleaner Code

Assignment operators are how you set and update variable values. They also allow more concise math logic.

### 👇 Examples:

```js
let total = 10;

// Add 5 to total
total += 5; // 15

// Subtract 3
total -= 3; // 12

// Multiply by 2
total *= 2; // 24

// Divide by 4
total /= 4; // 6
```

> 💡 These work with strings too:

```js
let greeting = "Hello";
greeting += " World"; // "Hello World"
```

---

## ❓ Conditional (Ternary) Operator

A shorthand for `if-else` logic in a single line.

```js
const age = 20;
const status = age >= 18 ? "Adult" : "Minor"; // "Adult"
```

### 🧠 Why Use It?

Cleaner and faster to read when assigning values based on conditions. Great for rendering UI states, setting defaults, etc.

---

## 📦 What’s Next?

We’ve covered the foundations of JavaScript operators. Next, we’ll dig into:

- 🧮 Advanced math patterns
- 🧠 Control flow strategies
- 🏗️ Building mini-projects using these concepts

---

## 🔗 Resources

- [MDN JavaScript Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)
- [JavaScript.info - Operators](https://javascript.info/operators)
- [ESLint Rules for Equality](https://eslint.org/docs/latest/rules/eqeqeq)

---

> 🔙 **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
