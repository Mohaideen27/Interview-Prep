Absolutely! Let's prepare you for your JavaScript + TypeScript interview in a way that helps you understand concepts, remember answers, and confidently explain them to an interviewer.

You have 80 questions covering Basic, Intermediate, Advanced JavaScript, and TypeScript. Rather than memorizing definitions, we'll prepare with:

1. Interview-ready answers – how to explain the concept to an interviewer.
2. Simple examples – code you can understand and remember.
3. Important differences – especially commonly asked comparison questions.
4. Follow-up questions – what interviewers might ask next.
5. Practical coding examples – to help you answer confidently.

# JavaScript interview preparation

## Part 1: Basic JavaScript (Questions 1–20)

### 1. What is JavaScript?

Interview answer:

JavaScript is a high-level, dynamically typed, interpreted programming language primarily used to make web pages interactive and dynamic.

It can run in browsers as well as on servers using environments like Node.js.

Example:

```
let name = "John";

console.log("Hello " + name);
```

Remember: HTML provides structure, CSS provides styling, and JavaScript provides functionality and interactivity.

### 2. What are the features of JavaScript?

Important features include:

1. Dynamically typed language.
2. Lightweight and interpreted/JIT-compiled.
3. Supports object-oriented programming.
4. Supports functional programming.
5. Single-threaded execution with an event loop.
6. Asynchronous programming using callbacks, promises, and async/await.
7. Prototype-based inheritance.
8. Cross-platform support.
9. First-class functions.
10. Supports DOM manipulation.

### 3. Difference between Java and JavaScript

| Java                                 | JavaScript                                     |
| ------------------------------------ | ---------------------------------------------- |
| General-purpose programming language | General-purpose scripting/programming language |
| Statically typed                     | Dynamically typed                              |
| Runs on JVM                          | Runs in JS engines                             |
| Class-based inheritance              | Prototype-based inheritance                    |
| Commonly compiled to bytecode        | Commonly JIT-compiled                          |
| Uses `.java` files                   | Uses `.js` files                               |

Interview tip: Java and JavaScript are different languages. Their similar names do not mean they are related in their design.

### 4. What are variables?

Variables are containers used to store data in a program.

JavaScript provides three ways to declare variables:

```
var age = 25;
let name = "John";
const country = "India";
```

### 5. Difference between var, let, and const

This is one of the most important JavaScript interview questions.

| Feature       | var         | let           | const         |
| ------------- | ----------- | ------------- | ------------- |
| Scope         | Function    | Block         | Block         |
| Redeclaration | Yes         | No            | No            |
| Reassignment  | Yes         | Yes           | No            |
| Hoisting      | Yes         | Yes           | Yes           |
| Initial value | `undefined` | Uninitialized | Uninitialized |

Example:

```
var a = 10;
var a = 20; // Allowed

let b = 10;
b = 20; // Allowed
// let b = 30; // Error

const c = 10;
// c = 20; // Error
```

Important: `let` and `const` are hoisted but remain in the Temporal Dead Zone until their declaration is evaluated.

Also, `const` prevents reassignment, not modification of an object.

```
const user = { name: "John" };

user.name = "David"; // Allowed
// user = {}; // Error
```

### 6. What are JavaScript data types?

JavaScript has seven primitive types and one non-primitive category.

Primitive types:

1. String
2. Number
3. Boolean
4. Undefined
5. Null
6. BigInt
7. Symbol

Non-primitive type:

\- Object (including arrays and functions)

Example:

```
let name = "John";
let age = 25;
let isActive = true;
let value;
let result = null;
let bigNumber = 123456789n;
let id = Symbol("id");

let user = { name: "John" };
let numbers = [1, 2, 3];
```

### 7. Difference between primitive and non-primitive data types

| Primitive                         | Non-primitive                     |
| --------------------------------- | --------------------------------- |
| Stores primitive values           | Stores object references          |
| Immutable values                  | Objects can be modified           |
| Copied by value                   | Reference is copied by value      |
| Examples: string, number, boolean | Examples: object, array, function |

Example:

```
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
```

Object example:

```
let obj1 = { name: "John" };
let obj2 = obj1;

obj2.name = "David";

console.log(obj1.name); // David
```

### 8. Difference between == and ===

- `==` compares values after performing type coercion when necessary.
- `===` compares values without type coercion.

```
console.log(5 == "5");  // true
console.log(5 === "5"); // false
```

Interview tip: Always prefer `===` unless you specifically need loose equality.

### 9. What is type coercion?

Type coercion is the process of converting one data type into another.

It can happen automatically (implicit coercion) or manually (explicit conversion).

```
console.log("5" + 2); // "52"
console.log("5" - 2); // 3

console.log(Number("10")); // 10
console.log(String(100));  // "100"
```

