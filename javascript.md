# JavaScript Concepts to Learn for Full-Stack Development

This README is a practical JavaScript roadmap for building real-world frontend and full-stack apps.

It includes:

- JavaScript fundamentals
- Functions
- Arrays and objects
- DOM manipulation
- Events
- Async JavaScript
- Fetch API
- OOP in JavaScript
- ES6+ features
- Browser APIs
- Debugging
- Practice projects

---

# 1. What Is JavaScript?

JavaScript is the programming language of the web.

It is used for:

- Making websites interactive
- Handling button clicks
- Updating UI without refreshing the page
- Fetching data from APIs
- Building frontend apps with React
- Building backend apps with Node.js
- Creating full-stack apps
- Building real-time apps
- Creating browser-based tools and dashboards

---

# 2. JavaScript Setup

You can run JavaScript in:

## Browser Console

Open Chrome DevTools:

```txt
Right click page -> Inspect -> Console
```

## HTML File

```html
<script>
  console.log("Hello JavaScript");
</script>
```

## External JS File

```html
<script src="script.js"></script>
```

## Node.js

```bash
node app.js
```

---

# 3. Variables

Variables store data.

## var

Old way. Avoid using it in modern JavaScript.

```js
var name = "Abhishek";
```

## let

Use when value can change.

```js
let age = 22;
age = 23;
```

## const

Use when value should not be reassigned.

```js
const country = "India";
```

## Rule

Use `const` by default.  
Use `let` only when reassignment is needed.  
Avoid `var`.

---

# 4. Data Types

JavaScript has primitive and non-primitive data types.

## Primitive Types

```js
const name = "Abhishek"; // string
const age = 22; // number
const isLoggedIn = true; // boolean
const score = null; // null
let city; // undefined
const id = Symbol("id"); // symbol
const bigNumber = 12345678901234567890n; // bigint
```

## Non-Primitive Types

```js
const user = {
  name: "Abhishek",
  age: 22,
};

const skills = ["HTML", "CSS", "JavaScript"];
```

---

# 5. Operators

## Arithmetic Operators

```js
const a = 10;
const b = 3;

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
console.log(a % b);
console.log(a ** b);
```

## Comparison Operators

```js
console.log(5 > 3);
console.log(5 < 3);
console.log(5 >= 5);
console.log(5 <= 4);
console.log(5 == "5");
console.log(5 === "5");
```

## Important

Prefer `===` instead of `==`.

```js
5 == "5"; // true
5 === "5"; // false
```

## Logical Operators

```js
const isLoggedIn = true;
const isAdmin = false;

console.log(isLoggedIn && isAdmin);
console.log(isLoggedIn || isAdmin);
console.log(!isLoggedIn);
```

---

# 6. Strings

Strings store text.

```js
const name = "Abhishek";
const message = "Hello " + name;
```

## Template Literals

```js
const name = "Abhishek";
const age = 22;

const message = `My name is ${name} and I am ${age} years old.`;
```

## Common String Methods

```js
const text = "JavaScript is awesome";

console.log(text.length);
console.log(text.toUpperCase());
console.log(text.toLowerCase());
console.log(text.includes("Script"));
console.log(text.startsWith("Java"));
console.log(text.endsWith("awesome"));
console.log(text.slice(0, 10));
console.log(text.split(" "));
console.log(text.replace("awesome", "powerful"));
console.log(text.trim());
```

---

# 7. Numbers and Math

```js
const price = 99.99;

console.log(Math.round(price));
console.log(Math.floor(price));
console.log(Math.ceil(price));
console.log(Math.random());
console.log(Math.max(10, 20, 30));
console.log(Math.min(10, 20, 30));
```

## Random Number Example

```js
const randomNumber = Math.floor(Math.random() * 10) + 1;
console.log(randomNumber);
```

---

# 8. Conditionals

Conditionals help your program make decisions.

## if else

```js
const age = 18;

if (age >= 18) {
  console.log("You can vote");
} else {
  console.log("You cannot vote");
}
```

## else if

