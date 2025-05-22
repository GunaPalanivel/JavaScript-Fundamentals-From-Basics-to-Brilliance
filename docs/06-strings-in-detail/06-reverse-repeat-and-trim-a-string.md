# String Manipulation in JavaScript: Reverse, Repeat, and Trim

## Introduction

String manipulation is fundamental in web development. Whether you're formatting user input, generating dynamic content, or processing data, these operations are essential. Let's explore three powerful string operations: reversing, repeating, and trimming.

## Reverse a String

While JavaScript doesn't have a built-in string reverse method, we can easily implement it using array operations:

```javascript
/**
 * Reverses a string by converting it to an array of characters,
 * reversing the array, and joining it back into a string.
 * Time Complexity: O(n) - Linear time (each operation touches each character once)
 * @param {string} str - Input string to reverse
 * @returns {string} Reversed string
 */
function reverseString(str) {
  // Split into array, reverse, and join
  return str.split("").reverse().join("");
}

const example = "hello";
console.log(reverseString(example)); // Output: "olleh"
```

### Why This Works:

1. `split('')` converts the string to an array of characters
2. `reverse()` reverses the array in place
3. `join('')` combines the array back into a string

## Repeat a String

The `repeat()` method creates a new string by concatenating the original string a specified number of times:

```javascript
/**
 * Repeats a string multiple times
 * Useful for generating patterns or placeholder content
 * @param {string} text - String to repeat
 * @param {number} count - Number of repetitions
 * @returns {string} Repeated string
 */
function repeatText(text, count) {
  if (count < 0) throw new Error("Count must be non-negative");
  return text.repeat(count);
}

console.log(repeatText("na", 3) + " Batman!"); // Output: "nanana Batman!"
```

### Performance Note:

- `repeat()` is highly optimized in modern JavaScript engines
- Avoid extremely large counts (millions+) as it consumes memory

## Trim a String

The `trim()` method removes whitespace from both ends of a string, which is crucial for cleaning user input:

```javascript
/**
 * Cleans user input by removing leading/trailing whitespace
 * Important for form validation and data processing
 * @param {string} input - User input string
 * @returns {string} Trimmed string
 */
function cleanInput(input) {
  return input.trim();
}

const userInput = "   user@example.com   ";
console.log(`Original: "${userInput}"`); // "   user@example.com   "
console.log(`Trimmed: "${cleanInput(userInput)}"`); // "user@example.com"
```

### Related Methods:

- `trimStart()` - Removes leading whitespace only
- `trimEnd()` - Removes trailing whitespace only

## Real-World Applications

1. **Form Processing**:

   ```javascript
   // Before saving user registration data
   function processRegistration(email, username) {
     return {
       email: email.trim().toLowerCase(),
       username: username.trim(),
     };
   }
   ```

2. **Text Formatting**:

   ```javascript
   // Generate a visual separator
   function createSeparator(length) {
     return "-".repeat(length);
   }
   ```

3. **Palindrome Checking**:
   ```javascript
   // Check if a string is a palindrome
   function isPalindrome(str) {
     const cleaned = str.toLowerCase().replace(/[^a-z0-9]/g, "");
     return cleaned === reverseString(cleaned);
   }
   ```

## Performance Considerations

1. **Reversing Large Strings**:

   - For very large strings (MBs+), consider streaming or chunked processing
   - The basic method shown works well for most web applications

2. **Memory Efficiency**:
   - `repeat()` creates new strings in memory
   - For frequent operations, consider alternative approaches

## Best Practices

1. **Input Validation**:

   ```javascript
   function safeRepeat(str, times) {
     if (typeof str !== "string") throw new TypeError("Input must be a string");
     if (times < 0) throw new RangeError("Times must be non-negative");
     return str.repeat(times);
   }
   ```

2. **Internationalization**:
   - Be aware that some Unicode characters (like emojis or combining marks) may not reverse cleanly
   - For complex text, consider using a library like `lodash`

## 💡 Bonus Tips

- **Combine ops**: You can chain methods to sanitize and manipulate input in one go:

```javascript
const rawInput = "   guna   ";
const cleanAndReversed = rawInput.trim().split("").reverse().join("");

console.log(cleanAndReversed); // "anug"
```

- **Performance tip**: For large strings, `.split('').reverse().join('')` is fine, but if you're reversing in a loop or at scale (like text processing tools), consider more optimized approaches using loops or buffers.

- **Edge Cases to Handle**:

  - Empty strings (`""`)
  - Unicode characters (especially emojis, combining characters)
  - Input validation (ensure it's a string before applying these methods)
    > Next up: 🔍 [**Strings Exercise**](./07-strings-exercise.md) — coming into play!

---

> **Back to Home:** [JavaScript Fundamentals: From Basics to Brilliance](../index.md)
