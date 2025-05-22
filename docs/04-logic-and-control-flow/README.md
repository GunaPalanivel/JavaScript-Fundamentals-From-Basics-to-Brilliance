# 🧠 Understanding Conditional Logic in JavaScript

Conditional statements are the backbone of decision-making in programming. In JavaScript, mastering control flow with tools like `if`, `else if`, `switch`, and the ternary operator allows developers to build logic-driven applications that respond intelligently to user inputs, states, and data.

---

### 📌 What You’ll Learn:

- ['if' Statement](./01-if-statement.md)
- [Truthy/Falsy Values](./02-truthy-and-falsy-values.md)
- [Logical Operators `(&&, ||)`](./03-logical-operators-AND-OR.md)
- [Logical Operators `(!NOT)`](./04-logical-operators-!NOT.md)
- ['switch' Statement](./05-switch-statement.md)
- [Ternary Operator](./06-ternary-operator.md)
- ['for' and 'while' Loops](./07-for-and-while-loops.md)

---

## ✅ `if`, `else if`, `else`: Core Conditional Logic

### 🔍 Concept

An `if` statement evaluates a condition. If it's true, a block of code runs. If false, that block is skipped.

### 🛠️ Setup & Syntax

```javascript
const age = 20;

if (age >= 18) {
  // ✅ Condition is true
  console.log("Access granted to the club.");
} else {
  // ❌ Condition is false
  console.log("Access denied. You must be 18 or older.");
}
```

- Code blocks are enclosed in `{}`.
- `else if` adds additional conditions.
- `else` handles any remaining cases (no condition needed).

### ⚠️ Important Note

Only the **first true** condition is executed. All others are skipped. Always order conditions from most specific to most general.

---

## 🔁 Truthy and Falsy in JavaScript

Understanding **truthy** and **falsy** values is essential. JavaScript uses coercion to determine the truthiness of non-boolean types in conditions.

### ❗ Six Falsy Values:

```js
false, 0, "", null, undefined, NaN;
```

Everything else is **truthy**, including:

```js
[], {}, "hello", 42;
```

### ✅ Best Practice

```javascript
const userInput = "";

if (userInput) {
  console.log("User entered something.");
} else {
  console.log("Input is empty or invalid.");
}
```

> `if (value)` is cleaner than `if (value !== "")`, and works across multiple types.

### 🔍 Boolean Conversion

```javascript
!!"hello"; // true
!!0; // false
Boolean([]); // true
Boolean(null); // false
```

---

## 🔗 Logical Operators: `&&`, `||`, `!`

Logical operators help combine or invert conditions. Understanding how they work with truthy/falsy values helps avoid bugs and write cleaner logic.

### `&&` (AND)

- Returns **first falsy** value or **last truthy** value.
- Short-circuits on falsy.

```javascript
const isLoggedIn = true;
const hasPremium = false;

// Only show premium content if both are true
if (isLoggedIn && hasPremium) {
  console.log("Showing premium features.");
}
```

### `||` (OR)

- Returns **first truthy** value or **last falsy** value.
- Short-circuits on truthy.

```javascript
const theme = userPreference || "light";
// If `userPreference` is falsy, fallback to "light"
```

### `!` (NOT)

- Inverts a value's truthiness.

```javascript
!false; // true
!!"hi"; // true (double negation to get boolean)
```

---

## 🧱 `switch` Statements

`switch` is useful when checking a single value against many known possibilities — it's often cleaner than multiple `else if` blocks.

### 🛠️ Syntax

```javascript
const superhero = "Iron Man";

switch (superhero) {
  case "Batman":
    console.log("Gadget expert.");
    break;
  case "Iron Man":
    console.log("Tech genius billionaire.");
    break;
  default:
    console.log("Unknown hero.");
}
```

### 🧠 Tips

- Always use `break` to avoid **fall-through**.
- `default` acts like `else`.

---

## 🧪 Ternary Operator: `? :`

The ternary operator is a concise one-liner for simple `if-else` logic.

### 🛠️ Syntax

```javascript
const canDrive = age >= 18 ? "You can drive." : "You cannot drive.";
console.log(canDrive);
```

- Useful for UI rendering, quick conditionals, or inline assignments.

### ⚠️ Don’t Overuse

Avoid nested ternaries — they’re hard to read. If logic gets complex, use `if-else` blocks instead.

---

## 🔁 Loops in JavaScript: `for` and `while`

When you need to repeat tasks — like iterating through arrays, repeating operations, or polling — JavaScript provides loop constructs.

### 🔄 For Loop

```javascript
// Prints numbers 0 to 9
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

- Initialization: `let i = 0`
- Condition: `i < 10`
- Final expression: `i++`

### 🔄 While Loop

```javascript
let i = 0;

while (i < 10) {
  console.log(i);
  i++; // Don’t forget to update, or you’ll get an infinite loop
}
```

- Best used when the number of iterations isn’t known in advance.

---

## 🧠 Real-World Tips

- 🔍 Use `Boolean()` or `!!` to explicitly convert types in conditions.
- 🧼 Clean conditionals make debugging easier and prevent logic errors.
- 📦 Keep `switch` statements and ternary expressions readable — prioritize clarity over cleverness.
- 🐛 Always test edge cases (empty string, `null`, `undefined`) in your logic.

---

## 📚 Resources

- [MDN Web Docs – if...else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)
- [JavaScript Truthy/Falsy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)
- [JavaScript Logical Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#logical_operators)
- [JavaScript Loops Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)

---

> 🔙 **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
