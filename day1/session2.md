# Day 1 – Session 2: JavaScript Fundamentals for Interviews

High-priority interview preparation

This session covers the core JavaScript concepts you need for a Junior Full Stack Developer interview.

We'll learn each topic in this format:

1. Simple explanation.
2. Syntax and code examples.
3. Real-world application.
4. Common interview questions.
5. Coding exercises.

Today's learning roadmap

# 12 Topics

1\. Variables

2\. Data types

3\. Operators

4\. Functions

5\. Arrays and objects

6\. Scope and hoisting

7\. Closures

8\. Callbacks

9\. Promises

10\. Async/await

11\. Array methods

12\. Destructuring and spread

Suggested duration: 4–5 hours including coding practice.

# 1. Variables: var, let and const

### What is a variable?

A variable is a container used to store data in JavaScript.

Example:

```
let name = "Mohideen";
let age = 27;

console.log(name);
console.log(age);
```

Output:

```
Mohideen
27
```

### Three ways to declare variables

JavaScript provides three main variable declaration keywords:

- `var`
- `let`
- `const`

### A. var

`var` is the older way of declaring variables.

```
var name = "Mohideen";

var name = "John";

console.log(name);
```

Output:

```
John
```

Features:

- Function scoped.
- Can be redeclared.
- Can be reassigned.
- Can be accessed before declaration due to hoisting, with value `undefined`.

### B. let

`let` is used when the variable value needs to change.

```
let age = 25;

age = 30;

console.log(age);
```

Output:

```
30
```

Features:

- Block scoped.
- Cannot be redeclared in the same scope.
- Can be reassigned.
- Hoisted but inaccessible before initialization.

### C. const

`const` is used when a variable should not be reassigned.

```
const country = "India";

console.log(country);
```

This is not allowed:

```
const age = 25;

age = 30; // Error
```

Features:

- Block scoped.
- Cannot be redeclared in the same scope.
- Cannot be reassigned.
- Must be initialized when declared.

Important interview trick:

```
const user = {
    name: "Mohideen",
    age: 25
};

user.age = 30;

console.log(user.age);
```

Output:

```
30
```

Why? Because `const` prevents reassignment of the variable binding, not modification of the object it references.

### var vs let vs const

| Feature                 | var      | let   | const |
| ----------------------- | -------- | ----- | ----- |
| Scope                   | Function | Block | Block |
| Redeclaration           | Yes      | No    | No    |
| Reassignment            | Yes      | Yes   | No    |
| Initialization required | No       | No    | Yes   |
| Hoisting                | Yes      | Yes   | Yes   |

Interview answer: Which should you use?

Prefer `const` by default. Use `let` when reassignment is required. Avoid `var` in modern JavaScript unless working with legacy code.

### Interview questions

1. What is a variable?
2. What is the difference between var, let and const?
3. Can we redeclare a let variable?
4. Can we change a const object?
5. What is block scope?
6. Why is let preferred over var?
7. Can we declare a variable without initializing it?
8. What happens if we access a const variable before declaration?

# 2. JavaScript Data Types

A data type determines what kind of value a variable stores.

JavaScript has two broad categories:

1. Primitive data types.
2. Non-primitive (reference) types.

### A. Primitive data types

There are seven primitive types.

| Data type | Example         |
| --------- | --------------- |
| String    | `"Hello"`       |
| Number    | `100`, `10.5`   |
| Boolean   | `true`, `false` |
| Undefined | `let x;`        |
| Null      | `let x = null;` |
| BigInt    | `123456789n`    |
| Symbol    | `Symbol("id")`  |

Examples:

```
let name = "Mohideen";
let age = 27;
let isDeveloper = true;
let salary;
let address = null;
let largeNumber = 123456789n;
let id = Symbol("userId");
```

### B. Non-primitive data types

Objects are reference types. Arrays and functions are also objects in JavaScript.

```
let user = {
    name: "Mohideen",
    age: 27
};

let skills = ["HTML", "CSS", "JavaScript"];

function greet() {
    console.log("Hello");
}
```

### typeof operator

Used to identify the type of a value.

```
console.log(typeof "Hello");
console.log(typeof 100);
console.log(typeof true);
console.log(typeof undefined);
console.log(typeof {});
console.log(typeof []);
console.log(typeof null);
```

Output:

