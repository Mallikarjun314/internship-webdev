# Javascript Variables



### 1. **What is a Variable?**

* A variable is a container for storing data values.

```javascript
let name = "Alice";
```

---

### 2. **`var`, `let`, and `const`**

* **`var`**: Function-scoped (older, avoid in modern JS)
* **`let`**: Block-scoped, re-assignable
* **`const`**: Block-scoped, cannot be re-assigned

```javascript
var x = 5;
let y = 10;
const z = 15;
```

---

### 3. **Variable Naming Rules**

* Can include letters, digits, `$`, `_`
* Must begin with letter, `$`, or `_`
* Case-sensitive, cannot be reserved keywords

```javascript
let $price = 100;
let _name = "John";
let userAge = 30;
```

---

### 4. **Hoisting**

* `var` is hoisted and initialized as `undefined`.
* `let` and `const` are hoisted but **not initialized** (temporal dead zone).

```javascript
console.log(a); // undefined
var a = 10;

console.log(b); // ReferenceError
let b = 20;
```

---

### 5. **Global vs Local Scope**

* Variables declared outside functions are global. Inside a block or function, they are local.

```javascript
let globalVar = "I'm global";

function test() {
  let localVar = "I'm local";
  console.log(localVar);
}
```

---

### 6. **Block Scope (`let` and `const`)**

* Restricted to the block `{}` where defined.

```javascript
{
  let a = 1;
  const b = 2;
  console.log(a, b); // 1 2
}
// console.log(a); // ReferenceError
```

---

### 7. **Function Scope (`var`)**

* Accessible anywhere inside the function.

```javascript
function demo() {
  var msg = "Hello";
  console.log(msg);
}
```

---

### 8. **Re-declaration and Re-assignment**

```javascript
var a = 1;
var a = 2; // allowed

let b = 3;
// let b = 4; // Error: redeclaration not allowed

const c = 5;
// c = 6; // Error: reassignment not allowed
```

---

### 9. **Constants and Mutability**

* `const` variables can’t be reassigned, but if it’s an object/array, contents **can** change.

```javascript
const arr = [1, 2, 3];
arr.push(4); // allowed
console.log(arr); // [1, 2, 3, 4]
```

---

### 10. **Best Practices**

* Always use `let` and `const` over `var`
* Use `const` by default; use `let` only if you need to reassign

```javascript
const MAX_LIMIT = 100;
let count = 0;
```

---

### 11. **Dynamic Typing**

* Variables can hold any type and change types during execution.

```javascript
let data = 10;
data = "Now a string";
```

---

### 12. **Destructuring Variables**

* Extract values from arrays or objects into variables.

```javascript
const [x, y] = [1, 2];
const { name, age } = { name: "Bob", age: 25 };
```

---

### 13. **Global Variables in Browser (`window`)**

* Variables declared with `var` in global scope become properties of `window`.

```javascript
var a = 10;
console.log(window.a); // 10
```

---

### 14. **Temporary Dead Zone (TDZ)**

* Time between hoisting and initialization of `let`/`const` is TDZ.

```javascript
// console.log(a); // ReferenceError
let a = 5;
```

---

### 15. **Immediately Initialized Constants**

* `const` must be initialized when declared.

```javascript
// const x; // Error
const x = 100;
```