### 10. What is NaN?

NaN stands for Not-a-Number.

It represents an invalid numeric result.

```
console.log("hello" / 2); // NaN
console.log(typeof NaN);  // "number"

console.log(Number.isNaN(NaN)); // true
```

### 11. Difference between null and undefined

| null                             | undefined                                              |
| -------------------------------- | ------------------------------------------------------ |
| Intentional absence of value     | Value has not been assigned                            |
| Assigned explicitly              | Usually the default value of an uninitialized variable |
| `typeof null` returns `"object"` | `typeof undefined` returns `"undefined"`               |

```
let a;
let b = null;

console.log(a); // undefined
console.log(b); // null
```

### 12. What is hoisting?

Hoisting is JavaScript's behavior of processing declarations before executing the code in their scope.

Example:

```
console.log(a); // undefined
var a = 10;
```

With `let`:

```
console.log(b); // ReferenceError
let b = 20;
```

Function declaration example:

```
sayHello();

function sayHello() {
    console.log("Hello");
}
```

### 13. What is scope?

Scope determines where a variable can be accessed in a program.

JavaScript has:

- Global scope
- Function scope
- Block scope
- Module scope

### 14. Difference between global, function, and block scope

Global scope:

```
let name = "John";

function greet() {
    console.log(name);
}
```

Function scope:

```
function test() {
    var age = 25;
}

// console.log(age); // Error
```

Block scope:

```
{
    let x = 10;
    const y = 20;
}

// console.log(x); // Error
```

### 15. What is a function?

A function is a reusable block of code that performs a specific task.

```
function add(a, b) {
    return a + b;
}

console.log(add(10, 20)); // 30
```

### 16. Difference between function declaration and function expression

Function declaration:

```
function greet() {
    console.log("Hello");
}
```

Function expression:

```
const greet = function() {
    console.log("Hello");
};
```

| Function declaration             | Function expression                                                         |
| -------------------------------- | --------------------------------------------------------------------------- |
| Can be called before declaration | Cannot be called before initialization                                      |
| Function declaration is hoisted  | Variable declaration is hoisted according to `var`, `let`, or `const` rules |
| Named function is common         | Can be anonymous or named                                                   |

### 17. What are arrow functions?

Arrow functions provide a shorter syntax for writing functions.

```
const add = (a, b) => a + b;

console.log(add(10, 20)); // 30
```

Important differences:

- Arrow functions do not have their own `this`.
- They do not have their own `arguments`.
- They cannot be used as constructors with `new`.
- They cannot be generator functions.

### 18. What is a callback function?

A callback is a function passed as an argument to another function and called by that function.

```
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

function message() {
    console.log("Welcome!");
}

greet("John", message);
```

### 19. What is a higher-order function?

A higher-order function is a function that accepts another function as an argument or returns a function.

```
function calculate(a, b, operation) {
    return operation(a, b);
}

function add(x, y) {
    return x + y;
}

console.log(calculate(10, 20, add)); // 30
```

Examples: `map()`, `filter()`, and `reduce()`.

### 20. What is a closure?

A closure is created when a function remembers and accesses variables from its outer lexical scope, even after the outer function has finished executing.

```
function outer() {
    let count = 0;

    return function inner() {
        count++;
        console.log(count);
    };
}

const counter = outer();

counter(); // 1
counter(); // 2
counter(); // 3
```

Interview tip: Closures are commonly used for data privacy, maintaining state, and function factories.

## Part 2: Intermediate JavaScript (Questions 21–45)

### 21. What is the DOM?

DOM stands for Document Object Model.

It is a programming interface that represents an HTML document as a tree of objects. JavaScript uses the DOM to access and modify HTML elements, attributes, styles, and content.

Example HTML:

```
<h1 id="title">Hello</h1>
```

JavaScript:

```
document.getElementById("title").textContent = "Welcome";
```

### 22. How do you manipulate the DOM?

We can manipulate the DOM using JavaScript methods.

Common methods:

- `getElementById()`
- `querySelector()`
- `querySelectorAll()`
- `createElement()`
- `appendChild()`
- `remove()`
- `setAttribute()`

Example:

```
const heading = document.querySelector("h1");

heading.textContent = "Hello JavaScript";
heading.style.color = "blue";
```

Creating an element:

```
const paragraph = document.createElement("p");

paragraph.textContent = "Welcome!";
document.body.appendChild(paragraph);
```

### 23. What is event handling?

Event handling means responding to user actions or browser events.

Examples:

- Click
- Mouseover
- Keypress
- Submit
- Change

Example:

```
const button = document.querySelector("button");

button.addEventListener("click", function() {
    alert("Button clicked!");
});
```

