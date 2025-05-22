# Introduction to JavaScript Variables and Data Types

> 📂 See the actual working code examples here: [02-VariablesAndDataTypes](https://github.com/rohithvarma73/JavaScript-Fundamentals-From-Basics-to-Brilliance/tree/997d572ea7886b1c74cf43c4babcc2de9b993201/02-variables-and-data-types)

> 📄 Also check: [Variables.md](./01-variables/variables.md) | [DataTypes.md](./02-data-types/data-types.md) | [StaticallyVsDynamically.md](./StaticallyVsDynamically.md)

---

## 📚 Overview

In this beginner-friendly guide, we’ll dive deep into two of the _core pillars_ of JavaScript:

- **Variables** — How we store and manage data.
- **Data Types** — What kind of data we can work with.

Mastering these is **non-negotiable** if you want to write clean, scalable JavaScript — whether you're building your first app or contributing to open source 🚀.

---

## 🧩 Variables

Variables = **containers for data**.  
They allow us to label and reuse values across our code, keeping it dynamic and maintainable.

In JavaScript, you can declare variables using three keywords: `var`, `let`, and `const`.  
Each has different behavior depending on **scope**, **mutability**, and **hoisting**.

---

### Declaring Variables

#### `var`

✅ _Old-school_ way to declare variables (pre-ES6).  
⚠️ But... it has **function scope** (not block scope) — leading to bugs if you’re not careful.

```javascript
// Declares a variable 'age' and assigns value 25
var age = 25;
```

---

#### `let`

✅ Introduced in ES6 (2015).  
✅ Has **block scope** — safer and preferred when the value needs to change.

```javascript
// Declares a mutable variable 'name'
let name = "John Doe";

name = "Jane Smith"; // ✔️ Allowed: reassigning using 'let'
```

---

#### `const`

✅ Also ES6.  
✅ Declares **constants** — values that **cannot** be reassigned.

```javascript
// Declare a constant 'PI' and assign a numeric value
const PI = 3.14159;

PI = 3.14; // ❌ Error: Assignment to constant variable
```

> ℹ️ **Note**: `const` only protects the _variable binding_, not the _contents_ of an object or array it points to.

---

### 📛 Variable Naming Rules

> Think of your variable names like _nicknames for your data_.  
> JavaScript has some house rules:

- Must start with a **letter**, **underscore** `_`, or **dollar sign** `$`.
- Can contain **letters**, **numbers**, `_`, and `$` after the first character.
- **Case sensitive** (`userName` ≠ `username`).
- ❌ Cannot be a **reserved keyword** (`let`, `class`, `return`, etc.)
- ✅ **Use meaningful names** — future you (and your team) will thank you!

```javascript
let userName = "Alice";      // ✔️ Valid
let user_name = "Bob";       // ✔️ Valid
let 1stName = "Charlie";     // ❌ Invalid: can't start with a number
let let = "David";           // ❌ Invalid: 'let' is a reserved word
```

---

### ✍️ Assigning and Updating Values

You **assign** a value with `=`, and **update** simply by reassigning.

```javascript
let score = 100; // Initial assignment

score = 120; // Updated score
```

---

## 🧠 Data Types

JavaScript is **dynamically typed** — meaning variables can hold _any type_ of value, and their type can change at runtime.

Data types fall into two big buckets:

| Type              | Examples                                                 |
| ----------------- | -------------------------------------------------------- |
| **Primitive**     | String, Number, Boolean, Null, Undefined, Symbol, BigInt |
| **Non-Primitive** | Object, Array, Function                                  |

---

### 🧱 Primitive Data Types

**Primitives** are **immutable** (they can’t be changed) and **passed by value** (copies are made).

---

#### String

Represents **text**.  
Can use `'single'`, `"double"`, or `` `backticks` `` (template literals).

```javascript
// Create a simple string
const greeting = "Hello, world!";

// Create a multi-line string using backticks
const multilineString = `This
is a
multiline string`;
```

---

#### Number

Represents **both integers and floating-point numbers**.

```javascript
const age = 25; // Integer value
const temperature = 20.5; // Floating-point value
```

---

#### Boolean

Represents **true** or **false** — used heavily in conditions.

```javascript
const isLoggedIn = true; // User login status
const hasPermission = false; // User permission status
```

---

#### Null

Represents an **intentional absence** of any value.

```javascript
let user = null; // Explicitly no user object yet
```

---

#### Undefined

When a variable is **declared but not initialized**, JavaScript auto-assigns `undefined`.

```javascript
let score;
console.log(score); // Output: undefined
```

---

### 🧩 Non-Primitive Data Types

**Non-primitives** are **mutable** and **passed by reference** (copies the memory address, not the value).

---

#### Object

Key-value pairs, like a real-world dictionary.

```javascript
// Create an object to represent a person
const person = {
  name: "John Doe",
  age: 30,
  isStudent: false,
  hobbies: ["reading", "coding", "painting"],
};
```

---

#### Array

Ordered collection of elements (can mix types).

```javascript
// List of numbers
const numbers = [1, 2, 3, 4, 5];

// Mixed array with different data types
const mixedArray = [true, "hello", 42, null, { key: "value" }];
```

---

#### Function

Functions are **first-class objects** — you can assign them to variables, pass them around, return them from other functions.

```javascript
// Define a function to greet a user
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet("Alice"); // Output: Hello, Alice!
```

---

## 🏁 Conclusion

Getting confident with **variables** and **data types** sets you up for:

- Writing **reusable**, **maintainable** JavaScript
- Avoiding bugs around **mutability**, **type coercion**, and **scope leaks**
- Building **scalable** projects and contributing to **real-world OSS**

Always:

- Use `let` and `const` — avoid `var`.
- Choose clear, descriptive variable names.
- Be mindful of how JavaScript treats types (dynamic typing = powerful + dangerous).

---

## 📖 Additional Resources

- [MDN Web Docs: JavaScript Data Types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
- [MDN Web Docs: JavaScript Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Variables)

---

> 📂 **To dive deeper and play with the code examples, visit:** [02-VariablesAndDataTypes GitHub](https://github.com/rohithvarma73/JavaScript-Fundamentals-From-Basics-to-Brilliance/tree/997d572ea7886b1c74cf43c4babcc2de9b993201/02-variables-and-data-types)

---

> 🔙 **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
