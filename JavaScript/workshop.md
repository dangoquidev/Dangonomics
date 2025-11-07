# Workshop – JavaScript Core & Practice (´･ᴗ･` )

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-green.svg)]()
[![Practice](https://img.shields.io/badge/Type-Hands--on%20Practice-blue.svg)]()

---

## Introduction (⁄⁄>////<⁄⁄)

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

**1.1 Create Variables**
```js
let name = "Alex";
const age = 25;
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
Guess before you run it — JS can be surprising (°ロ°) !

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
Try calling it with and without arguments.

Create a function `sum(...numbers)` that accepts any number of arguments and returns their sum.

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
```js
const person = {
  name: "Alex",
  age: 25,
  city: "Paris",
  introduce() {
    return `Hi, I'm ${this.name}, ${this.age} years old from ${this.city}`;
  }
};
```

---

**4.2 Destructuring**
```js
const user = { name: "Alex", age: 25, city: "Paris", email: "alex@mail.com" };
const { name, email } = user;
```
→ Try renaming or giving default values.

---

**4.3 Spread & Merge**
```js
const defaults = { theme: "dark", lang: "en" };
const userPrefs = { lang: "fr", notifications: true };
const merged = { ...defaults, ...userPrefs };
```
---

## Exercise 5: Control Flow & Loops (｡•̀ᴗ-)✧

### Objective
Write logic using conditions and loops.

### Tasks

**5.1 FizzBuzz**
Loop from 1 to 50:
* Print "Fizz" if divisible by 3
* "Buzz" if divisible by 5
* "FizzBuzz" if both
* Else print the number

---

**5.2 Switch Statement**
Create a function `getDayName(dayNumber)` that takes a number (1-7) and returns the weekday name.

---

**5.4 For...of vs For...in**
Try both on arrays and objects. What’s the difference?

---

## Exercise 6: Modern ES6+ Features (´▽`ʃ♡ƪ)

**6.1 Template Literals** – use backticks instead of + concatenation.

**6.2 Spread Operator** – combine or copy arrays.

**6.3 Rest Parameters** – handle multiple arguments in functions.

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

## Exercise 8: DOM Manipulation (⁄⁄>////<⁄⁄)

**8.1 Selecting Elements** – try `getElementById`, `querySelector`, etc.

**8.2 Creating Elements** – use `createElement`, `textContent`, and `appendChild`.

**8.3 Event Listeners** – create a button + input, print the input value on click.

**8.4 Event Object** – inspect `event.target`, `event.type`, `event.key`.

**8.5 Form Handling** – prevent default submission and log form data.

**8.6 Dynamic List Game** – make a tiny todo list with add/remove buttons.

---

## Exercise 9: localStorage & JSON (•ᴗ•)

* Save a user object to `localStorage`
* Retrieve and display it on reload
* Clear it with a button

Use `JSON.stringify()` and `JSON.parse()` for conversion.

---

## Exercise 13: Mini Project – Pokémon Fetcher (≧◡≦) ♡

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

Next steps:
* Build your own small web app
* Learn Express.js or React
* Practice every day — small steps build mastery (๑˃̵ᴗ˂̵)و