```js
const marks = 85;

if (marks >= 90) {
  console.log("A grade");
} else if (marks >= 75) {
  console.log("B grade");
} else {
  console.log("C grade");
}
```

## Ternary Operator

```js
const age = 20;

const result = age >= 18 ? "Adult" : "Minor";
console.log(result);
```

## switch

```js
const role = "admin";

switch (role) {
  case "admin":
    console.log("Full access");
    break;
  case "user":
    console.log("Limited access");
    break;
  default:
    console.log("Guest access");
}
```

---

# 9. Loops

Loops help repeat code.

## for loop

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

## while loop

```js
let count = 1;

while (count <= 5) {
  console.log(count);
  count++;
}
```

## for...of

Used for arrays.

```js
const skills = ["HTML", "CSS", "JavaScript"];

for (const skill of skills) {
  console.log(skill);
}
```

## for...in

Used for object keys.

```js
const user = {
  name: "Abhishek",
  age: 22,
};

for (const key in user) {
  console.log(key, user[key]);
}
```

---

# 10. Functions

Functions are reusable blocks of code.

## Function Declaration

```js
function greet(name) {
  return `Hello ${name}`;
}

console.log(greet("Abhishek"));
```

## Function Expression

```js
const greet = function (name) {
  return `Hello ${name}`;
};
```

## Arrow Function

```js
const greet = (name) => {
  return `Hello ${name}`;
};
```

## Short Arrow Function

```js
const add = (a, b) => a + b;
```

## Default Parameters

```js
function greet(name = "User") {
  return `Hello ${name}`;
}
```

---

# 11. Scope

Scope decides where a variable can be accessed.

## Global Scope

```js
const name = "Abhishek";

function showName() {
  console.log(name);
}
```

## Function Scope

```js
function test() {
  const message = "Hello";
  console.log(message);
}

// console.log(message); // Error
```

## Block Scope

```js
if (true) {
  let x = 10;
  const y = 20;
}

// console.log(x); // Error
```

---

# 12. Hoisting

Hoisting means JavaScript moves declarations to the top internally.

## Function Hoisting

```js
sayHello();

function sayHello() {
  console.log("Hello");
}
```

This works.

## var Hoisting

```js
console.log(name);
var name = "Abhishek";
```

This gives `undefined`, not an error.

## let and const

```js
console.log(age);
let age = 22;
```

This gives an error.

---

# 13. Arrays

Arrays store lists.

```js
const skills = ["HTML", "CSS", "JavaScript"];
```

## Access Items

```js
console.log(skills[0]);
console.log(skills[1]);
```

## Add and Remove Items

```js
skills.push("React");
skills.pop();

skills.unshift("Git");
skills.shift();
```

## Common Array Methods

```js
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((num) => console.log(num));

const doubled = numbers.map((num) => num * 2);

const even = numbers.filter((num) => num % 2 === 0);

const found = numbers.find((num) => num > 3);

const total = numbers.reduce((sum, num) => sum + num, 0);

const hasEven = numbers.some((num) => num % 2 === 0);

const allPositive = numbers.every((num) => num > 0);
```

## Most Important Array Methods

Learn these deeply:

- `map`
- `filter`
- `reduce`
- `find`
- `some`
- `every`
- `forEach`
- `includes`
- `sort`
- `slice`
- `splice`

---

# 14. Objects

Objects store data in key-value pairs.

```js
const user = {
  name: "Abhishek",
  age: 22,
  isDeveloper: true,
};
```

## Access Object Values

```js
console.log(user.name);
console.log(user["age"]);
```

## Add New Property

```js
user.city = "Jamshedpur";
```

## Update Property

```js
user.age = 23;
```

## Delete Property

```js
delete user.city;
```

## Object Methods

```js
const user = {
  name: "Abhishek",
  greet() {
    console.log(`Hello, I am ${this.name}`);
  },
};

user.greet();
```

---

# 15. Destructuring

Destructuring helps extract values.

## Object Destructuring

```js
const user = {
  name: "Abhishek",
  age: 22,
};

const { name, age } = user;
```

## Array Destructuring

```js
const colors = ["red", "green", "blue"];

const [first, second] = colors;
```