### 24. What is event bubbling?

Event bubbling means an event starts from the target element and moves upward through its parent elements.

Example:

```
document.querySelector("#child")
    .addEventListener("click", () => {
        console.log("Child clicked");
    });

document.querySelector("#parent")
    .addEventListener("click", () => {
        console.log("Parent clicked");
    });
```

If you click the child, both handlers execute: child first, then parent.

### 25. What is event capturing?

Event capturing is the opposite direction of event bubbling.

The event travels from the outermost ancestor toward the target element.

```
element.addEventListener("click", function() {
    console.log("Capturing");
}, true);
```

The third argument `true` enables capturing.

### 26. What is event delegation?

Event delegation means attaching a single event listener to a parent element instead of attaching separate listeners to multiple child elements.

It works using event bubbling.

Example:

```
document.querySelector("#parent")
    .addEventListener("click", function(event) {
        if (event.target.matches("button")) {
            console.log("Button clicked");
        }
    });
```

Advantages:

- Improves performance when handling many elements.
- Reduces event listeners.
- Works for dynamically added child elements.

### 27. Difference between synchronous and asynchronous JavaScript

| Synchronous                                  | Asynchronous                                                                       |
| -------------------------------------------- | ---------------------------------------------------------------------------------- |
| Executes one operation at a time in sequence | Allows operations to complete later                                                |
| Each operation waits for the previous one    | Does not block the main thread while waiting for supported asynchronous operations |
| Can block execution                          | Helps handle time-consuming operations                                             |

Example:

```
console.log("First");
console.log("Second");
console.log("Third");
```

Output:

```
First
Second
Third
```

Asynchronous example:

```
console.log("First");

setTimeout(() => {
    console.log("Second");
}, 1000);

console.log("Third");
```

Output:

```
First
Third
Second
```

### 28. What is a Promise?

A Promise is an object that represents the eventual success or failure of an asynchronous operation.

Example:

```
const promise = new Promise((resolve, reject) => {
    let success = true;

    if (success) {
        resolve("Data received");
    } else {
        reject("Something went wrong");
    }
});

promise
    .then(result => console.log(result))
    .catch(error => console.log(error));
```

### 29. What are the states of a Promise?

A Promise has three states:

1. Pending: Initial state; operation is not completed.
2. Fulfilled: Operation completed successfully.
3. Rejected: Operation failed.

Once fulfilled or rejected, a Promise is settled and its state cannot change again.

### 30. What is async/await?

Async/await is a modern way to handle asynchronous JavaScript code using Promise-based operations.

- `async` makes a function return a Promise.
- `await` waits for a Promise to settle and gives its fulfillment value or throws its rejection reason.

Example:

```
async function getData() {
    const response = await fetch(
        "https://jsonplaceholder.typicode.com/users"
    );

    const data = await response.json();

    console.log(data);
}

getData();
```

### 31. Difference between Promise and async/await

| Promise                                          | Async/await                          |
| ------------------------------------------------ | ------------------------------------ |
| Uses `.then()` and `.catch()`                    | Uses `await` and `try/catch`         |
| Can create Promise chains                        | Provides a sequential-looking syntax |
| Can become difficult to read with complex chains | Often easier to read                 |
| Fundamental asynchronous mechanism               | Syntax built on Promises             |

Important: Async/await does not replace Promises. It is built on top of them.

### 32. What is the Fetch API?

Fetch API is used to make HTTP requests and communicate with servers.

Example:

```
fetch("https://jsonplaceholder.typicode.com/users")
    .then(response => {
        if (!response.ok) {
            throw new Error("Request failed");
        }

        return response.json();
    })
    .then(data => console.log(data))
    .catch(error => console.log(error));
```

Common HTTP methods:

- GET – retrieve data.
- POST – create data.
- PUT – replace data.
- PATCH – partially update data.
- DELETE – delete data.

Remember: `fetch()` generally rejects for network errors, not simply because the server returns a 404 or 500 response. Check `response.ok`.

### 33. What is JSON?

JSON stands for JavaScript Object Notation.

It is a lightweight data format used to exchange information between clients and servers.

Example:

```
const user = {
    name: "John",
    age: 25
};

const jsonData = JSON.stringify(user);

const objectData = JSON.parse(jsonData);
```

Two important methods:

- `JSON.stringify()` converts a JavaScript value into a JSON string.
- `JSON.parse()` converts a valid JSON string into a JavaScript value.

### 34. What is destructuring?

Destructuring allows us to extract values from arrays or properties from objects into variables.

Array destructuring:

```
const numbers = [10, 20, 30];

const [a, b, c] = numbers;

console.log(a); // 10
console.log(b); // 20
```

Object destructuring:

```
const user = {
    name: "John",
    age: 25
};

const { name, age } = user;

console.log(name); // John
```

### 35. What are spread and rest operators?

Both use three dots (`...`), but their purposes are different.

Spread operator: Expands elements of an iterable or properties of an object.

```
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];

console.log(arr2); // [1, 2, 3, 4, 5]
```

Rest operator: Collects multiple values into a single array or object.

```
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(10, 20, 30)); // 60
```

### 36. What are template literals?

Template literals allow us to create strings using backticks.

They support:

- String interpolation.
- Multiline strings.
- Embedded expressions.

Example:

```
const name = "John";
const age = 25;

console.log(`My name is ${name} and I am ${age} years old.`);
```

### 37. What are array methods?

Array methods are built-in functions used to perform operations on arrays.

Common methods:

| Method       | Purpose                                    |
| ------------ | ------------------------------------------ |
| `push()`     | Adds an element at the end                 |
| `pop()`      | Removes the last element                   |
| `shift()`    | Removes the first element                  |
| `unshift()`  | Adds an element at the beginning           |
| `map()`      | Creates a transformed array                |
| `filter()`   | Creates an array of matching elements      |
| `reduce()`   | Reduces elements to one accumulated result |
| `find()`     | Returns the first matching element         |
| `includes()` | Checks whether a value exists              |
| `sort()`     | Sorts an array in place                    |
| `slice()`    | Returns a selected portion                 |
| `splice()`   | Adds/removes elements in place             |

### 38. Explain map(), filter(), and reduce().

These three are extremely important in JavaScript interviews.

map(): Transforms every element and returns a new array.

```
const numbers = [1, 2, 3, 4];

const result = numbers.map(num => num * 2);

console.log(result); // [2, 4, 6, 8]
```

filter(): Returns a new array containing elements that satisfy a condition.

```
const numbers = [1, 2, 3, 4, 5];

const result = numbers.filter(num => num > 2);

console.log(result); // [3, 4, 5]
```

reduce(): Processes array elements and accumulates a single result.

```
const numbers = [1, 2, 3, 4];

const result = numbers.reduce(
    (total, num) => total + num, 0
);

console.log(result); // 10
```

### 39. Difference between forEach() and map()

| forEach()                              | map()                                  |
| -------------------------------------- | -------------------------------------- |
| Iterates through array elements        | Transforms array elements              |
| Returns `undefined`                    | Returns a new array                    |
| Used for side effects                  | Used to create transformed arrays      |
| Does not support breaking with `break` | Does not support breaking with `break` |

Example:

```
const numbers = [1, 2, 3];

const a = numbers.forEach(num => num * 2);
const b = numbers.map(num => num * 2);

console.log(a); // undefined
console.log(b); // [2, 4, 6]
```

### 40. Difference between find() and filter()

| find()                          | filter()                      |
| ------------------------------- | ----------------------------- |
| Returns first matching element  | Returns all matching elements |
| Returns an element or undefined | Returns an array              |
| Stops after first match         | Checks all elements           |

Example:

```
const numbers = [10, 20, 30, 40];

console.log(numbers.find(n => n > 20));
// 30

console.log(numbers.filter(n => n > 20));
// [30, 40]
```

### 41. Difference between slice() and splice()

| slice()                        | splice()                            |
| ------------------------------ | ----------------------------------- |
| Does not modify original array | Modifies original array             |
| Extracts elements              | Adds, removes, or replaces elements |
| Returns a shallow copy         | Returns removed elements            |

Example:

```
const arr = [10, 20, 30, 40];

console.log(arr.slice(1, 3));
// [20, 30]

console.log(arr);
// [10, 20, 30, 40]
```

Splice example:

```
const arr = [10, 20, 30, 40];

arr.splice(1, 2);

console.log(arr);
// [10, 40]
```

### 42. What is optional chaining?

Optional chaining (`?.`) allows us to safely access nested properties without throwing an error when an intermediate value is `null` or `undefined`.

```
const user = {
    name: "John",
    address: {
        city: "Chennai"
    }
};

console.log(user.address?.city); // Chennai
console.log(user.company?.name); // undefined
```

### 43. What is the ternary operator?

The ternary operator is a shorter alternative to an `if-else` statement.

Syntax:

```
condition ? expression1 : expression2;
```

Example:

```
const age = 20;

const result = age >= 18 ? "Adult" : "Minor";

console.log(result); // Adult
```

### 44. Difference between shallow copy and deep copy

Shallow copy: Copies the outer object, but nested objects are still shared by reference.

```
const original = {
    name: "John",
    address: {
        city: "Chennai"
    }
};

const copy = { ...original };

copy.address.city = "Bangalore";

console.log(original.address.city);
// Bangalore
```

