# Javascript Datatypes

### 1. **Primitive Data Types**

* The simplest types in JavaScript. Immutable and stored by value.

---

#### 1.1 **String**

* Represents textual data.

```javascript
let name = "Alice";
console.log(typeof name); // string
```

---

#### 1.2 **Number**

* Represents both integers and floating-point numbers.

```javascript
let age = 30;
let price = 19.99;
console.log(typeof price); // number
```

---

#### 1.3 **Boolean**

* Represents `true` or `false`.

```javascript
let isOnline = true;
console.log(typeof isOnline); // boolean
```

---

#### 1.4 **Undefined**

* A variable that has been declared but not assigned a value.

```javascript
let user;
console.log(typeof user); // undefined
```

---

#### 1.5 **Null**

* Represents the intentional absence of any value.

```javascript
let selected = null;
console.log(typeof selected); // object (this is a known quirk)
```

---

#### 1.6 **Symbol** *(ES6)*

* Unique and immutable identifier, often used for object property keys.

```javascript
const sym = Symbol("id");
console.log(typeof sym); // symbol
```

---

#### 1.7 **BigInt** *(ES2020)*

* Represents large integers beyond the `Number.MAX_SAFE_INTEGER`.

```javascript
const big = 1234567890123456789012345678901234567890n;
console.log(typeof big); // bigint
```

---

### 2. **Reference (Non-Primitive) Data Types**

* Complex types stored by reference.

---

#### 2.1 **Object**

* Key-value pairs, used to store collections of data.

```javascript
let person = { name: "Bob", age: 25 };
console.log(typeof person); // object
```

---

#### 2.2 **Array**

* Ordered collection of items.

```javascript
let colors = ["red", "green", "blue"];
console.log(typeof colors); // object
console.log(Array.isArray(colors)); // true
```

---

#### 2.3 **Function**

* A callable object. Technically an object with `typeof` returning `'function'`.

```javascript
function greet() {
  return "Hello!";
}
console.log(typeof greet); // function
```

---

#### 2.4 **Date**

* Built-in object for handling dates and times.

```javascript
let today = new Date();
console.log(today.toDateString());
```

---

#### 2.5 **RegExp (Regular Expression)**

* Used for pattern matching in strings.

```javascript
let pattern = /abc/;
console.log(pattern.test("abcdef")); // true
```

---

### 3. **Type Conversion**

* Convert between types explicitly or implicitly.

---

#### 3.1 **String Conversion**

```javascript
let num = 123;
console.log(String(num)); // "123"
```

#### 3.2 **Number Conversion**

```javascript
let str = "42";
console.log(Number(str)); // 42
```

#### 3.3 **Boolean Conversion**

```javascript
console.log(Boolean(0));     // false
console.log(Boolean("Hi"));  // true
```

---

### 4. **Type Coercion**

* JavaScript automatically converts types when needed.

```javascript
console.log("5" + 1); // "51" (string)
console.log("5" - 1); // 4   (number)
```

---

### 5. **`typeof` Operator**

* Returns a string indicating the type of the operand.

```javascript
console.log(typeof null); // "object" (bug in JS)
console.log(typeof []);   // "object"
console.log(typeof NaN);  // "number"
```

---

### 6. **`instanceof` Operator**

* Checks whether an object is an instance of a specific class.

```javascript
console.log([] instanceof Array); // true
console.log({} instanceof Object); // true
```

---

### 7. **`Array.isArray()`**

* Reliable way to check if a value is an array.

```javascript
let val = [1, 2, 3];
console.log(Array.isArray(val)); // true
```

---

### 8. **`NaN` (Not a Number)**

* Represents an invalid number.

```javascript
let result = "abc" * 3;
console.log(isNaN(result)); // true
```

---

### 9. **`null` vs `undefined`**

* `undefined`: variable declared but not assigned.
* `null`: explicitly assigned "no value".

```javascript
let a;
let b = null;
console.log(typeof a); // undefined
console.log(typeof b); // object
```

---

### 10. **Dynamic Typing**

* JavaScript variables can hold any type at any time.

```javascript
let data = 42;
data = "Now I’m a string";
```