```
string
number
boolean
undefined
object
object
object
```

Important interview trick: `typeof null` returns `"object"` due to a historical JavaScript behavior.

To check whether something is an array:

```
console.log(Array.isArray([])); // true
```

### Primitive vs reference types

| Primitive                 | Reference                               |
| ------------------------- | --------------------------------------- |
| Stores the value directly | Variables hold a reference to an object |
| Immutable values          | Objects can be modified                 |
| Copied by value           | Reference is copied                     |
| Example: string           | Example: object                         |

Example:

```
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20
```

Reference example:

```
let user1 = { name: "John" };
let user2 = user1;

user2.name = "David";

console.log(user1.name); // David
```

### Interview questions

1. What are JavaScript data types?
2. How many primitive data types are there?
3. What is the difference between null and undefined?
4. What is the difference between primitive and reference types?
5. What is the typeof operator?
6. Why does typeof null return object?
7. How do you check whether a variable is an array?
8. Is an array a primitive or reference type?

# 3. JavaScript Operators

Operators perform operations on values and variables.

### A. Arithmetic operators

```
let a = 10;
let b = 5;

console.log(a + b); // 15
console.log(a - b); // 5
console.log(a * b); // 50
console.log(a / b); // 2
console.log(a % b); // 0
console.log(a ** b); // 100000
```

| Operator | Meaning        |
| -------- | -------------- |
| `+`      | Addition       |
| `-`      | Subtraction    |
| `*`      | Multiplication |
| `/`      | Division       |
| `%`      | Remainder      |
| `**`     | Exponentiation |
| `++`     | Increment      |
| `--`     | Decrement      |

### B. Comparison operators

```
console.log(10 > 5);   // true
console.log(10 < 5);   // false
console.log(10 >= 10); // true
console.log(10 === 10); // true
console.log(10 !== 5); // true
```

### Important: == vs ===

`==` compares values after type coercion where applicable.

`===` compares without type coercion.

```
console.log(5 == "5");  // true
console.log(5 === "5"); // false
```

Prefer `===` in most application code.

### C. Logical operators

```
let age = 25;
let hasId = true;

console.log(age >= 18 && hasId); // true
console.log(age < 18 || hasId);  // true
console.log(!hasId);             // false
```

\| Operator | Meaning |\
\|---|---|\
\| `&&` | AND |\
\| `||` | OR |\
\| `!` | NOT |

### D. Assignment operators

```
let x = 10;

x += 5; // 15
x -= 2; // 13
x *= 2; // 26
x /= 2; // 13
```

### E. Ternary operator

A shorter way to write conditional expressions.

```
let age = 20;

let result = age >= 18 ? "Eligible" : "Not Eligible";

console.log(result);
```

### F. Nullish coalescing operator

Returns the right-hand value only when the left-hand value is null or undefined.

```
let username = null;

console.log(username ?? "Guest"); // Guest
```

Difference between `||` and `??`:

```
console.log(0 || 100); // 100
console.log(0 ?? 100); // 0
```

### Interview questions

1. What are operators in JavaScript?
2. What is the difference between == and ===?
3. What are logical operators?
4. What is the ternary operator?
5. What is the difference between || and ???
6. What is the modulus operator?
7. What is the difference between ++a and a++?
8. What is type coercion?

# 4. Functions and Arrow Functions

### What is a function?

A function is a reusable block of code that performs a specific task.

Example:

```
function greet() {
    console.log("Hello Mohideen");
}

greet();
```

Output:

```
Hello Mohideen
```

### A. Function with parameters

```
function add(a, b) {
    return a + b;
}

console.log(add(10, 20));
```

Output:

```
30
```

Here:

- `a` and `b` are parameters.
- `10` and `20` are arguments.
- `return` sends the result back.

### B. Function expression

A function can be assigned to a variable.

```
const greet = function() {
    console.log("Hello");
};

greet();
```

### C. Arrow function

Introduced in ES6.

```
const greet = () => {
    console.log("Hello Mohideen");
};

greet();
```

Shorter version:

```
const add = (a, b) => a + b;

console.log(add(10, 20));
```

Output:

```
30
```

### D. Types of functions

No parameters, no return value

```
function greet() {
    console.log("Hello");
}
```

Parameters and return value

```
function multiply(a, b) {
    return a * b;
}
```

Default parameters