## Function Parameter Destructuring

```js
function printUser({ name, age }) {
  console.log(name, age);
}

printUser({ name: "Abhishek", age: 22 });
```

---

# 16. Spread and Rest Operator

## Spread

Used to copy or merge.

```js
const arr1 = [1, 2];
const arr2 = [3, 4];

const combined = [...arr1, ...arr2];
```

```js
const user = {
  name: "Abhishek",
};

const updatedUser = {
  ...user,
  age: 22,
};
```

## Rest

Used to collect remaining values.

```js
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3, 4));
```

---

# 17. DOM

DOM stands for Document Object Model.

The browser converts your HTML into a tree-like structure called the DOM.

JavaScript can use the DOM to:

- Select elements
- Change text
- Change styles
- Add elements
- Remove elements
- Handle user events
- Update UI dynamically

---

# 18. Selecting DOM Elements

## getElementById

```html
<h1 id="title">Hello</h1>
```

```js
const title = document.getElementById("title");
console.log(title);
```

## querySelector

```js
const title = document.querySelector("#title");
const button = document.querySelector(".btn");
```

## querySelectorAll

```js
const items = document.querySelectorAll(".item");

items.forEach((item) => {
  console.log(item.textContent);
});
```

---

# 19. Changing DOM Content

```html
<h1 id="title">Old Title</h1>
```

```js
const title = document.querySelector("#title");

title.textContent = "New Title";
title.innerHTML = "<span>New HTML Title</span>";
```

## Difference

Use `textContent` when inserting text.

Use `innerHTML` only when you need to insert HTML.

Be careful with `innerHTML` because it can create security issues if you insert user input directly.

---

# 20. Changing Styles With JavaScript

```js
const title = document.querySelector("#title");

title.style.color = "red";
title.style.fontSize = "40px";
title.style.backgroundColor = "black";
```

Better approach:

```js
title.classList.add("active");
title.classList.remove("hidden");
title.classList.toggle("dark");
```

---

# 21. Creating and Removing Elements

## Create Element

```js
const li = document.createElement("li");
li.textContent = "Learn JavaScript";

document.querySelector("#todo-list").appendChild(li);
```

## Remove Element

```js
li.remove();
```

---

# 22. DOM Events

Events are actions performed by the user or browser.

Examples:

- Click
- Submit
- Input change
- Key press
- Mouse move
- Page load

## Click Event

```html
<button id="btn">Click Me</button>
```

```js
const btn = document.querySelector("#btn");

btn.addEventListener("click", () => {
  console.log("Button clicked");
});
```

## Input Event

```html
<input id="nameInput" />
```

```js
const input = document.querySelector("#nameInput");

input.addEventListener("input", (event) => {
  console.log(event.target.value);
});
```

## Submit Event

```html
<form id="form">
  <input id="todoInput" />
  <button type="submit">Add</button>
</form>
```

```js
const form = document.querySelector("#form");

form.addEventListener("submit", (event) => {
  event.preventDefault();

  const input = document.querySelector("#todoInput");
  console.log(input.value);
});
```

---

# 23. Event Object

The event object gives information about the event.

```js
button.addEventListener("click", (event) => {
  console.log(event.target);
});
```

Useful properties:

- `event.target`
- `event.currentTarget`
- `event.preventDefault()`
- `event.stopPropagation()`
- `event.key`
- `event.clientX`
- `event.clientY`

---

# 24. Event Bubbling

Event bubbling means an event starts from the clicked element and moves up to its parents.

```html
<div id="parent">
  <button id="child">Click</button>
</div>
```

```js
document.querySelector("#parent").addEventListener("click", () => {
  console.log("Parent clicked");
});

document.querySelector("#child").addEventListener("click", () => {
  console.log("Child clicked");
});
```

When the child button is clicked, both child and parent handlers can run.

To stop bubbling:

```js
event.stopPropagation();
```

---

# 25. Event Delegation

Event delegation means adding one event listener to a parent instead of adding listeners to many children.

