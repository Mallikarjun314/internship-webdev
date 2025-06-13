# Javascript Conditionals


### 1. **`if` Statement**

* Executes a block of code if a specified condition is true.

```javascript
let age = 18;
if (age >= 18) {
  console.log("You are an adult.");
}
```

---

### 2. **`if...else` Statement**

* Executes one block of code if condition is true, another if false.

```javascript
let age = 16;
if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}
```

---

### 3. **`else if` Statement**

* Tests multiple conditions in sequence.

```javascript
let score = 85;
if (score >= 90) {
  console.log("A");
} else if (score >= 80) {
  console.log("B");
} else {
  console.log("C or below");
}
```

---

### 4. **Ternary Operator (`? :`)**

* A shorthand for `if...else`.

```javascript
let age = 20;
let status = age >= 18 ? "Adult" : "Minor";
console.log(status); // Adult
```

---

### 5. **`switch` Statement**

* Selects one of many blocks of code to execute based on a variable’s value.

```javascript
let color = "blue";
switch (color) {
  case "red":
    console.log("Stop!");
    break;
  case "blue":
    console.log("Cool!");
    break;
  default:
    console.log("Unknown color");
}
```

---

### 6. **Logical Operators in Conditions**

* Use `&&` (AND), `||` (OR), and `!` (NOT) to combine or modify conditions.

```javascript
let temp = 25;
if (temp > 20 && temp < 30) {
  console.log("Comfortable weather");
}

let raining = false;
if (!raining) {
  console.log("Go outside");
}
```

---

### 7. **Truthy & Falsy Values**

* JavaScript treats some values as `false` in conditionals: `false`, `0`, `""`, `null`, `undefined`, `NaN`. All others are truthy.

```javascript
if ("") {
  console.log("Won't run");
}

if ("Hello") {
  console.log("Will run"); // because "Hello" is truthy
}
```

---

### 8. **Nullish Coalescing (`??`)**

* Returns right-hand value if left-hand is `null` or `undefined`.

```javascript
let name = null;
let displayName = name ?? "Guest";
console.log(displayName); // Guest
```

---

### 9. **Optional Chaining with Conditionals (`?.`)**

* Prevents errors when accessing nested properties.

```javascript
let user = {};
if (user.profile?.name) {
  console.log(user.profile.name);
} else {
  console.log("No name available");
}
```

---

### 10. **Using `Boolean()` and Double Negation `!!`**

* Convert values explicitly to boolean for clarity in conditions.

```javascript
let value = "Hello";
if (Boolean(value)) {
  console.log("Truthy");
}

console.log(!!value); // true
```

---

### 11. **Short-circuit Evaluation**

* Executes expressions conditionally using `&&` or `||`.

```javascript
let isLoggedIn = true;
isLoggedIn && console.log("Welcome!"); // runs if true

let userName = null;
console.log(userName || "Guest"); // Guest
```

---

### 12. **Chained Ternary Operators** *(Use with caution)*

* Nested ternary expressions for multiple conditions.

```javascript
let score = 75;
let grade = score > 90 ? "A" : score > 80 ? "B" : "C";
console.log(grade); // C
```