```
function greet(name = "Guest") {
    console.log("Hello " + name);
}

greet();
```

Output: `Hello Guest`

### Function declaration vs arrow function

| Function declaration                       | Arrow function                                                    |
| ------------------------------------------ | ----------------------------------------------------------------- |
| Uses `function` keyword                    | Uses `=>`                                                         |
| Has its own `this` depending on invocation | Inherits `this` lexically                                         |
| Can be called before declaration           | Cannot access a const/let function variable before initialization |
| Can be used as a constructor               | Cannot be used with `new`                                         |

Important: Arrow functions do not have their own `this`, `arguments`, or `prototype`.

### Interview questions

1. What is a function?
2. What is the difference between parameters and arguments?
3. What is a return statement?
4. What is a function declaration?
5. What is a function expression?
6. What is an arrow function?
7. What is the difference between normal and arrow functions?
8. What are default parameters?
9. What is an anonymous function?
10. What is a callback function?

# 5. Arrays and Objects

These are among the most important concepts in React development.

## A. Arrays

An array stores multiple values in a single variable.

```
let skills = ["HTML", "CSS", "JavaScript", "React"];

console.log(skills[0]); // HTML
console.log(skills[1]); // CSS
```

Array indexing starts from zero.

### Common array methods

```
let numbers = [10, 20, 30];

numbers.push(40);    // Add at end
numbers.pop();       // Remove from end
numbers.unshift(5);  // Add at beginning
numbers.shift();     // Remove from beginning

console.log(numbers);
```

Other important methods:

| Method        | Purpose                                 |
| ------------- | --------------------------------------- |
| `includes()`  | Checks whether an element exists        |
| `indexOf()`   | Returns element index                   |
| `find()`      | Returns first matching element          |
| `findIndex()` | Returns first matching index            |
| `slice()`     | Returns a selected portion              |
| `splice()`    | Adds/removes elements in original array |
| `sort()`      | Sorts elements                          |
| `reverse()`   | Reverses array                          |
| `join()`      | Converts array into a string            |

## B. Objects

An object stores data in key-value pairs.

```
const employee = {
    name: "Mohideen",
    age: 27,
    role: "Full Stack Developer",
    skills: ["React", "Python", "Django"]
};

console.log(employee.name);
console.log(employee.role);
console.log(employee.skills);
```

### Adding and updating properties

```
employee.city = "Chennai";

employee.age = 28;

console.log(employee);
```

### Deleting properties

```
delete employee.city;
```

### Object methods

```
const user = {
    name: "John",

    greet: function() {
        console.log("Hello " + this.name);
    }
};

user.greet();
```

### Real-world example from ShopSphere

Suppose your e-commerce application has products:

```
const products = [
    {
        id: 1,
        name: "Laptop",
        price: 50000,
        category: "Electronics"
    },
    {
        id: 2,
        name: "Mobile",
        price: 20000,
        category: "Electronics"
    }
];

console.log(products[0].name); // Laptop
console.log(products[1].price); // 20000
```

This structure is very common when receiving JSON data from REST APIs.

### Interview questions

1. What is an array?
2. What is an object?
3. What is the difference between arrays and objects?
4. How do you add elements to an array?
5. What is the difference between push and pop?
6. What is the difference between slice and splice?
7. How do you access object properties?
8. What is a nested object?
9. Can an object contain an array?
10. How do you iterate through an array of objects?

# 6. Scope and Hoisting

These two concepts are frequently asked in JavaScript technical interviews.

## A. What is scope?

Scope determines where a variable can be accessed in JavaScript.

There are three important types.

### 1. Global scope

A variable declared outside functions and blocks can generally be accessed throughout its accessible script/module scope.

```
let name = "Mohideen";

function greet() {
    console.log(name);
}

greet();

console.log(name);
```

Output:

```
Mohideen
Mohideen
```

### 2. Function scope

Variables declared using `var` inside a function are accessible within that function.

```
function test() {
    var age = 25;

    console.log(age);
}

test();

// console.log(age); // ReferenceError
```

### 3. Block scope

Variables declared using `let` and `const` inside `{}` are accessible only inside that block.

```
if (true) {
    let age = 25;
    const name = "Mohideen";

    console.log(age);
}

// console.log(age); // ReferenceError
```

### Scope comparison

