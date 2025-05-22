# **🧪 Arithmetic Operators in Action**

In this lesson, you'll learn how to use **arithmetic operators** in JavaScript to perform foundational math operations. These are **critical building blocks** for solving problems, manipulating data, and writing any kind of logic in your code — from simple calculations to building entire logic layers in real-world apps.

---

## 🚀 Introduction

Arithmetic operations are everywhere in JavaScript: validating forms, calculating totals, animating UIs, tracking state, and more. Here, we’ll explore the core operators:

- ➕ Addition (`+`)
- ➖ Subtraction (`-`)
- ✖ Multiplication (`*`)
- ➗ Division (`/`)
- 🧮 Modulus / Remainder (`%`)
- 🔼 Exponentiation (`**`)
- ⬆ Increment (`++`)
- ⬇ Decrement (`--`)

---

## ⚙️ Setup & Usage

Below is a clean, commented code snippet demonstrating each operation in practice:

```javascript
// Addition (+)
// Adds two numbers together
const sum = 10 + 5;
console.log("Addition: 10 + 5 =", sum); // Output: 15

// Subtraction (-)
// Subtracts the right number from the left
const difference = 20 - 7;
console.log("Subtraction: 20 - 7 =", difference); // Output: 13

// Multiplication (*)
// Multiplies two numbers
const product = 6 * 4;
console.log("Multiplication: 6 * 4 =", product); // Output: 24

// Division (/)
// Divides the left number by the right number
const quotient = 15 / 3;
console.log("Division: 15 / 3 =", quotient); // Output: 5

// Modulus (%)
// Returns the remainder after division
// Example: 17 divided by 5 is 3 with a remainder of 2
const remainder = 17 % 5;
console.log("Modulus: 17 % 5 =", remainder); // Output: 2

// Exponentiation (**)
// Raises the left number to the power of the right number
// Example: 3 to the power of 3 (3 * 3 * 3)
const power = 3 ** 3;
console.log("Exponentiation: 3 ** 3 =", power); // Output: 27

// Increment (++)
// Increases a number by 1
let incrementValue = 5;
incrementValue++; // Same as incrementValue = incrementValue + 1
console.log("Increment: 5++ =", incrementValue); // Output: 6

// Decrement (--)
// Decreases a number by 1
let decrementValue = 8;
decrementValue--; // Same as decrementValue = decrementValue - 1
console.log("Decrement: 8-- =", decrementValue); // Output: 7
```

---

## 🧠 Tips & Real-World Insights

- `++` and `--` can be used **before or after** a variable (`++x` vs `x++`), which changes _when_ the increment happens. Use `x++` to increment **after** using the value, `++x` to increment **before**.
- `%` is super useful in **looping patterns**, like wrapping index positions in circular arrays or toggling states.
- `**` works cleanly for power operations, but you can also use `Math.pow()` if you need compatibility with older browsers (pre-ES2016).
- Always handle **division by zero** in real-world code. JavaScript returns `Infinity` or `NaN`, which can cause downstream bugs.

---

## 🛠️ Bonus: Use Cases in Real Projects

- **E-commerce App**: Calculate total prices (`price * quantity`), apply discounts (`total - couponValue`), and show remainder stock.
- **Game Logic**: Use `%` to cycle through players or weapons. Use `++` to increase score.
- **Animations**: Apply increments to control movement or opacity over time.

---

## 📚 Resources

- [MDN - Arithmetic Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)
- [JavaScript Info – Operators](https://javascript.info/operators)

---

## ✅ Summary

Math operations in JavaScript are simple but powerful. They're the **foundation for everything** from game engines to dashboards. Mastering these is a **non-negotiable first step** toward becoming a confident JavaScript developer.

> ➜ Next up: 🔍 [**Comparison Operators**](./03-comparison-operators-&-equality.md) — where logic starts coming into play!

---

> 🔙 **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