```html
<ul id="todoList">
  <li>Todo 1</li>
  <li>Todo 2</li>
  <li>Todo 3</li>
</ul>
```

```js
const todoList = document.querySelector("#todoList");

todoList.addEventListener("click", (event) => {
  if (event.target.tagName === "LI") {
    console.log("Clicked:", event.target.textContent);
  }
});
```

This is useful when list items are added dynamically.

---

# 26. Browser Storage

## localStorage

Data stays even after closing browser.

```js
localStorage.setItem("theme", "dark");

const theme = localStorage.getItem("theme");

localStorage.removeItem("theme");

localStorage.clear();
```

## sessionStorage

Data is removed when the tab is closed.

```js
sessionStorage.setItem("token", "abc123");
```

## JSON With Storage

```js
const user = {
  name: "Abhishek",
  age: 22,
};

localStorage.setItem("user", JSON.stringify(user));

const savedUser = JSON.parse(localStorage.getItem("user"));
```

---

# 27. JSON

JSON stands for JavaScript Object Notation.

It is used to send data between frontend and backend.

## JavaScript Object

```js
const user = {
  name: "Abhishek",
  age: 22,
};
```

## JSON String

```json
{
  "name": "Abhishek",
  "age": 22
}
```

## JSON.stringify

Converts JavaScript object into JSON string.

```js
const jsonString = JSON.stringify(user);
```

## JSON.parse

Converts JSON string into JavaScript object.

```js
const parsedUser = JSON.parse(jsonString);
```

---

# 28. Asynchronous JavaScript

JavaScript can handle tasks that take time, like:

- API calls
- Timers
- File loading
- Database requests in Node.js
- User interactions

---

# 29. setTimeout and setInterval

## setTimeout

Runs code after a delay.

```js
setTimeout(() => {
  console.log("Runs after 2 seconds");
}, 2000);
```

## setInterval

Runs code again and again after an interval.

```js
const intervalId = setInterval(() => {
  console.log("Runs every second");
}, 1000);
```

Stop interval:

```js
clearInterval(intervalId);
```

---

# 30. Callbacks

A callback is a function passed into another function.

```js
function greet(name, callback) {
  console.log(`Hello ${name}`);
  callback();
}

greet("Abhishek", () => {
  console.log("Callback executed");
});
```

Callbacks are common in:

- Event listeners
- Array methods
- Timers
- Older async code

---

# 31. Promises

A promise represents a future value.

It can be:

- Pending
- Fulfilled
- Rejected

```js
const promise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Data received");
  } else {
    reject("Something went wrong");
  }
});

promise
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  });
```

---

# 32. async/await

`async/await` makes asynchronous code look cleaner.

```js
async function getData() {
  try {
    const result = await promise;
    console.log(result);
  } catch (error) {
    console.log(error);
  }
}
```

Use `try/catch` for error handling.

---

# 33. Fetch API

Fetch is used to call APIs from the browser.

## GET Request

```js
async function getUsers() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/users");
    const data = await response.json();

    console.log(data);
  } catch (error) {
    console.log("Error:", error);
  }
}

getUsers();
```

## POST Request

```js
async function createPost() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
      },
      body: JSON.stringify({
        title: "New Post",
        body: "This is a post",
        userId: 1,
      }),
    });

    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.log("Error:", error);
  }
}

createPost();
```

---

# 34. Error Handling

## try/catch

```js
try {
  const result = riskyFunction();
  console.log(result);
} catch (error) {
  console.log("Something went wrong:", error.message);
}
```

## Throw Custom Error

```js
function divide(a, b) {
  if (b === 0) {
    throw new Error("Cannot divide by zero");
  }

  return a / b;
}
```

---

# 35. OOP in JavaScript

OOP stands for Object-Oriented Programming.

It helps you structure code using objects and classes.

Main OOP concepts:

- Object
- Class
- Constructor
- Method
- `this`
- Encapsulation
- Inheritance
- Polymorphism
- Abstraction

---

# 36. Objects in OOP

```js
const user = {
  name: "Abhishek",
  email: "abhishek@example.com",

  login() {
    console.log(`${this.name} logged in`);
  },
};

user.login();
```

