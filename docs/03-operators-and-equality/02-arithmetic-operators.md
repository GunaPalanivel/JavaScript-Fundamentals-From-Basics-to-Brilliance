# **🧪 Arithmetic Operators in Action**

```js
// Addition (+): Adds two numbers
const sum = 10 + 5;
console.log("Addition: 10 + 5 =", sum); // Output: 15

// Subtraction (-): Subtracts right operand from left
const difference = 20 - 7;
console.log("Subtraction: 20 - 7 =", difference); // Output: 13

// Multiplication (*): Multiplies two numbers
const product = 6 * 4;
console.log("Multiplication: 6 * 4 =", product); // Output: 24

// Division (/): Divides left operand by right
const quotient = 15 / 3;
console.log("Division: 15 / 3 =", quotient); // Output: 5

// Modulus (%): Gives remainder of division
const remainder = 17 % 5;
console.log("Modulus: 17 % 5 =", remainder); // Output: 2

// Exponentiation (**): Raises first operand to the power of second
const power = 3 ** 3;
console.log("Exponentiation: 3 ** 3 =", power); // Output: 27

// Increment (++): Increases value by 1
let incrementValue = 5;
incrementValue++; // Same as: incrementValue = incrementValue + 1
console.log("Increment: 5++ =", incrementValue); // Output: 6

// Decrement (--): Decreases value by 1
let decrementValue = 8;
decrementValue--; // Same as: decrementValue = decrementValue - 1
console.log("Decrement: 8-- =", decrementValue); // Output: 7
```

---

## 💡 Tips for Using Arithmetic Operators

- Use `++` and `--` carefully—especially **pre vs post** increment in loops or conditions (`++i` vs `i++`).
- Modulus `%` is great for checking **even/odd** numbers: `x % 2 === 0` means even.
- Exponentiation `**` is available from ES2016+. Use `Math.pow()` if you need backward compatibility.

---

> **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
