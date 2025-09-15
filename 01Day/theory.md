## 🧠 1. Variables in JavaScript

Variables store data values and can be declared using `var`, `let`, or `const`. Understanding their differences is crucial for writing clean and bug-free code.

### 🟦 `var` (Function-scoped)

*   **Scope**: Function-level; accessible throughout the entire function where declared.
*   **Hoisting**: Declarations are hoisted to the top, but initializations are not.
*   **Re-declaration**: Allowed within the same scope.

```javascript
function example() {
  console.log(x); // undefined
  var x = 5;
  console.log(x); // 5
}
```

### 🟨 `let` (Block-scoped)

*   **Scope**: Block-level; confined to the block (e.g., loops, conditionals) where declared.
*   **Hoisting**: Hoisted but not initialized, leading to a "temporal dead zone" until declaration.
*   **Re-declaration**: Not allowed within the same scope.

```javascript
function example() {
  if (true) {
    let y = 10;
    console.log(y); // 10
  }
  // console.log(y); // ReferenceError: y is not defined
}
```

### 🟩 `const` (Block-scoped, Constant)

*   **Scope**: Block-level.
*   **Hoisting**: Similar to `let`; hoisted but not initialized.
*   **Re-declaration**: Not allowed.
*   **Re-assignment**: Not allowed; the variable must be initialized at the time of declaration.

```javascript
const z = 15;
// z = 20; // TypeError: Assignment to constant variable.
```

---

## 🧩 2. Functions in JavaScript

Functions are blocks of code designed to perform a particular task. They can be declared in various ways:

#### Function Declaration
```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```

#### Function Expression (Anonymous Function)
```javascript
const greet = function(name) {
  return `Hello, ${name}!`;
};
```

#### Arrow Function (ES6+)
```javascript
const greet = (name) => `Hello, ${name}!`;
```

Arrow functions offer a concise syntax and lexically bind the `this` value, making them particularly useful in certain contexts like callbacks.

---

## 🌐 3. Scoping in JavaScript

Scope determines the accessibility of variables and functions in different parts of the code.

### Global Scope

Variables declared outside any function or block are in the global scope and can be accessed anywhere in the code.

```javascript
var globalVar = 'I am global';

function checkScope() {
  console.log(globalVar); // 'I am global'
}
```

### Function Scope

Variables declared within a function are only accessible inside that function.

```javascript
function localScope() {
  var localVar = 'I am local';
  console.log(localVar); // 'I am local'
}
// console.log(localVar); // ReferenceError: localVar is not defined
```

### Block Scope (ES6+)

Introduced with `let` and `const`, block scope confines variables to the block, statement, or expression where they are declared.

```javascript
if (true) {
  let blockVar = 'I am block-scoped';
  console.log(blockVar); // 'I am block-scoped'
}
// console.log(blockVar); // ReferenceError: blockVar is not defined
```

---

## 🚀 4. ES6+ Features

ECMAScript 2015 (ES6) introduced several new features to JavaScript, enhancing its capabilities and syntax.

### 🧵 Template Literals
Allow for embedded expressions and multi-line strings.
```javascript
const name = 'Alice';
const greeting = `Hello, ${name}!`;
```

### 🧭 Destructuring Assignment
Provides a way to unpack values from arrays or properties from objects into distinct variables.
```javascript
const person = { name: 'Bob', age: 30 };
const { name, age } = person;
```

### 📦 Modules
Enable the use of `import` and `export` to modularize code.
```javascript
// In module.js
export const pi = 3.14159;

// In main.js
import { pi } from './module.js';
```

### 🧮 Default Parameters
Allow functions to have default values for parameters.
```javascript
function multiply(a, b = 1) {
  return a * b;
}
```

### 🧩 Rest and Spread Operators
*   **Rest**: Collects multiple elements into an array.
```javascript
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
```

*   **Spread**: Expands an array or object into individual elements or properties.
```javascript
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5];
```

---

## 📝 Summary

*   **`var`**: Function-scoped, hoisted, allows re-declaration.
*   **`let`**: Block-scoped, hoisted, does not allow re-declaration.
*   **`const`**: Block-scoped, hoisted, does not allow re-declaration or re-assignment.
*   **Functions**: Can be declared in various ways; arrow functions have a concise syntax and lexically bind `this`.
*   **Scoping**: Determines variable accessibility; global, function, and block scopes are key concepts.
*   **ES6+ Features**: Introduced template literals, destructuring, modules, default parameters, and rest/spread operators, enhancing JavaScript's functionality and readability.