Here:

- `user` is an object
- `name` and `email` are properties
- `login` is a method
- `this.name` refers to the current object

---

# 37. Classes

A class is a blueprint for creating objects.

```js
class User {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }

  login() {
    console.log(`${this.name} logged in`);
  }
}

const user1 = new User("Abhishek", "abhishek@example.com");
const user2 = new User("Rahul", "rahul@example.com");

user1.login();
user2.login();
```

---

# 38. Constructor

The constructor runs automatically when a new object is created.

```js
class Product {
  constructor(name, price) {
    this.name = name;
    this.price = price;
  }
}

const laptop = new Product("Laptop", 50000);
console.log(laptop.name);
```

---

# 39. this Keyword

`this` refers to the object that is calling the method.

```js
class User {
  constructor(name) {
    this.name = name;
  }

  sayName() {
    console.log(this.name);
  }
}

const user = new User("Abhishek");
user.sayName();
```

Be careful with `this` inside normal functions and arrow functions.

---

# 40. Inheritance

Inheritance allows one class to use features of another class.

```js
class User {
  constructor(name) {
    this.name = name;
  }

  login() {
    console.log(`${this.name} logged in`);
  }
}

class Admin extends User {
  deleteUser() {
    console.log(`${this.name} deleted a user`);
  }
}

const admin = new Admin("Abhishek");

admin.login();
admin.deleteUser();
```

---

# 41. super Keyword

`super` calls the parent class constructor or method.

```js
class User {
  constructor(name) {
    this.name = name;
  }
}

class Admin extends User {
  constructor(name, role) {
    super(name);
    this.role = role;
  }
}

const admin = new Admin("Abhishek", "admin");
console.log(admin.name);
console.log(admin.role);
```

---

# 42. Encapsulation

Encapsulation means hiding internal details and exposing only what is needed.

```js
class BankAccount {
  #balance = 0;

  deposit(amount) {
    if (amount <= 0) {
      throw new Error("Invalid amount");
    }

    this.#balance += amount;
  }

  getBalance() {
    return this.#balance;
  }
}

const account = new BankAccount();
account.deposit(1000);

console.log(account.getBalance());
```

`#balance` is private and cannot be accessed directly outside the class.

---

# 43. Polymorphism

Polymorphism means different classes can have methods with the same name but different behavior.

```js
class Animal {
  speak() {
    console.log("Animal makes sound");
  }
}

class Dog extends Animal {
  speak() {
    console.log("Dog barks");
  }
}

class Cat extends Animal {
  speak() {
    console.log("Cat meows");
  }
}

const animals = [new Dog(), new Cat()];

animals.forEach((animal) => animal.speak());
```

---

# 44. Abstraction

Abstraction means hiding complex implementation details.

Example:

```js
class Payment {
  pay(amount) {
    this.#connectToGateway();
    console.log(`Paid ₹${amount}`);
  }

  #connectToGateway() {
    console.log("Connecting to payment gateway...");
  }
}

const payment = new Payment();
payment.pay(500);
```

The user only calls `pay()`.  
They do not need to know how gateway connection works internally.

---

# 45. Prototypes

JavaScript uses prototypes internally for inheritance.

```js
function User(name) {
  this.name = name;
}

User.prototype.login = function () {
  console.log(`${this.name} logged in`);
};

const user = new User("Abhishek");
user.login();
```

Modern JavaScript usually uses `class`, but classes are built on top of prototypes.

---

# 46. Modules

Modules help split code into multiple files.

## Named Export

```js
// math.js
export function add(a, b) {
  return a + b;
}
```

```js
// app.js
import { add } from "./math.js";

console.log(add(2, 3));
```

## Default Export

```js
// logger.js
export default function logger(message) {
  console.log(message);
}
```

```js
// app.js
import logger from "./logger.js";

logger("Hello");
```

---

# 47. ES6+ Features

Modern JavaScript features you should know:

## let and const

```js
const name = "Abhishek";
let age = 22;
```

## Template Literals

```js
const message = `Hello ${name}`;
```

## Arrow Functions

