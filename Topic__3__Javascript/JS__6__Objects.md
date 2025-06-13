# Javascript Objects

### 1. **Object Literal**

* The most common way to create an object using curly braces.

```javascript
const person = {
  name: "Alice",
  age: 25
};
console.log(person.name); // Alice
```

---

### 2. **Accessing Properties**

* You can use dot `.` or bracket `[]` notation to access properties.

```javascript
console.log(person.age);      // 25
console.log(person["name"]); // Alice
```

---

### 3. **Adding & Modifying Properties**

* Assign new values or create new properties.

```javascript
person.job = "Developer";
person.age = 26;
console.log(person); 
```

---

### 4. **Deleting Properties**

* Use the `delete` keyword to remove properties.

```javascript
delete person.job;
console.log(person);
```

---

### 5. **Nested Objects**

* Objects can contain other objects.

```javascript
const user = {
  name: "Bob",
  address: {
    city: "New York",
    zip: 10001
  }
};
console.log(user.address.city); // New York
```

---

### 6. **Methods in Objects**

* Functions stored as object properties.

```javascript
const car = {
  brand: "Toyota",
  start() {
    console.log("Car started");
  }
};
car.start(); // Car started
```

---

### 7. **`this` Keyword**

* Refers to the object the method belongs to.

```javascript
const dog = {
  name: "Buddy",
  bark() {
    console.log(`${this.name} says woof`);
  }
};
dog.bark(); // Buddy says woof
```

---

### 8. **Constructor Function**

* Template for creating multiple objects with the same structure.

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const p1 = new Person("Eve", 30);
console.log(p1.name); // Eve
```

---

### 9. **Classes (ES6)**

* Modern syntax for constructor functions and inheritance.

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a noise`);
  }
}
const cat = new Animal("Whiskers");
cat.speak(); // Whiskers makes a noise
```

---

### 10. **Prototypes & Inheritance**

* Allows objects to inherit properties/methods from other objects.

```javascript
function Animal(name) {
  this.name = name;
}
Animal.prototype.speak = function() {
  console.log(`${this.name} speaks`);
};
const dog = new Animal("Rex");
dog.speak(); // Rex speaks
```

---

### 11. **Object.create()**

* Creates a new object using an existing object as the prototype.

```javascript
const parent = {
  greet() {
    console.log("Hello!");
  }
};
const child = Object.create(parent);
child.greet(); // Hello!
```

---

### 12. **Object Destructuring**

* Extracts properties into variables.

```javascript
const user = { name: "Sam", age: 22 };
const { name, age } = user;
console.log(name, age); // Sam 22
```

---

### 13. **Computed Property Names**

* Allows dynamic property names in object literals.

```javascript
const key = "score";
const obj = {
  [key]: 100
};
console.log(obj.score); // 100
```

---

### 14. **Object.entries(), Object.keys(), Object.values()**

* Useful methods to iterate over object properties.

```javascript
const obj = { a: 1, b: 2 };
console.log(Object.keys(obj));   // ['a', 'b']
console.log(Object.values(obj)); // [1, 2]
console.log(Object.entries(obj)); // [['a', 1], ['b', 2]]
```

---

### 15. **Object.assign()**

* Copies properties from one or more objects into a target object.

```javascript
const a = { x: 1 };
const b = { y: 2 };
const merged = Object.assign({}, a, b);
console.log(merged); // { x: 1, y: 2 }
```

---

### 16. **Spread Operator (`...`)**

* An easier alternative to merge or clone objects.

```javascript
const obj1 = { foo: "bar" };
const obj2 = { ...obj1, baz: 42 };
console.log(obj2); // { foo: "bar", baz: 42 }
```

---

### 17. **Optional Chaining (`?.`)**

* Safely access deeply nested properties.

```javascript
const user = {};
console.log(user.address?.city); // undefined (no error)
```

---

### 18. **Object Freezing & Sealing**

* `Object.freeze()` prevents all changes.
* `Object.seal()` allows changing existing properties, but not adding/removing.

```javascript
const obj = { a: 1 };
Object.freeze(obj);
obj.a = 2; // No effect
console.log(obj.a); // 1
```

---

### 19. **JSON.stringify() & JSON.parse()**

* Convert object to/from JSON format.

```javascript
const person = { name: "Alice", age: 30 };
const str = JSON.stringify(person);
const parsed = JSON.parse(str);
console.log(parsed.name); // Alice
```

---

### 20. **Private Properties (ES2022 `#`)**

* Encapsulate object fields using `#`.

```javascript
class Secret {
  #hidden = "classified";
  reveal() {
    return this.#hidden;
  }
}
const s = new Secret();
console.log(s.reveal()); // classified
```