| Scope    | var | let | const |
| -------- | --- | --- | ----- |
| Global   | Yes | Yes | Yes   |
| Function | Yes | Yes | Yes   |
| Block    | No  | Yes | Yes   |

Note: Global declarations have some differences between browser scripts and JavaScript modules.

## B. What is hoisting?

Hoisting is JavaScript's behavior of processing declarations before executing code in their scope.

### Example 1: var hoisting

```
console.log(a);

var a = 10;
```

Output:

```
undefined
```

Conceptually, this behaves like:

```
var a;

console.log(a);

a = 10;
```

### Example 2: let hoisting

```
console.log(a);

let a = 10;
```

Output:

```
ReferenceError
```

Why?

`let` is hoisted but remains inaccessible in the Temporal Dead Zone (TDZ) until initialization.

### Example 3: const hoisting

```
console.log(name);

const name = "Mohideen";
```

Output: `ReferenceError`

### Function hoisting

Function declarations can be called before their declaration.

```
greet();

function greet() {
    console.log("Hello");
}
```

Output:

```
Hello
```

But this does not work:

```
greet();

const greet = () => {
    console.log("Hello");
};
```

It throws a ReferenceError because the `greet` variable is in its TDZ.

### Interview questions

1. What is scope in JavaScript?
2. What are the different types of scope?
3. What is global scope?
4. What is function scope?
5. What is block scope?
6. What is hoisting?
7. How does hoisting work with var?
8. How does hoisting work with let and const?
9. What is the Temporal Dead Zone?
10. Are function declarations hoisted?

# 7. Closures

Frequently asked interview topic

### What is a closure?

A closure is created when an inner function remembers and accesses variables from its outer function's lexical scope, even after the outer function has finished executing.

Let's understand with a simple example.

```
function outer() {
    let count = 0;

    function inner() {
        count++;
        console.log(count);
    }

    return inner;
}

const counter = outer();

counter();
counter();
counter();
```

Output:

```
1
2
3
```

### How does this work?

Step 1: The `outer()` function executes.

Step 2: It creates a variable called `count`.

Step 3: It returns the `inner()` function.

Step 4: The inner function remembers the `count` variable.

Step 5: Every time we call `counter()`, the same remembered variable is updated.

This is a closure.

### Real-world application

Closures are useful for:

- Data privacy.
- Maintaining state.
- Creating counters.
- Function factories.
- Event handlers.

Example of data privacy:

```
function bankAccount() {
    let balance = 1000;

    return {
        deposit: function(amount) {
            balance += amount;
        },

        getBalance: function() {
            return balance;
        }
    };
}

const account = bankAccount();

account.deposit(500);

console.log(account.getBalance()); // 1500
```

Here, the `balance` variable cannot be directly accessed from outside the function.

### Interview questions

1. What is a closure?
2. Why do we use closures?
3. What is lexical scope?
4. Can an inner function access outer function variables?
5. What happens to outer variables after the outer function finishes?
6. How do closures help with data privacy?
7. Give a real-world example of closures.
8. What is the difference between closure and scope?

Interview-ready answer:

"A closure is a function that remembers the variables from its outer lexical scope, even after the outer function has completed execution. It is useful for maintaining state and data privacy."

# 8. Callback Functions

### What is a callback function?

A callback is a function passed as an argument to another function and executed by that function.

Example:

```
function greet(name) {
    console.log("Hello " + name);
}

function processUser(callback) {
    let username = "Mohideen";

    callback(username);
}

processUser(greet);
```

Output:

```
Hello Mohideen
```

Explanation:

1. `greet` is a function.
2. We pass it as an argument to `processUser`.
3. `processUser` calls the callback.
4. The username is passed to `greet`.

### Callback with arrow functions

```
function calculate(a, b, callback) {
    let result = a + b;

    callback(result);
}

calculate(10, 20, (value) => {
    console.log(value);
});
```

Output:

```
30
```

### Synchronous callback

```
function first(callback) {
    console.log("First");

    callback();
}

first(() => {
    console.log("Second");
});
```

Output:

```
First
Second
```

### Asynchronous callback

```
console.log("Start");

setTimeout(() => {
    console.log("Inside callback");
}, 2000);

console.log("End");
```

Output:

```
Start
End
Inside callback
```

The callback executes after approximately two seconds.

### What is callback hell?

Callback hell occurs when multiple nested callbacks make code difficult to read and maintain.