```js
const add = (a, b) => a + b;
```

## Destructuring

```js
const { name, age } = user;
```

## Spread Operator

```js
const newUser = { ...user, city: "Jamshedpur" };
```

## Optional Chaining

```js
console.log(user?.profile?.avatar);
```

## Nullish Coalescing

```js
const username = inputName ?? "Guest";
```

## Array Methods

```js
const names = users.map((user) => user.name);
```

---

# 48. Closures

A closure happens when a function remembers variables from its outer scope.

```js
function counter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const increment = counter();

console.log(increment());
console.log(increment());
console.log(increment());
```

Closures are used in:

- Private variables
- Event handlers
- React hooks
- Function factories
- State management

---

# 49. Higher-Order Functions

A higher-order function is a function that:

- Takes another function as an argument
- Returns another function

```js
function calculate(a, b, operation) {
  return operation(a, b);
}

const result = calculate(5, 3, (x, y) => x + y);

console.log(result);
```

Array methods like `map`, `filter`, and `reduce` are higher-order functions.

---

# 50. The Event Loop

JavaScript is single-threaded, but it can handle async tasks using the event loop.

Main parts:

- Call stack
- Web APIs
- Callback queue
- Microtask queue
- Event loop

Example:

```js
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```

Output:

```txt
Start
End
Promise
Timeout
```

Promises run before `setTimeout` because promise callbacks go into the microtask queue.

---

# 51. Debouncing

Debouncing delays a function until the user stops doing something.

Useful for:

- Search input
- API calls
- Window resize
- Autocomplete

```js
function debounce(fn, delay) {
  let timerId;

  return function (...args) {
    clearTimeout(timerId);

    timerId = setTimeout(() => {
      fn(...args);
    }, delay);
  };
}

const search = debounce((query) => {
  console.log("Searching for:", query);
}, 500);
```

---

# 52. Throttling

Throttling runs a function at most once in a fixed time.

Useful for:

- Scroll events
- Resize events
- Mouse movement
- Infinite scrolling

```js
function throttle(fn, delay) {
  let shouldWait = false;

  return function (...args) {
    if (shouldWait) return;

    fn(...args);
    shouldWait = true;

    setTimeout(() => {
      shouldWait = false;
    }, delay);
  };
}
```

---

# 53. Browser APIs

Useful browser APIs:

## alert, prompt, confirm

```js
alert("Hello");

const name = prompt("Enter your name");

const confirmed = confirm("Are you sure?");
```

## Location

```js
console.log(window.location.href);
```

## History

```js
history.back();
history.forward();
```

## Navigator

```js
console.log(navigator.userAgent);
```

## Clipboard

```js
await navigator.clipboard.writeText("Copied text");
```

---

# 54. Debugging JavaScript

## console.log

```js
console.log("Value:", value);
```

## console.table

```js
console.table(users);
```

## debugger

```js
function test() {
  debugger;
  console.log("Debugging");
}
```

## Chrome DevTools

Learn:

- Console tab
- Sources tab
- Breakpoints
- Network tab
- Local storage viewer
- Performance basics

---

# 55. JavaScript in React

React uses many JavaScript concepts.

Important JS concepts for React:

- Variables
- Functions
- Arrow functions
- Arrays
- Objects
- Destructuring
- Spread operator
- `map`
- `filter`
- Conditional rendering
- Events
- Modules
- Promises
- async/await
- Fetch API
- Closures

Example:

```jsx
const todos = [
  { id: 1, title: "Learn JS" },
  { id: 2, title: "Learn React" },
];

function TodoList() {
  return (
    <ul>
      {todos.map((todo) => (
        <li key={todo.id}>{todo.title}</li>
      ))}
    </ul>
  );
}
```

---

# 56. JavaScript in Node.js

Node.js uses JavaScript on the backend.

Important JS concepts for Node.js:

- Functions
- Objects
- Modules
- async/await
- Promises
- Error handling
- JSON
- Array methods
- Classes
- Environment variables
- File system basics

Example:

```js
import express from "express";

const app = express();

app.use(express.json());

app.get("/", (req, res) => {
  res.json({
    message: "Server is running",
  });
});

app.listen(3000, () => {
  console.log("Server running on port 3000");
});
```

---

# 57. Learning Order

Follow this order:

1. Variables
2. Data types
3. Operators
4. Strings
5. Numbers and Math
6. Conditionals
7. Loops
8. Functions
9. Scope
10. Arrays
11. Objects
12. Array methods
13. Destructuring
14. Spread/rest
15. DOM selection
16. DOM manipulation
17. DOM events
18. Event bubbling and delegation
19. Forms with DOM
20. localStorage/sessionStorage
21. JSON
22. setTimeout/setInterval
23. Callbacks
24. Promises
25. async/await
26. Fetch API
27. Error handling
28. OOP objects/classes
29. `this`
30. Inheritance
31. Encapsulation
32. Modules
33. ES6+ features
34. Closures
35. Higher-order functions
36. Event loop
37. Debouncing/throttling
38. Browser APIs
39. Debugging
40. JavaScript for React and Node.js

---

# 58. Practice Projects

## Beginner Projects

### 1. Counter App

Concepts:

- Variables
- DOM
- Events
- Updating text

Features:

- Increment
- Decrement
- Reset

---

### 2. Color Changer

Concepts:

- DOM selection
- Events
- Style manipulation
- Math.random

Features:

- Change background color
- Generate random hex color

---

### 3. Simple Calculator

Concepts:

- Functions
- Conditionals
- Events
- Input values

Features:

- Add
- Subtract
- Multiply
- Divide

---

## Intermediate Projects

### 4. Todo App With Local Storage

Concepts:

- DOM
- Events
- Arrays
- Objects
- localStorage
- JSON

Features:

- Add todo
- Delete todo
- Mark completed
- Save in localStorage

---

### 5. Form Validator

Concepts:

- Forms
- Events
- Regex basics
- Error handling
- DOM updates

Features:

- Name validation
- Email validation
- Password validation
- Error messages

---

### 6. Weather App

Concepts:

- Fetch API
- async/await
- DOM updates
- Error handling

Features:

- Search city
- Show temperature
- Show weather status
- Loading state
- Error state

---

## Advanced Projects

### 7. Quiz App

Concepts:

- Arrays
- Objects
- DOM
- Events
- State management

Features:

- Multiple questions
- Score tracking
- Next question
- Result screen

---

### 8. Expense Tracker

Concepts:

- Arrays
- Objects
- localStorage
- Forms
- Array methods

Features:

- Add income
- Add expense
- Delete transaction
- Calculate balance
- Save data

---

### 9. API Dashboard

Concepts:

- Fetch API
- async/await
- Error handling
- DOM rendering
- Loading states

Features:

- Fetch users/posts/products
- Search
- Filter
- Sort
- Render cards/table

---

### 10. OOP Banking System

Concepts:

- Classes
- Constructor
- Methods
- Encapsulation
- Inheritance

Features:

- Create account
- Deposit
- Withdraw
- Check balance
- Admin account
- Private balance

---

# 59. JavaScript Checklist Before React

Before learning React deeply, make sure you know:

- Functions
- Arrow functions
- Arrays
- Objects
- Destructuring
- Spread/rest
- Array methods: `map`, `filter`, `reduce`
- Conditional rendering logic
- DOM basics
- Events
- Forms
- JSON
- Fetch API
- Promises
- async/await
- Modules
- Closures basics

---

# 60. JavaScript Checklist Before Node.js

Before learning backend with Node.js, make sure you know:

- Functions
- Objects
- Modules
- JSON
- Promises
- async/await
- Error handling
- Array methods
- Classes basics
- Environment variables concept
- HTTP request/response basics

---

# Final Advice

Do not try to memorize JavaScript.

Build small things repeatedly.

The most important JavaScript skills for full-stack development are:

- Thinking in data
- Working with arrays and objects
- Writing clean functions
- Handling events
- Understanding async code
- Calling APIs
- Rendering data to UI
- Debugging errors

If you master these, React, Node.js, Express, Next.js, and full-stack development become much easier.