Deep copy: Copies nested data so that changes to the copied nested objects do not affect the original.

```
const original = {
    name: "John",
    address: {
        city: "Chennai"
    }
};

const copy = structuredClone(original);

copy.address.city = "Bangalore";

console.log(original.address.city);
// Chennai
```

Note: `structuredClone()` supports many built-in data types, but not every JavaScript value, such as functions.

### 45. What are ES6 features?

ES6 (ECMAScript 2015) introduced many important JavaScript features.

Common features:

1. `let` and `const`
2. Arrow functions
3. Template literals
4. Destructuring
5. Spread and rest operators
6. Classes
7. Promises
8. Modules (`import` and `export`)
9. Default parameters
10. Enhanced object literals
11. Iterators and generators
12. Maps and Sets

## Part 3: Advanced JavaScript (Questions 46–60)

### 46. What is the event loop?

The event loop is a mechanism that coordinates synchronous and asynchronous JavaScript execution.

It checks whether the call stack is empty and then schedules queued callbacks for execution.

Example:

```
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

```
Start
End
Promise
Timeout
```

Why?

1. Synchronous code executes first.
2. Promise callbacks go into the microtask queue.
3. Timer callbacks go into the task (callback) queue.
4. Microtasks are processed before the next task.

### 47. What is the call stack?

The call stack is a data structure that tracks function execution.

It follows the LIFO principle: Last In, First Out.

Example:

```
function first() {
    second();
}

function second() {
    console.log("Hello");
}

first();
```

Execution:

1. `first()` enters the stack.
2. `second()` enters the stack.
3. `console.log()` executes.
4. `second()` is removed.
5. `first()` is removed.

### 48. What is the callback queue?

The callback queue, also called the task queue, stores callbacks from tasks such as timers and certain browser events until the call stack is available.

Example:

```
setTimeout(() => {
    console.log("Hello");
}, 1000);
```

After the timer expires, its callback becomes eligible to run as a task.

### 49. What is the microtask queue?

The microtask queue stores high-priority asynchronous callbacks.

Examples:

- Promise `.then()`
- Promise `.catch()`
- Promise `.finally()`
- `queueMicrotask()`
- MutationObserver callbacks in browsers

Microtasks are processed after the current synchronous execution finishes and before the next task begins.

Example:

```
console.log("A");

setTimeout(() => console.log("B"), 0);

Promise.resolve().then(() => console.log("C"));

console.log("D");
```

Output:

```
A
D
C
B
```

### 50. What is lexical scope?

Lexical scope means that variable accessibility is determined by where functions and blocks are written in the source code.

Example:

```
function outer() {
    let name = "John";

    function inner() {
        console.log(name);
    }

    inner();
}

outer(); // John
```

The inner function can access variables from its outer scope.

### 51. What is the this keyword?

`this` refers to a value determined by how a function is called.

Example:

```
const user = {
    name: "John",

    greet() {
        console.log(this.name);
    }
};

user.greet(); // John
```

In this example, `this` refers to the `user` object.

Important cases:

- Object method: usually the object before the dot.
- Regular function: depends on how it is called.
- Arrow function: inherits `this` from its surrounding lexical scope.
- Constructor called with `new`: refers to the newly created instance.

### 52. What is prototypal inheritance?

Prototypal inheritance is a mechanism through which JavaScript objects can inherit properties and methods from other objects.

Example:

```
const person = {
    greet() {
        console.log("Hello");
    }
};

const user = Object.create(person);

user.name = "John";

user.greet(); // Hello
```

Here, `user` inherits the `greet()` method from `person`.

### 53. Difference between call(), apply(), and bind()

All three methods are used to control the `this` value of a function.

| Method    | Description                                             |
| --------- | ------------------------------------------------------- |
| `call()`  | Calls a function immediately with arguments separately  |
| `apply()` | Calls a function immediately with arguments as an array |
| `bind()`  | Returns a new function with `this` bound                |

Example:

```
const person = {
    name: "John"
};

function greet(city, country) {
    console.log(
        `Hello ${this.name} from ${city}, ${country}`
    );
}

greet.call(person, "Chennai", "India");

greet.apply(person, ["Chennai", "India"]);

const newFunction = greet.bind(
    person,
    "Chennai",
    "India"
);

newFunction();
```

### 54. What is debouncing?

Debouncing ensures that a function executes only after a specified amount of time has passed since the last call.

It is useful in search boxes and autocomplete functionality.

Example:

```
function debounce(func, delay) {
    let timer;

    return function(...args) {
        clearTimeout(timer);

        timer = setTimeout(() => {
            func.apply(this, args);
        }, delay);
    };
}