Example:

```
getUser(function(user) {
    getOrders(user.id, function(orders) {
        getPayment(orders, function(payment) {
            console.log(payment);
        });
    });
});
```

Promises and async/await help manage this complexity.

### Interview questions

1. What is a callback function?
2. Why do we use callbacks?
3. What is the difference between synchronous and asynchronous callbacks?
4. What is callback hell?
5. How can we avoid callback hell?
6. Can we pass an arrow function as a callback?
7. Is every callback asynchronous?

Important interview point: No. A callback can be synchronous or asynchronous.

# 9. Promises

Very important

### What is a Promise?

A Promise is a JavaScript object that represents the eventual success or failure of an asynchronous operation.

For example:

- Fetching data from an API.
- Reading data from a server.
- Performing an asynchronous operation.

### Three states of a Promise

Pending

The operation is still in progress.

Fulfilled

Operation succeeded.

Rejected

Operation failed.

### Creating a Promise

```
const myPromise = new Promise((resolve, reject) => {
    let success = true;

    if (success) {
        resolve("Data received successfully");
    } else {
        reject("Something went wrong");
    }
});
```

Here:

- `resolve()` indicates success.
- `reject()` indicates failure.

### Handling a Promise

We use `.then()`, `.catch()` and `.finally()`.

```
myPromise
    .then((result) => {
        console.log(result);
    })
    .catch((error) => {
        console.log(error);
    })
    .finally(() => {
        console.log("Operation completed");
    });
```

### Real-world example: Fetch API

```
fetch("https://jsonplaceholder.typicode.com/users")
    .then((response) => {
        if (!response.ok) {
            throw new Error("API request failed");
        }

        return response.json();
    })
    .then((data) => {
        console.log(data);
    })
    .catch((error) => {
        console.log(error.message);
    });
```

This fetches user data from an API.

### Promise methods

| Method                 | Purpose                                                   |
| ---------------------- | --------------------------------------------------------- |
| `Promise.all()`        | Waits for all promises to fulfill; rejects if one rejects |
| `Promise.allSettled()` | Waits for all promises to settle                          |
| `Promise.race()`       | Settles with the first settled promise                    |
| `Promise.any()`        | Fulfills with the first fulfilled promise                 |
| `Promise.resolve()`    | Creates a fulfilled promise                               |
| `Promise.reject()`     | Creates a rejected promise                                |

### Interview questions

1. What is a Promise?
2. What are the three Promise states?
3. What is resolve?
4. What is reject?
5. What is the difference between then and catch?
6. What is finally?
7. What is Promise.all()?
8. What is Promise.allSettled()?
9. What is the difference between Promise.race() and Promise.any()?
10. Why do we use Promises instead of nested callbacks?

# 10. Async and Await

### What is async/await?

Async/await is a modern way of working with Promises. It makes asynchronous code easier to read and write.

### Async keyword

An `async` function always returns a Promise.

```
async function greet() {
    return "Hello Mohideen";
}

greet().then((result) => {
    console.log(result);
});
```

Output:

```
Hello Mohideen
```

Although we return a string, JavaScript wraps it in a fulfilled Promise.

### Await keyword

`await` pauses execution of the surrounding async function until the Promise settles.

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

### Error handling with try/catch

```
async function getUsers() {
    try {
        const response = await fetch(
            "https://jsonplaceholder.typicode.com/users"
        );

        if (!response.ok) {
            throw new Error("Failed to fetch users");
        }

        const data = await response.json();

        console.log(data);

    } catch (error) {
        console.log("Error:", error.message);
    }
}

getUsers();
```

### Promise vs async/await

| Promise                                          | Async/await                                                                           |
| ------------------------------------------------ | ------------------------------------------------------------------------------------- |
| Uses `.then()` and `.catch()`                    | Uses `await` and `try/catch`                                                          |
| Can become difficult to read when deeply chained | Often easier to read                                                                  |
| Represents asynchronous completion               | Syntax for working with Promises                                                      |
| Can be used directly                             | Must use await inside an async function, except at supported top-level await contexts |

### Real-world React example

Imagine ShopSphere needs to display products from Django REST Framework.

```
async function fetchProducts() {
    try {
        const response = await fetch(
            "http://localhost:8000/api/products/"
        );

        if (!response.ok) {
            throw new Error("Unable to fetch products");
        }

        const products = await response.json();

        console.log(products);

    } catch (error) {
        console.log(error.message);
    }
}
```

