# Javascript Loops

## for loop:

- Used when the number of iterations is known beforehand. 
- Consists of three parts: initialization, condition, and increment/decrement. 

Example: 

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
## while loop

- Repeats a block of code as long as a specified condition is true. 
- Useful when the number of iterations is not known in advance. 

Example: 

```js
let i = 0;

while (i < 5) {
  console.log(i);
  i++;
}
```

## do . . . while loop: 

- Similar to while, but the code block is executed at least once, regardless of the condition. 
- The condition is checked after the code block executes. 

Example: 
```js
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 5);
```
## for...in loop: 

- Iterates over the enumerable properties of an object, Returns the property names (keys) as strings

Example:
```js
const person = { name: 'Alice', age: 30 };

for (let key in person) {

  console.log(key, person[key]);

}
```
## for . . . of loop: 

- Iterates over the values of iterable objects, such as arrays, strings, maps, and sets. 

Example: 

```js
const colors = ['red', 'green', 'blue'];

for (let color of colors) {

  console.log(color);

}
```

## forEach loop: 

- Array method that executes a provided function once for each array element. 

Example: 
```js
const numbers = [1, 2, 3];

numbers.forEach(function(number) {

  console.log(number);

});
```