const search = debounce((value) => {
    console.log("Searching:", value);
}, 500);
```

If the user keeps typing, the function waits until typing stops for 500 milliseconds.

### 55. What is throttling?

Throttling ensures that a function executes at most once during a specified time interval.

It is useful for scroll and resize events.

Example:

```
function throttle(func, delay) {
    let lastCall = 0;

    return function(...args) {
        const now = Date.now();

        if (now - lastCall >= delay) {
            lastCall = now;
            func.apply(this, args);
        }
    };
}

const handleScroll = throttle(() => {
    console.log("Scrolling");
}, 1000);
```

Debouncing vs throttling:

- Debouncing: Executes after repeated calls stop.
- Throttling: Limits how frequently a function executes.

### 56. What is memory management in JavaScript?

Memory management is the process of allocating, using, and releasing memory.

JavaScript automatically manages memory.

The main stages are:

1. Memory allocation.
2. Memory usage.
3. Memory cleanup through garbage collection.

Example:

```
let user = {
    name: "John"
};

user = null;
```

The original object may become eligible for garbage collection if no reachable references remain.

### 57. What is garbage collection?

Garbage collection is the automatic process of identifying and reclaiming memory that is no longer reachable.

JavaScript engines commonly use a mark-and-sweep approach.

Example of a memory leak:

```
let users = [];

function addUser() {
    users.push({
        name: "John"
    });
}
```

If this keeps adding objects without removing them, memory usage can grow unnecessarily.

Common causes of memory leaks:

- Unremoved event listeners.
- Unnecessary global variables.
- Timers that are never cleared.
- Unintended references to unused objects.

### 58. What are modules in JavaScript?

Modules allow us to split JavaScript code into separate files and reuse functionality.

They improve code organization and maintainability.

Export:

```
// math.js

export function add(a, b) {
    return a + b;
}
```

Import:

```
// app.js

import { add } from "./math.js";

console.log(add(10, 20));
```

### 59. Difference between CommonJS and ES modules

| CommonJS                                      | ES modules                                  |
| --------------------------------------------- | ------------------------------------------- |
| Uses `require()`                              | Uses `import`                               |
| Uses `module.exports`                         | Uses `export`                               |
| Traditionally common in Node.js               | Standard JavaScript module system           |
| Loads modules synchronously in typical usage  | Supports static imports and dynamic imports |
| CommonJS exports are based on runtime loading | ES imports are statically analyzable        |

Example:

CommonJS:

```
const math = require("./math");

module.exports = math;
```

ES modules:

```
import { add } from "./math.js";

export { add };
```

### 60. How do you handle errors in JavaScript?

We can handle errors using `try`, `catch`, `finally`, and `throw`.

Example:

```
try {
    let result = 10 / 0;

    throw new Error("Something went wrong");

} catch (error) {
    console.log(error.message);

} finally {
    console.log("Execution completed");
}
```

- `try`: Contains code that might throw an error.
- `catch`: Handles the error.
- `finally`: Executes whether an error occurs or not.
- `throw`: Creates or throws an error.

With async/await:

```
async function getData() {
    try {
        const response = await fetch("/api/users");

        if (!response.ok) {
            throw new Error("API request failed");
        }

        const data = await response.json();

        console.log(data);

    } catch (error) {
        console.log(error.message);
    }
}
```

# Part 4: TypeScript Interview Questions (20 Questions)

### 1. What is TypeScript?

TypeScript is a strongly typed programming language built on top of JavaScript and developed by Microsoft.

It adds static type checking and additional development features to JavaScript.

TypeScript code is compiled into JavaScript.

Example:

```
let name: string = "John";
let age: number = 25;

console.log(name, age);
```

### 2. Difference between JavaScript and TypeScript

| JavaScript                                 | TypeScript                                        |
| ------------------------------------------ | ------------------------------------------------- |
| Dynamically typed                          | Supports static type checking                     |
| Uses `.js` files                           | Uses `.ts` files                                  |
| Type errors often appear at runtime        | Many type errors are detected during development  |
| No built-in static type system             | Provides a static type system                     |
| Runs directly in supported JS environments | Must be transformed into JavaScript for execution |

### 3. Why do we use TypeScript?

Advantages:

1. Detects many errors during development.
2. Improves code readability.
3. Provides better IDE support.
4. Supports autocomplete.
5. Makes large applications easier to maintain.
6. Supports interfaces and generics.
7. Improves collaboration in development teams.

### 4. What are static and dynamic typing?

Static typing: Types are checked during development/compilation.

```
let age: number = 25;

// age = "John"; // Type error
```

Dynamic typing: Types are determined at runtime.

```
let age = 25;

age = "John"; // Allowed
```

### 5. What are type annotations?

Type annotations explicitly specify the type of a variable, parameter, or return value.

```
let name: string = "John";