This is a useful example to explain in your interview.

### Interview questions

1. What is async/await?
2. Why do we use async?
3. What does await do?
4. Can we use await outside an async function?
5. What does an async function return?
6. How do you handle errors in async/await?
7. What is the difference between async/await and Promises?
8. Can we use multiple await statements?
9. How do you execute multiple API requests concurrently?
10. What is the difference between sequential and parallel API requests?

Important practical concept:

Sequential:

```
const user = await getUser();
const orders = await getOrders();
```

Parallel, when the operations are independent:

```
const [user, orders] = await Promise.all([
    getUser(),
    getOrders()
]);
```

# 11. map(), filter(), reduce()

Extremely important for React interviews

These are JavaScript array methods. You will frequently use them when displaying API data, filtering products, calculating cart totals, and managing React state.

Let's use your ShopSphere e-commerce application as an example.

Consider this array:

```
const products = [
    { id: 1, name: "Laptop", price: 50000 },
    { id: 2, name: "Mobile", price: 20000 },
    { id: 3, name: "Headphones", price: 2000 },
    { id: 4, name: "Keyboard", price: 1500 }
];
```

## A. map()

`map()` creates a new array by transforming every element of the original array.

Example:

```
const prices = products.map((product) => {
    return product.price;
});

console.log(prices);
```

Output:

```
[50000, 20000, 2000, 1500]
```

Short syntax:

```
const names = products.map(product => product.name);

console.log(names);
```

Output:

```
["Laptop", "Mobile", "Headphones", "Keyboard"]
```

Real-world React example:

```
function ProductList() {
    const products = [
        { id: 1, name: "Laptop" },
        { id: 2, name: "Mobile" },
        { id: 3, name: "Keyboard" }
    ];

    return (
        <div>
            {products.map((product) => (
                <h3 key={product.id}>
                    {product.name}
                </h3>
            ))}
        </div>
    );
}
```

Here, `map()` converts product data into React elements.

## B. filter()

`filter()` creates a new array containing only the elements that satisfy a condition.

Example:

```
const expensiveProducts = products.filter(
    product => product.price > 10000
);

console.log(expensiveProducts);
```

Output:

```
[
    { id: 1, name: "Laptop", price: 50000 },
    { id: 2, name: "Mobile", price: 20000 }
]
```

Real-world example:

Suppose you want to display only available products.

```
const products = [
    { name: "Laptop", available: true },
    { name: "Mobile", available: false },
    { name: "Keyboard", available: true }
];

const availableProducts = products.filter(
    product => product.available === true
);

console.log(availableProducts);
```

## C. reduce()

`reduce()` processes an array and combines its elements into a single accumulated result.

Example: Calculate total price.

```
const prices = [100, 200, 300, 400];

const total = prices.reduce((sum, price) => {
    return sum + price;
}, 0);

console.log(total);
```

Output:

```
1000
```

Understand the parameters:

```
array.reduce((accumulator, currentValue) => {
    return accumulator + currentValue;
}, initialValue);
```

- `accumulator`: Stores the accumulated result.
- `currentValue`: Current element.
- `initialValue`: Starting value.

### Real-world ShopSphere cart example

```
const cart = [
    { name: "Laptop", price: 50000, quantity: 1 },
    { name: "Mouse", price: 1000, quantity: 2 },
    { name: "Keyboard", price: 2000, quantity: 1 }
];

const totalAmount = cart.reduce((total, item) => {
    return total + item.price * item.quantity;
}, 0);

console.log(totalAmount);
```

Output:

```
54000
```

## Difference between map(), filter() and reduce()

| Method   | Purpose                  | Return value              |
| -------- | ------------------------ | ------------------------- |
| map()    | Transform elements       | New array                 |
| filter() | Select matching elements | New array                 |
| reduce() | Accumulate elements      | Single accumulated result |

Remember this interview shortcut

map()

Transform

filter()

Select

reduce()

Accumulate

### Interview questions

1. What is map()?
2. What is filter()?
3. What is reduce()?
4. What is the difference between map and forEach?
5. What is the difference between map and filter?
6. Does map modify the original array?
7. Does filter modify the original array?
8. What is the accumulator in reduce?
9. What happens if we don't provide an initial value to reduce?
10. How do you calculate a shopping cart total using reduce?

