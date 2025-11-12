# Workshop – JavaScript Core & Practice (Updated)

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-green.svg)]()
[![Practice](https://img.shields.io/badge/Type-Hands--on%20Practice-blue.svg)]()

---

## Introduction

Welcome to the **JavaScript Core Workshop**! Here you’ll learn the magic behind JS through fun little coding quests. Each mission helps you unlock new skills so you can soon build your own front-end projects with **HTML, CSS, and JavaScript** (´▽`ʃ♡ƪ)

You can test everything directly in your browser console or playgrounds like [JSFiddle](https://jsfiddle.net/) or [CodePen](https://codepen.io/).

**Goal:** Learn the basics of JS through interactive challenges — think of it as a little adventure game to prepare you for your first Express or web projects.

---

## Resources (｡•̀ᴗ-)✧

* [MDN JavaScript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [JavaScript.info Guide](https://javascript.info/)
* Practice environments: [JSFiddle](https://jsfiddle.net/) / [CodePen](https://codepen.io/)

---

## Exercise 1: Variables & Types (⌒‿⌒)

### Objective
Understand how JavaScript handles variable declarations, scope, and type conversions.

### Tasks

For now you will work with js script and execute them using node.

If possible, keep track of everything you do properly. It can be useful if you want to verify something to your teacher.

**1.1 Create Variables**
```js
let name = "Alex";
const age = 22;
var city = "Paris";
```
Explain the difference between `var`, `let`, and `const`. Which one should you prefer in modern JS?

---

**1.2 Type Checking**
```js
let a = 42;
let b = "42";
let c = true;
let d = null;
let e;
let f = [1, 2, 3];
let g = { name: "test" };
```
Log their types in the console using `typeof`.

→ Try to find: what’s the difference between `==` and `===`?

---

**1.3 Type Coercion**
```js
console.log("5" + 3);
console.log("5" - 3);
console.log(true + 1);
console.log(false + "hello");
```
Guess before you run it. JS can be surprising (°ロ°) !

---

**1.4 Truthy & Falsy**
Create an array of mixed values and filter only the truthy ones:
```js
const values = [0, "hello", "", null, undefined, NaN, [], {}, "0", false];
```
Hint: use `Boolean(value)` or `!!value`.

---

## Exercise 2: Functions & Scope (•‿•)

### Objective
Learn how to write and use functions effectively.

### Tasks

**2.1 Function Declarations vs Expressions**
Create three versions of a function that multiplies two numbers:
1. Classic function declaration
2. Function expression
3. Arrow function

---

**2.2 Default Parameters & Rest**
```js
function greet(name = "stranger") {
  return `Hello, ${name}!`;
}
```
Try calling it with and without arguments. What do you understand ?

---

## Exercise 3: Arrays & Methods (≧◡≦)

### Objective
Manipulate and transform data structures efficiently.

### Tasks

**3.1 Array Operations**
```js
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
```
Perform these in separate steps:
1. Filter only even numbers
2. Map each number to its square
3. Reduce to get the sum
4. Find the first number greater than 5
5. Check if all numbers are positive

---

**3.2 Product Challenge**
```js
const products = [
  { name: "Laptop", price: 1000, category: "tech" },
  { name: "Phone", price: 500, category: "tech" },
  { name: "Shirt", price: 30, category: "clothing" },
  { name: "Shoes", price: 80, category: "clothing" }
];
```
* Get all product names
* Filter products with price > 50
* Calculate total price
* Get only tech products

---

**3.3 Sorting & Reversing**
Sort the products array by price (ascending and descending).

---

## Exercise 4: Objects & Destructuring (´｡• ω •｡`)

### Objective
Understand how to work with objects and modern syntax.

### Tasks

**4.1 Object Basics**

Create an object called person with the properties name, age, and city.
Add a method introduce() that returns a string like: *Hi, I'm Alex, 22 years old from Paris.*

---

**4.2 Destructuring**

Create an object user with name, age, city, and email.
Use destructuring to extract name and email.

Then try:
Renaming **email** to **contact** during destructuring
Giving **country** a default value (for example "France")
---

**4.3 Spread & Merge**
Create two objects defaults and userPrefs.
**defaults** should have **theme** and **lang**
**userPrefs** should override **lang** and add **notifications: true**

Use the spread operator to merge them into a new object settings and log it.
---

## Exercise 5: Control Flow & Loops (｡•̀ᴗ-)✧

### Objective
Write logic using conditions and loops.

### Tasks

**5.1 FizzBuzz but in JS (classic)**
Loop from 1 to 50:
* Print "Fizz" if divisible by 3
* "Buzz" if divisible by 5
* "FizzBuzz" if both
* Else print the number

---

**5.2 Switch Statement**
Create a function `getDayName(dayNumber)` that takes a number (1-7) and returns the weekday name.
You must use a **Switch**.

---

**5.4 For...of vs For...in**
Try both on arrays and objects. What’s the difference?

---

## Exercise 6: Modern ES6+ Features (´▽`ʃ♡ƪ)

**6.1 Template Literals** – use backticks instead of + concatenation.

Try to log this :

```js
const name = "Alex";
const city = "Paris";

console.log("Hi, I'm " + name + " from " + city + ".");
```

without using any **+**

---

**6.2 Spread Operator** – combine or copy arrays.

Combine the two arrays without using any function `like concat()` or loops.

```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5];
```

---

**6.3 Rest Parameters** – handle multiple arguments in functions.

Create a function `sum(...numbers)` that accepts any number of arguments and returns their sum. *What are these mysterious dots before the variable...*

---

## Exercise 7: Asynchronous JavaScript (•̀ᴗ•́ )و ̑̑

**7.1 Timeout Promise**
Create a function `delay(ms)` returning a promise resolved after `ms` ms.

**7.2 Promise Chaining**
Chain a few delays to log messages in sequence.

**7.3 Fetch API**
Use `fetch()` to get data from `https://jsonplaceholder.typicode.com/users` and log usernames.

**7.4 Async/Await**
Rewrite the previous using `async/await` with `try/catch`.

---

## Exercise 8: DOM Manipulation

Let's go back to something familiar: HTML, but this time controlled by JavaScript.

The html file is already provided [here](./Exercise8.html).

Use it to complete the following exercises in a script.js file.
---

### Tasks

#### **8.1 Selecting Elements**

Use `document.getElementById()` and `document.querySelector()` to select:

* The button with id `myButton`
* The input with id `myInput`
  Then, `console.log()` them to confirm you selected the right elements.

---

#### **8.2 Creating Elements**

Use `document.createElement()` to create:

* A new `<p>` element
* Give it some `textContent` like "Hello from JavaScript!"
* Use `appendChild()` to add it to the `<body>`.

---

#### **8.3 Event Listeners**

Add an event listener to the button `myButton`:
When clicked, it should:

1. Read the value of the input `myInput`
2. Print it in the console
3. Clear the input after printing

---

#### **8.4 Event Object**

Modify your button’s event listener to log:

```js
console.log(event.target, event.type);
```

Then, add a `keydown` event on `document` and log the pressed key:

---

#### **8.5 Form Handling**

First, prevent the form from reloading.

Then log an object with all form data:

```js
{ username: "Alex", email: "alex@mail.com" }
```

Use `new FormData(form)` and convert it with `Object.fromEntries()`.

---

#### **8.6 Dynamic List Game**

Turn the last section into a mini todo list:

* When clicking "Add Task", get the input value
* Create a new `<li>` element with that text
* Add a "Remove" button inside each `<li>`
* When clicking the "Remove", remove that `<li>` from the list

---

### Bonus Challenge

Add some CSS directly from JS using element style or toggle a class with `.classList.add()` / `.classList.toggle()`.

---

## Exercise 9: localStorage & JSON (•ᴗ•)

* Save a user object to `localStorage`
* Retrieve and display it on reload
* Clear it with a button

Use `JSON.stringify()` and `JSON.parse()` for conversion.

---

Many issues come from simple errors. Learn how to find and fix them!

**Tips:**
- Use `console.log()` to track variable values.
- Check your browser DevTools → **Console** and **Sources** tab.
- `undefined` means a variable exists but has no value.
- `ReferenceError` often means you used something before declaring it.

---

## Before the final exercise

Learn how to split code into multiple files.

**math.js**
```js
export function add(a, b) {
  return a + b;
}
```

**main.js**
```js
import { add } from './math.js';
console.log(add(2, 3));
```

Try creating a small utility file and importing it into another JS file.

---

## Exercise 10: Mini Project – Pokémon Fetcher (≧◡≦) ♡

Create a mini **Pokémon search app**:

1. Input field for Pokémon name
2. Button to search
3. Display Pokémon sprite, name, type, and stats
4. Show an error if not found

**Bonus mini-quests:**
* Add a random Pokémon button
* Save last 5 searches in `localStorage`
* Add a small loading animation

API: [https://pokeapi.co/](https://pokeapi.co/)

---

## End of Workshop (´｡• ᵕ •｡`)

You’ve completed the journey! You now know:
- JS variables & types
- Functions & arrays
- Objects & loops
- Modern ES6 syntax
- Basic DOM manipulation & async fetch
- Debugging, modules, and backend context

Thanks and good luck for your next project !