let age: number = 25;

function add(a: number, b: number): number {
    return a + b;
}
```

### 6. What is type inference?

Type inference means TypeScript automatically determines the type based on the assigned value.

```
let name = "John";

let age = 25;
```

TypeScript understands that `name` is a string and `age` is a number.

### 7. What are interfaces?

An interface defines the structure or shape of an object.

Example:

```
interface User {
    name: string;
    age: number;
    email: string;
}

const user: User = {
    name: "John",
    age: 25,
    email: "john@gmail.com"
};
```

Interfaces help maintain consistent object structures.

### 8. What are type aliases?

A type alias allows us to create a custom name for a type.

Example:

```
type User = {
    name: string;
    age: number;
};

const user: User = {
    name: "John",
    age: 25
};
```

### 9. Difference between interface and type

| Interface                          | Type                                             |
| ---------------------------------- | ------------------------------------------------ |
| Defines object shapes              | Defines many kinds of types                      |
| Supports declaration merging       | Cannot be reopened through declaration merging   |
| Uses `extends` for inheritance     | Uses intersections (`&`) for composition         |
| Commonly used for object contracts | Used for unions, primitives, tuples, and objects |

Example:

```
interface Person {
    name: string;
}

interface Employee extends Person {
    salary: number;
}
```

Using type:

```
type Person = {
    name: string;
};

type Employee = Person & {
    salary: number;
};
```

### 10. What are union types?

Union types allow a variable to accept multiple possible types.

Example:

```
let value: string | number;

value = "Hello";
value = 100;
```

The `|` symbol represents a union.

### 11. What are intersection types?

Intersection types combine multiple types into one.

Example:

```
type Person = {
    name: string;
};

type Employee = {
    salary: number;
};

type Staff = Person & Employee;

const user: Staff = {
    name: "John",
    salary: 30000
};
```

The `&` symbol represents an intersection.

### 12. What are optional properties?

Optional properties are properties that may or may not be present in an object.

We use `?` to define them.

```
interface User {
    name: string;
    age?: number;
}

const user: User = {
    name: "John"
};
```

Here, `age` is optional.

### 13. What is an enum?

An enum is a TypeScript feature used to define a set of named constants.

Example:

```
enum Direction {
    Up,
    Down,
    Left,
    Right
}

let direction: Direction = Direction.Up;
```

By default, numeric enum values start at zero.

String enum example:

```
enum Status {
    Success = "SUCCESS",
    Failed = "FAILED",
    Pending = "PENDING"
}
```

### 14. What are generics?

Generics allow us to create reusable components, functions, and types that work with different data types while maintaining type safety.

Example:

```
function identity<T>(value: T): T {
    return value;
}

console.log(identity<string>("Hello"));
console.log(identity<number>(100));
```

Here, `T` represents a type parameter.

Another example:

```
function getFirst<T>(items: T[]): T | undefined {
    return items[0];
}

console.log(getFirst([10, 20, 30]));
console.log(getFirst(["A", "B", "C"]));
```

### 15. What is the any type?

The `any` type disables most TypeScript type checking for that value.

Example:

```
let value: any = 10;

value = "Hello";
value = true;
```

It allows any type of value.

Interview tip: Avoid using `any` unnecessarily because it removes many benefits of TypeScript.

### 16. Difference between any and unknown

| any                                        | unknown                                                                  |
| ------------------------------------------ | ------------------------------------------------------------------------ |
| Allows any operation without type checking | Requires type checking before most operations                            |
| Less type-safe                             | More type-safe                                                           |
| Can assign to other types freely           | Cannot assign directly to a specific type without narrowing or assertion |

Example:

```
let a: any = "Hello";

console.log(a.toUpperCase()); // Allowed
```

Using unknown:

```
let b: unknown = "Hello";

if (typeof b === "string") {
    console.log(b.toUpperCase());
}
```

### 17. What is type narrowing?

Type narrowing means reducing a variable's possible types using conditions or type guards.

Example:

```
function printValue(value: string | number) {
    if (typeof value === "string") {
        console.log(value.toUpperCase());
    } else {
        console.log(value.toFixed(2));
    }
}
```

Here, TypeScript identifies the correct type inside each condition.

Common narrowing techniques:

- `typeof`
- `instanceof`
- `in`
- Equality checks
- Custom type guard functions

### 18. What is the never type?

The `never` type represents values that never occur.

It is commonly used for functions that never return normally, such as functions that always throw an error or run indefinitely.

Example:

```
function throwError(message: string): never {
    throw new Error(message);
}
```

Another example:

```
function infiniteLoop(): never {
    while (true) {
        // Never exits
    }
}
```

### 19. What are access modifiers?

Access modifiers control the visibility of class properties and methods.

TypeScript provides three common access modifiers:

Public: Accessible from anywhere. It is the default.

Private: Accessible only within the declaring class.

Protected: Accessible within the declaring class and its subclasses.

Example:

```
class Person {
    public name: string;