### Coding exercise

Given the following array:

```
const employees = [
    { name: "Arun", salary: 25000 },
    { name: "Kumar", salary: 40000 },
    { name: "Ravi", salary: 30000 },
    { name: "John", salary: 50000 }
];
```

Write code to:

1. Get only employee names using `map()`.
2. Find employees earning more than ₹30,000 using `filter()`.
3. Calculate the total salary using `reduce()`.
4. Calculate the average salary using `reduce()`.

# 12. Destructuring and Spread Operator

## A. Destructuring

Destructuring allows you to extract values from arrays or properties from objects and assign them to variables.

### 1. Array destructuring

Without destructuring:

```
const skills = ["HTML", "CSS", "JavaScript"];

const first = skills[0];
const second = skills[1];

console.log(first);
console.log(second);
```

With destructuring:

```
const skills = ["HTML", "CSS", "JavaScript"];

const [first, second, third] = skills;

console.log(first);
console.log(second);
console.log(third);
```

Output:

```
HTML
CSS
JavaScript
```

### Skipping array elements

```
const numbers = [10, 20, 30];

const [first, , third] = numbers;

console.log(first); // 10
console.log(third); // 30
```

### 2. Object destructuring

Without destructuring:

```
const user = {
    name: "Mohideen",
    age: 27,
    city: "Chennai"
};

console.log(user.name);
console.log(user.age);
```

With destructuring:

```
const { name, age, city } = user;

console.log(name);
console.log(age);
console.log(city);
```

### Renaming variables

```
const user = {
    name: "Mohideen",
    age: 27
};

const { name: username, age: userAge } = user;

console.log(username);
console.log(userAge);
```

### Default values

```
const user = {
    name: "Mohideen"
};

const { name, city = "Chennai" } = user;

console.log(city);
```

Output:

```
Chennai
```

### Real-world React example

```
function UserProfile({ name, age, city }) {
    return (
        <div>
            <h2>{name}</h2>
            <p>{age}</p>
            <p>{city}</p>
        </div>
    );
}
```

Here, we destructure props directly in the function parameters.

## B. Spread operator (...)

The spread operator expands elements of an iterable or properties of an object.

### 1. Spread with arrays

```
const arr1 = [10, 20, 30];
const arr2 = [40, 50, 60];

const result = [...arr1, ...arr2];

console.log(result);
```

Output:

```
[10, 20, 30, 40, 50, 60]
```

### 2. Copying an array

```
const original = [10, 20, 30];

const copy = [...original];

copy.push(40);

console.log(original); // [10, 20, 30]
console.log(copy);     // [10, 20, 30, 40]
```

### 3. Spread with objects

```
const user = {
    name: "Mohideen",
    age: 27
};

const updatedUser = {
    ...user,
    city: "Chennai"
};

console.log(updatedUser);
```

Output:

```
{
    name: "Mohideen",
    age: 27,
    city: "Chennai"
}
```

### 4. Updating object properties

```
const user = {
    name: "Mohideen",
    age: 27
};

const updatedUser = {
    ...user,
    age: 28
};

console.log(updatedUser);
```

The original object remains unchanged.

### 5. Spread in React state

This is particularly important.

```
const [user, setUser] = useState({
    name: "Mohideen",
    age: 27
});

function updateAge() {
    setUser({
        ...user,
        age: 28
    });
}
```

Why use spread?

We preserve the existing properties while updating only the age property.

### C. Rest operator

The rest operator also uses `...`, but it collects remaining elements or properties.

Example:

```
const numbers = [10, 20, 30, 40];

const [first, ...remaining] = numbers;

console.log(first);     // 10
console.log(remaining); // [20, 30, 40]
```

Function example:

```
function add(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}

console.log(add(10, 20, 30, 40));
```

Output:

```
100
```

### Spread vs Rest

| Spread                     | Rest                                          |
| -------------------------- | --------------------------------------------- |
| Expands values             | Collects values                               |
| Used in arrays and objects | Used in destructuring and function parameters |
| Combines arrays            | Collects remaining arguments                  |

Important interview point: Spread makes only a shallow copy. Nested objects can still share references.

### Interview questions

