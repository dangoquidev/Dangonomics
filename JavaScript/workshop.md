# Workshop – JavaScript Core & Practice

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-green.svg)]()
[![Practice](https://img.shields.io/badge/Type-Hands--on%20Practice-blue.svg)]()

## Introduction

Welcome to the **JavaScript Core Workshop**! You've already written some JS — now it's time to **revisit, structure, and solidify your fundamentals** like a pro developer.

**Important:**
Some tasks will require you to **research solutions online** (MDN, Stack Overflow, official docs).
This mirrors how real developers learn and solve problems in the wild.

**Prerequisites:**
Basic understanding of HTML and previous exposure to JS syntax.

---

## Resources

* [MDN JavaScript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [JavaScript.info Guide](https://javascript.info/)
* Console testing playground: [JSFiddle](https://jsfiddle.net/) / [CodePen](https://codepen.io/)

---

## Exercise 1: Variables & Types

### Objective

Understand how JavaScript handles variable declarations, scope, and type conversions.

### Tasks

**1.1 Create Variables**

```js
let name = "Alex";
const age = 25;
var city = "Paris";
```

**RESEARCH TASK:**
Explain the difference between `var`, `let`, and `const`.
Which one should you prefer in modern JS? Why is `var` considered outdated?

---

**1.2 Type Checking**

Create different variables:

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

**RESEARCH TASK:**
* What's the difference between `==` and `===` in JS?
* Why does `typeof null` return `"object"`? Is this a bug?
* How can you check if a variable is an array?

---

**1.3 Type Coercion**

Predict the output before running:

```js
console.log("5" + 3);
console.log("5" - 3);
console.log(true + 1);
console.log(false + "hello");
```

**RESEARCH TASK:**
Understand implicit vs explicit type conversion in JavaScript.

---

**1.4 Truthy & Falsy**

Create an array of mixed values and filter only the truthy ones:

```js
const values = [0, "hello", "", null, undefined, NaN, [], {}, "0", false];
// Filter to keep only truthy values
```

**Hint:** Use `Boolean(value)` or `!!value`.

---

## Exercise 2: Functions & Scope

### Objective

Master different ways to declare functions and understand scope.

### Tasks

**2.1 Function Declarations vs Expressions**

Create three versions of a function that multiplies two numbers:

1. Classic function declaration
2. Function expression
3. Arrow function

Test them all. What's the difference in syntax?

---

**2.2 Default Parameters & Rest**

```js
function greet(name = "stranger") {
  return `Hello, ${name}!`;
}
```

Test with and without arguments.

**RESEARCH TASK:**
Create a function `sum(...numbers)` that accepts any number of arguments and returns their sum.
Research "rest parameters" in JavaScript.

---

**2.3 Closure Counter**

**RESEARCH TASK:**
Create a function `createCounter()` that returns another function. Each time you call the returned function, it should increment and return a counter.

Expected behavior:

```js
const counter1 = createCounter();
console.log(counter1()); // 1
console.log(counter1()); // 2
console.log(counter1()); // 3

const counter2 = createCounter();
console.log(counter2()); // 1 (independent counter)
```

→ Research "JavaScript closure" and "lexical scope".

---

**2.4 Higher Order Functions**

**RESEARCH TASK:**
Create a function `repeat(n, action)` that executes a callback function `n` times.

```js
repeat(3, () => console.log("Hello"));
// Should print "Hello" 3 times
```

---

## Exercise 3: Arrays & Methods

### Objective

Learn how to manipulate and transform data structures efficiently.

### Tasks

**3.1 Array Operations**

Given this array:

```js
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
```

Perform these operations **in separate steps**:

1. Filter only even numbers
2. Map each number to its square
3. Reduce to get the sum of all numbers
4. Find the first number greater than 5
5. Check if all numbers are positive

**RESEARCH TASK:**
What's the difference between `.map()` and `.forEach()`? When should you use each?

---

**3.2 Array Transformation Challenge**

```js
const products = [
  { name: "Laptop", price: 1000, category: "tech" },
  { name: "Phone", price: 500, category: "tech" },
  { name: "Shirt", price: 30, category: "clothing" },
  { name: "Shoes", price: 80, category: "clothing" }
];
```

Tasks:
* Get all product names
* Filter products with price > 50
* Calculate total price of all products
* Get only tech products

---

**3.3 Sorting & Reversing**

**RESEARCH TASK:**
Sort the products array by price (ascending and descending).
Research how `.sort()` works with objects.

---

**3.4 Chaining Methods**

Combine multiple array methods in one chain:
From the numbers array, get the sum of squares of even numbers.

```js
const result = numbers
  // your code here
```

---

## Exercise 4: Objects & Destructuring

### Objective

Master object manipulation and modern syntax.

### Tasks

**4.1 Object Basics**

Create a `person` object with properties: name, age, city, and a method `introduce()` that returns a string.

```js
const person = {
  // your code
};

console.log(person.introduce()); // "Hi, I'm Alex, 25 years old from Paris"
```

---

**4.2 Object Destructuring**

Extract properties from this object using destructuring:

```js
const user = { 
  name: "Alex", 
  age: 25, 
  city: "Paris",
  email: "alex@mail.com"
};

// Extract name and email in one line
```

**RESEARCH TASK:**
How do you rename variables during destructuring?
How do you set default values?

---

**4.3 Spread & Merge Objects**

```js
const defaults = { theme: "dark", lang: "en" };
const userPrefs = { lang: "fr", notifications: true };
```

Merge these objects so `userPrefs` overrides `defaults`.

**RESEARCH TASK:**
What happens if you spread in different orders?

---

**4.4 Group by Property**

**RESEARCH TASK:**
Given this array:

```js
const users = [
  { name: "Alex", city: "Paris" },
  { name: "Juliette", city: "Lyon" },
  { name: "Noa", city: "Paris" },
  { name: "Marc", city: "Lyon" }
];
```

Return an object grouped by city:

```js
{
  Paris: ["Alex", "Noa"],
  Lyon: ["Juliette", "Marc"]
}
```

Hint: Use `Array.reduce()` to build the result object.

---

**4.5 Object Methods**

**RESEARCH TASK:**
Use `Object.keys()`, `Object.values()`, and `Object.entries()` on an object.
What does each return?

---

## Exercise 5: Control Flow & Loops

### Objective

Use conditions and loops to build small logical programs.

### Tasks

**5.1 FizzBuzz Classic**

Loop from 1 to 50:

* Print "Fizz" if divisible by 3
* Print "Buzz" if divisible by 5
* Print "FizzBuzz" if divisible by both
* Otherwise print the number

---

**5.2 Switch Statement**

**RESEARCH TASK:**
Create a function `getDayName(dayNumber)` that takes a number (1-7) and returns the day name using a `switch` statement.

---

**5.3 Counting Letters**

**RESEARCH TASK:**
Write a function `countLetters(str)` that returns how many times each letter appears.

```js
countLetters("banana");
// { b: 1, a: 3, n: 2 }
```

→ Research "iterating over strings" and "using objects as maps".

---

**5.4 For...of vs For...in**

**RESEARCH TASK:**
What's the difference between `for...of` and `for...in`?
Give examples with arrays and objects.

---

## Exercise 6: Modern ES6+ Features

### Objective

Use modern syntax to make code cleaner and more readable.

### Tasks

**6.1 Template Literals**

Replace this concatenation:

```js
let name = "Alex";
let age = 25;
console.log("Hello, my name is " + name + " and I am " + age + " years old.");
```

With template literals (backticks).

**RESEARCH TASK:**
Can you use expressions inside template literals? Try `${2 + 2}`.

---

**6.2 Spread Operator**

```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
```

Combine these arrays using the spread operator.

**RESEARCH TASK:**
How do you copy an array without mutating the original?

---

**6.3 Rest Parameters**

**RESEARCH TASK:**
Explain the difference between spread (`...arr`) and rest (`...args`).
Create examples for both.

---

**6.4 Destructuring Arrays**

```js
const colors = ["red", "green", "blue", "yellow"];
```

Extract the first two colors and the rest in separate variables.

**RESEARCH TASK:**
How do you skip elements during array destructuring?

---

**6.5 Optional Chaining**

**RESEARCH TASK:**
Research the `?.` operator. How does it help with nested objects?

```js
const user = {
  profile: {
    address: {
      city: "Paris"
    }
  }
};

// Safely access city even if profile or address is undefined
```

---

**6.6 Nullish Coalescing**

**RESEARCH TASK:**
What's the difference between `||` and `??`?

```js
const value1 = 0 || "default";
const value2 = 0 ?? "default";
```

What will each variable contain?

---

## Exercise 7: Asynchronous JavaScript

### Objective

Understand how JS handles asynchronous code and promises.

### Tasks

**7.1 Timeout Promise**

**RESEARCH TASK:**
Create a function `delay(ms)` that returns a promise resolved after `ms` milliseconds.

```js
delay(2000).then(() => console.log("Done after 2 seconds!"));
```

→ Research "Promise constructor" and `setTimeout`.

---

**7.2 Promise Chaining**

Create a sequence of promises that:
1. Waits 1 second, logs "First"
2. Waits 1 more second, logs "Second"
3. Waits 1 more second, logs "Third"

Use `.then()` chaining.

---

**7.3 Fetch API**

**RESEARCH TASK:**
Use `fetch()` to get data from:
`https://jsonplaceholder.typicode.com/users`

Log all usernames in the console.

What does `.json()` do on the response?

---

**7.4 Async/Await**

**RESEARCH TASK:**
Rewrite the previous fetch using `async/await`.
Add proper error handling with `try/catch`.

```js
async function getUsers() {
  // your code
}
```

---

**7.5 Promise.all**

**RESEARCH TASK:**
Fetch multiple endpoints simultaneously using `Promise.all()`:

* `https://jsonplaceholder.typicode.com/users/1`
* `https://jsonplaceholder.typicode.com/posts/1`

Log both results when both requests complete.

---

**7.6 Error Handling**

**RESEARCH TASK:**
What happens if a fetch fails? How do you catch network errors?
Try fetching from an invalid URL and handle the error properly.

---

## Exercise 8: DOM Manipulation

### Objective

Practice interaction with the HTML document.

### Tasks

**8.1 Selecting Elements**

**RESEARCH TASK:**
What's the difference between:
* `getElementById()`
* `querySelector()`
* `querySelectorAll()`
* `getElementsByClassName()`

Select elements using each method.

---

**8.2 Creating Elements**

**RESEARCH TASK:**
Create a new `<div>` element, add text, a class, and append it to the document body.

Research: `createElement`, `textContent`, `classList.add()`, `appendChild()`.

---

**8.3 Event Listeners**

Create a button and input field.
Add a click listener to the button that logs the input value.

**RESEARCH TASK:**
What's the difference between `onclick="..."` attribute and `addEventListener()`?

---

**8.4 Event Object**

**RESEARCH TASK:**
What information is available in the `event` object?
Try logging `event.target`, `event.type`, `event.key` (for keyboard events).

---

**8.5 Form Handling**

Create a form with fields: name, email, age.

**RESEARCH TASK:**
Prevent form submission default behavior and log form data instead.
Research `event.preventDefault()`.

---

**8.6 Dynamic List**

Create a todo list where:
* Users can add items
* Each item has a delete button
* Clicking delete removes the item

**RESEARCH TASK:**
How do you remove an element from the DOM?
Research `removeChild()` vs `remove()`.

---

## Exercise 9: localStorage & JSON

### Objective

Persist data in the browser.

### Tasks

**9.1 Save & Load Data**

**RESEARCH TASK:**
Use `localStorage` to:
* Save a user object
* Retrieve it on page load
* Clear it

Research: `localStorage.setItem()`, `getItem()`, `removeItem()`.

---

**9.2 JSON Methods**

**RESEARCH TASK:**
What do `JSON.stringify()` and `JSON.parse()` do?
Why do we need them for localStorage?

---

**9.3 Persistent Todo List**

Enhance the previous todo list to save items in localStorage.
When the page reloads, todos should still be there.

---

## Exercise 10: Debugging & Console

### Objective

Use developer tools efficiently.

### Tasks

**10.1 Console Methods**

Try all these:

```js
console.log()
console.warn()
console.error()
console.table()
console.group() / console.groupEnd()
console.time() / console.timeEnd()
```

**RESEARCH TASK:**
When should you use each console method?

---

**10.2 Debugger Statement**

**RESEARCH TASK:**
Insert `debugger;` in your code.
Open DevTools and see what happens.
How do you step through code execution?

---

**10.3 Error Types**

**RESEARCH TASK:**
What's the difference between:
* `SyntaxError`
* `ReferenceError`
* `TypeError`

Create examples of each.

---

## Exercise 11: Advanced Array Challenges

### Objective

Combine everything you've learned.

### Tasks

**11.1 Flatten Array**

**RESEARCH TASK:**
Flatten a nested array without using `.flat()`.

```js
const nested = [1, [2, 3], [4, [5, 6]]];
// Result: [1, 2, 3, 4, 5, 6]
```

---

**11.2 Remove Duplicates**

**RESEARCH TASK:**
Remove duplicates from an array.
Research: `Set` data structure.

```js
const arr = [1, 2, 2, 3, 4, 4, 5];
// Result: [1, 2, 3, 4, 5]
```

---

**11.3 Array Intersection**

**RESEARCH TASK:**
Find common elements between two arrays.

```js
const arr1 = [1, 2, 3, 4];
const arr2 = [3, 4, 5, 6];
// Result: [3, 4]
```

---

**11.4 Sort Objects by Multiple Properties**

**RESEARCH TASK:**
Sort an array of users first by age, then by name if ages are equal.

---

## Exercise 12: String Manipulation

### Objective

Master string operations.

### Tasks

**12.1 Reverse String**

Reverse a string **without** using `.reverse()`.

---

**12.2 Palindrome Check**

**RESEARCH TASK:**
Create a function that checks if a word is a palindrome.

```js
isPalindrome("racecar"); // true
isPalindrome("hello");   // false
```

Ignore case and spaces.

---

**12.3 Count Vowels**

Count how many vowels (a, e, i, o, u) are in a string.

---

**12.4 Capitalize Words**

**RESEARCH TASK:**
Create a function that capitalizes the first letter of each word.

```js
capitalizeWords("hello world"); // "Hello World"
```

---

## Exercise 13: Project – Pokémon Fetcher 🎮

### Objective

Combine async + DOM + logic in a real application.

### Requirements

Build a Pokémon search application:

1. **HTML Structure:**
   * Input field for Pokémon name
   * Search button
   * Display area for results

2. **Functionality:**
   * User types a Pokémon name (e.g., "pikachu")
   * Click search button
   * Fetch data from: `https://pokeapi.co/api/v2/pokemon/<name>`
   * Display:
     - Pokémon sprite (image)
     - Name
     - Types (e.g., "Electric")
     - Base stats (HP, Attack, Defense)

3. **Error Handling:**
   * If Pokémon not found, show error message
   * Handle network errors

4. **Bonus Features:**
   * Loading indicator while fetching
   * Search history (store last 5 searches in localStorage)
   * Random Pokémon button
   * Style it with CSS

**RESEARCH TASKS:**
* How to extract specific data from nested API responses?
* How to dynamically create and style DOM elements?
* How to handle lowercase/uppercase input?

**API Documentation:** [PokeAPI](https://pokeapi.co/)

---

## Exercise 14: Bonus Challenges 🔥

### Logic Puzzles

**14.1 Fibonacci Sequence**

**RESEARCH TASK:**
Generate the first N numbers of the Fibonacci sequence.

```js
fibonacci(7); // [0, 1, 1, 2, 3, 5, 8]
```

---

**14.2 Prime Numbers**

Check if a number is prime.

---

**14.3 Factorial**

Calculate factorial using recursion.

**RESEARCH TASK:**
What is recursion? When should you use it?

---

**14.4 Anagram Checker**

Check if two strings are anagrams of each other.

```js
isAnagram("listen", "silent"); // true
```

---

**14.5 Random Number Generator**

Generate a random integer between `min` and `max` (inclusive).

**RESEARCH TASK:**
How does `Math.random()` work?

---

**14.6 Debounce Function**

**RESEARCH TASK:**
Create a debounce function that delays execution until after a user stops typing.

```js
const debouncedSearch = debounce(searchFunction, 500);
```

This is used in real search bars!

---

## End of Workshop

You've reviewed:

✅ JavaScript Core Syntax  
✅ Variables, Types & Type Coercion  
✅ Functions, Closures & Scope  
✅ Arrays & Advanced Methods  
✅ Objects & Destructuring  
✅ Modern ES6+ Features  
✅ Async Code (Promises, Fetch, Async/Await)  
✅ DOM Manipulation & Events  
✅ localStorage & Data Persistence  
✅ Debugging Techniques  

**Next Steps:**
* Build a complete web application using all these concepts
* Learn a framework (React, Vue, or Svelte)
* Practice on [LeetCode](https://leetcode.com/) or [Codewars](https://www.codewars.com/)
* Contribute to open source projects

Remember: **The best way to learn is by building real projects!**

*Now go forth and code! (づ｡◕‿‿◕｡)づ*