    private age: number;

    protected salary: number;

    constructor(name: string, age: number, salary: number) {
        this.name = name;
        this.age = age;
        this.salary = salary;
    }
}

const person = new Person("John", 25, 30000);

console.log(person.name); // Allowed
// console.log(person.age); // Error
```

### 20. How do you use TypeScript with React?

TypeScript can be used with React to provide type safety for components, props, state, and event handlers.

Example: React component with props

```
interface UserProps {
    name: string;
    age: number;
}

function User({ name, age }: UserProps) {
    return (
        <div>
            <h2>{name}</h2>
            <p>{age}</p>
        </div>
    );
}

export default User;
```

Example: useState with TypeScript

```
import { useState } from "react";

function Counter() {
    const [count, setCount] = useState<number>(0);

    return (
        <button onClick={() => setCount(count + 1)}>
            Count: {count}
        </button>
    );
}

export default Counter;
```

Example: Event handling

```
function handleChange(
    event: React.ChangeEvent<HTMLInputElement>
) {
    console.log(event.target.value);
}
```

Benefits:

- Better type safety.
- Fewer runtime errors caused by type mismatches.
- Better autocomplete.
- Easier maintenance.
- Clear component contracts.

# Part 5: Most important interview topics to revise

If you have limited preparation time, prioritize these topics. Interviewers frequently use them to check whether you understand JavaScript beyond definitions.

## JavaScript priority checklist

Your revision progress

0/12 completed

var vs let vs const

\== vs ===

Hoisting and Temporal Dead Zone

Scope and closures

Callbacks and higher-order functions

map(), filter(), reduce()

Promises and async/await

Event loop and microtask queue

this keyword and arrow functions

call(), apply(), bind()

Debouncing and throttling

Shallow copy vs deep copy

## TypeScript priority checklist

Your revision progress

0/10 completed

Interface vs type

any vs unknown

Union vs intersection

Generics

Type inference

Type narrowing

Optional properties

never type

Access modifiers

TypeScript with React

# Part 6: JavaScript coding questions to practice

Knowing definitions is not enough. Interviewers may ask you to write code without using built-in shortcuts.

Try these questions:

| No. | Coding question                     | Concept   |
| --- | ----------------------------------- | --------- |
| 1   | Reverse a string                    | Strings   |
| 2   | Check palindrome                    | Strings   |
| 3   | Find the largest number in an array | Arrays    |
| 4   | Find the second-largest number      | Arrays    |
| 5   | Remove duplicates from an array     | Set       |
| 6   | Find even and odd numbers           | Filter    |
| 7   | Find the frequency of characters    | Objects   |
| 8   | Find the sum of array elements      | Reduce    |
| 9   | Find missing number in an array     | Logic     |
| 10  | Flatten a nested array              | Recursion |
| 11  | Find duplicate elements             | Arrays    |
| 12  | Sort an array without sort()        | Sorting   |

Example coding question:

Reverse a string without using reverse().

```
function reverseString(str) {
    let result = "";

    for (let i = str.length - 1; i >= 0; i--) {
        result += str[i];
    }

    return result;
}

console.log(reverseString("hello"));
// olleh
```

# Part 7: A 7-day interview preparation plan

| Day   | Topics                                   |
| ----- | ---------------------------------------- |
| Day 1 | JavaScript basics (1–20)                 |
| Day 2 | DOM, events and arrays                   |
| Day 3 | Promises, async/await and Fetch          |
| Day 4 | Event loop, closures, `this`, prototypes |
| Day 5 | TypeScript fundamentals (1–13)           |
| Day 6 | TypeScript advanced topics and React     |
| Day 7 | Coding practice and mock interview       |

My recommendation: Spend 40% of your preparation time understanding concepts, 40% writing code, and 20% answering questions aloud.

# Part 8: Let's practice with a mock interview

I can act as your technical interviewer. I'll ask one question at a time, wait for your answer, evaluate it, correct mistakes, and give you an ideal interview answer.

## Choose your interview practice

1\. Your preparation level

Beginner – Basic JavaScript

Intermediate – JavaScript and DOM

Advanced – JavaScript concepts

TypeScript and React

Full interview – Mixed questions

2\. Practice style

One question at a time (recommended)

Rapid-fire interview

Practical coding interview

Start mock interview&#x20;

One question before we begin: Are you preparing for a fresher interview or an experienced developer interview? This will help me adjust the difficulty and expected answers.