1. What is destructuring?
2. What is array destructuring?
3. What is object destructuring?
4. What are default values in destructuring?
5. What is the spread operator?
6. What is the rest operator?
7. What is the difference between spread and rest?
8. How do you merge two arrays?
9. How do you copy an object?
10. What is a shallow copy?
11. How do you update React state using spread?
12. Does spread perform a deep copy?

# 13. JavaScript coding interview practice

Now let's practise the most commonly asked coding problems from today's topics.

### Exercise 1 – var, let and const

Predict the output:

```
var a = 10;
let b = 20;
const c = 30;

a = 15;
b = 25;

console.log(a);
console.log(b);
console.log(c);
```

### Exercise 2 – Functions

Write a function that accepts two numbers and returns their sum.

Expected:

```
add(10, 20); // 30
```

### Exercise 3 – Arrays

Find the largest number:

```
const numbers = [10, 45, 23, 89, 12];
```

Expected: `89`

### Exercise 4 – Objects

Create an employee object containing:

- Name
- Age
- Designation
- Skills

Print all the properties.

### Exercise 5 – map()

Convert the following numbers into their squares.

```
const numbers = [1, 2, 3, 4, 5];
```

Expected:

```
[1, 4, 9, 16, 25]
```

### Exercise 6 – filter()

Find all numbers greater than 50.

```
const numbers = [10, 60, 30, 80, 45, 90];
```

Expected:

```
[60, 80, 90]
```

### Exercise 7 – reduce()

Find the sum:

```
const numbers = [10, 20, 30, 40, 50];
```

Expected: `150`

### Exercise 8 – Closures

Create a counter using closures.

Expected:

```
const counter = createCounter();

counter(); // 1
counter(); // 2
counter(); // 3
```

### Exercise 9 – Promises

Create a Promise that resolves with `"Success"` and print the result using `.then()`.

### Exercise 10 – Async/await

Create an async function that fetches user information from:

`https://jsonplaceholder.typicode.com/users`

Print the response using async/await and handle errors using try/catch.

# 14. Test your JavaScript interview knowledge

Try these questions without referring to the notes.

JavaScript assessment

0/12 answered

1\. Which variable declaration is block scoped?

var only

let and const

All three are function scoped

None

2\. What is the output of typeof null?

null

undefined

object

number

3\. What is the result of 5 == '5'?

true

false

undefined

Error

4\. Which function syntax uses =>?

Anonymous function only

Arrow function

Callback only

Constructor

5\. What does a closure remember?

Only global variables

Its outer lexical environment

Only function arguments

The DOM

6\. What is a callback?

A variable

A function passed to another function

An array method

A Promise state

7\. What are the three states of a Promise?

Start, stop, end

True, false, null

Pending, fulfilled, rejected

Open, close, wait

8\. What does an async function return?

Always a string

Always a number

A Promise

An array

9\. Which method creates a new array by transforming each element?

filter()

reduce()

map()

forEach()

10\. Which method is used to accumulate an array into one result?

map()

filter()

reduce()

find()

11\. What does the spread operator do?

Deletes array values

Expands iterable values or object properties

Creates a Promise

Declares variables

12\. What does the rest operator do?

Expands an array

Collects remaining values

Sorts an array

Copies an object deeply

Submit assessment

# 15. Your assignment for today

Before moving to React.js, complete these tasks.

JavaScript study checklist

0/14

Explain var, let and const without notes.

Explain all seven primitive data types.

Write examples for arithmetic, comparison and logical operators.

Create five functions, including two arrow functions.

Create an array of five products.

Create an object representing an employee.

Explain scope and hoisting with code.

Write a closure-based counter.

Create a callback example.

Create and handle a Promise.

Fetch API data using async/await.

Use map(), filter() and reduce() on product data.

Demonstrate array and object destructuring.

Copy and update an object using spread.

## How we'll continue

I recommend that you don't just memorize these definitions. Interviewers often ask you to write code and predict outputs.

Let's start your actual JavaScript interview practice.

Choose your interview difficulty

Beginner – Basic JavaScript questions

Intermediate – Output-based and coding questions

Advanced – Closures, event loop, Promises and tricky questions

Start JavaScript mock interview&#x20;

My advice: Pay special attention to `map()`, `filter()`, `reduce()`, closures, Promises, async/await and destructuring. These concepts are particularly useful in your React.js and ShopSphere project discussions.


