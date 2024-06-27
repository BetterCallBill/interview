# HTML

### <span style="color:red;">How to increase SEO?</span>

To increase SEO, I focus on the following steps:

1. **Quality Content**: Create relevant and engaging content with targeted keywords.
2. **Keywords**: Research and use keywords that users are likely to search for.
3. **On-Page Optimization**: Optimize titles, meta descriptions, headers, and URLs.
4. **Mobile-Friendly**: Ensure the website is responsive and loads quickly on mobile devices.
5. **Backlinks**: Build high-quality backlinks from reputable sites.
6. **Regular Updates**: Keep content fresh and updated regularly.
7. **Technical SEO**: Improve site speed, fix broken links, and ensure proper indexing.

By implementing these strategies, I can help improve the site's search engine ranking.

# CSS

### <span style="color:red;">CSS preprocessor</span>

-   sass: scss & sass
-   sass: indentation
-   scss: curly braces to nest statements, and newlines instead of semicolons to separate them

### <span style="color:red;">CSS modules - webpack</span>

This approach is designed to fix the problem of the global scope in CSS.

CSS Modules allow you to scope CSS styles to individual components, preventing global namespace pollution. Here’s a simple example using React:

### Step 1: Create a CSS Module

Create a CSS file named `Button.module.css`:

```css
/* Button.module.css */
.button {
    background-color: blue;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.button:hover {
    background-color: darkblue;
}
```

### Step 2: Create a React Component

Create a React component named `Button.js`:

```javascript
// Button.js
import React from 'react';
import styles from './Button.module.css';

const Button = () => {
    return <button className={styles.button}>Click Me</button>;
};

export default Button;
```

### Step 3: Use the Component

Now, you can use the `Button` component in your application:

```javascript
// App.js
import React from 'react';
import Button from './Button';

const App = () => {
    return (
        <div>
            <h1>My App</h1>
            <Button />
        </div>
    );
};

export default App;
```

### Explanation:

-   **Button.module.css**: Contains the CSS styles scoped to the Button component.
-   **Button.js**: Imports the CSS module and uses the scoped class names to style the button.
-   **App.js**: Integrates the Button component, which uses the scoped styles.

This way, the styles in `Button.module.css` only apply to the `Button` component, avoiding conflicts with other styles in the application.

### <span style="color:red;">selector</span>

-   DOM selector

```javascript
// QuerySelector Methods:
querySelector();
querySelectorAll();

// GetElement Methods:
getElementById();
getElementsByTagName();
getElementsByClassName();
```

-   CSS selector  
    https://www.w3schools.com/cssref/css_selectors.php

### <span style="color:red;">CSS position</span>

-   static: HTML elements are positioned static by default.
-   relative: is positioned relative to its normal position
-   fixed: is positioned relative to the viewport
-   absolute: is positioned relative to the nearest positioned ancestor
-   sticky: A sticky element toggles between relative and fixed

**11 Ways to Center a Div or Text in a Div in CSS**  
https://blog.hubspot.com/website/center-div-css

How to Center a Div Within a Div

-   Know the width and height of the div: Using the Position, Top, Left, and Margin Properties

```css
.parent {
    background: gray;
    height: 300px;
    width: 300px;
    position: relative;
}

.child {
    background: orange;
    width: 100px;
    height: 100px;
    position: absolute;
    top: 50%;
    left: 50%;
    margin: -60px 0 0 -60px;
}
```

-   Unknown height and width: Using the Position, Top, Left, and Transform Properties

```css
.parent {
    background: gray;
    height: 100px;
    width: 100px;
    position: relative;
}

.child {
    background-color: orange;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

-   Using Flexbox

```css
html,
body {
    height: 100%;
}

.parent {
    height: 200px;
    background: gray;
    display: flex;
    align-items: center;
    justify-content: center;
}

.child {
    background-color: orange;
    width: 100px;
    height: 100px;
}
```

### <span style="color:red;">CSS box model</span>

### <span style="color:red;">Flex vs Grid</span>

-   Layout methods
-   Grid: designed for two-dimensional layout - rows, and columns at the same time
-   Flex: designed for layout in one dimension - either a row or a column

### <span style="color:red;">How to design the CSS structure of a project</span>

-   existing style guide for CSS
-   Avoid styles for specific elements
-   Break down your project into components
-   Use a preprocessor like Sass or Less, or BEM naming convention Blocks, Elements and Modifiers

---

# JS

### <span style="color:red;">Heap 堆 vs Stack 栈</span>

### <span style="color:red;">var, let, const</span>

**var:**

-   globally scoped / function / locally scoped

```javascript
var greeter;
console.log(greeter); // greeter is undefined
greeter = 'say hello';
```

Hoisting of var: undefined.

**let:**

-   block scoped
-   can be updated but not re-declared.

Hoisting of let: Reference Error

**const:**

-   block scoped
-   must be initialized during declaration
-   cannot be updated or re-declared
-   a const object cannot be updated, the properties of this objects can be updated

Hoisting of const: syntax errror, so the code will simply not run.

---

### <span style="color:red;">What is Hoisting</span>

In JavaScript, a variable can be declared after it has been used.
In other words; a variable can be used before it has been declared.
**JavaScript only hoists declarations, not initializations.**

```javascript
console.log(a);
console.log(b);
console.log(c);
let a = 1;
const b = 2;
var c = 3;

// 后面又加了 use strict 问输出什么
// Uncaught ReferenceError: Cannot access 'a' before initialization
```

### <span style="color:red;">pass by value & pass by reference</span>

### <span style="color:red;">Class - inheritance 继承</span>

```javascript
class Student extends Person {
    constructor(name) {
        super(name);
    }
}
```

### <span style="color:red;">prototype</span>

Class.prototype => explicit prototype  
**proto** => implicit prototype

### <span style="color:red;">this</span>

```
What is this?
In JavaScript, the this keyword refers to an object.

Which object depends on how this is being invoked (used or called).

The this keyword refers to different objects depending on how it is used:

In an object method, this refers to the object.
Alone, this refers to the global object.
In a function, this refers to the global object.
In a function, in strict mode, this is undefined.
In an event, this refers to the element that received the event.
Methods like call(), apply(), and bind() can refer this to any object.
```

### <span style="color:red;">ES6</span>

-   arrow function
-   spread operator ...
-   modules

### <span style="color:red;">ES6 arrow function</span>

-   this, this is lexically bound in arrow function
-   Constructors
-   arguments object
-   Implicit return
-   Use arrow functions for concise, simple functions that don’t require their own this binding or other special features.
-   Use regular functions when you need more control over this, when defining methods within classes, or when working with constructor functions.

When not to use arrow functions

-   Inside an object literal.
-   Object prototype
-   Invoking constructors
-   Callback with dynamic context

---

### <span style="color:red;">Closure 闭包</span>

#### What is Closure

A closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

#### Why we need Closure / pros & cons

Pros

-   Data Encapsulation: With a function closure you can store data in a separate scope, and share it only where necessary.

#### Examples

-   JavaScript closures can be used to implement throttle and debounce functionality in your application.

#### When to use

-   Closures are very helpful to hide the implementation details in javascript. Closures can be useful to create private variables and functions.

function scope, glodbal scope, bloack scope, module scope,

**Lexical Scope**
Lexical Scoping means the variable that are defined outside your scope are automatically available in inner scope, which means you don’t need to pass those to inner scope.

### <span style="color:red;">setTimeout((){}, 1000)</span>

stack =>
webapis =>
task queue =>
event loop (check whether stask is empty. If stack is empty, push task queue into stack) =>
stack

---

### <span style="color:red;">Shallow copy, deep copy, spread operator / 基础类型，复杂数据类型，array 和 object 如何深度复制</span>

In JavaScript, deep copying an array or object means creating a new array or object that is a complete, independent copy of the original, including nested objects and arrays. Here are common methods to achieve deep copying:

### Using JSON Methods:

For simple objects and arrays (without functions, `undefined`, or special objects like `Date`):

```javascript
let originalArray = [1, 2, [3, 4]];
let copiedArray = JSON.parse(JSON.stringify(originalArray));

let originalObject = { a: 1, b: { c: 2 } };
let copiedObject = JSON.parse(JSON.stringify(originalObject));
```

### Using a Recursive Function:

This approach works for more complex objects and arrays, including those with functions and special objects.

```javascript
function deepCopy(obj) {
    if (obj === null || typeof obj !== 'object') {
        return obj;
    }

    if (Array.isArray(obj)) {
        let copy = [];
        for (let i = 0; i < obj.length; i++) {
            copy[i] = deepCopy(obj[i]);
        }
        return copy;
    }

    let copy = {};
    for (let key in obj) {
        if (obj.hasOwnProperty(key)) {
            copy[key] = deepCopy(obj[key]);
        }
    }
    return copy;
}

// Usage
let originalArray = [1, 2, [3, 4]];
let copiedArray = deepCopy(originalArray);

let originalObject = { a: 1, b: { c: 2 } };
let copiedObject = deepCopy(originalObject);
```

### Using Libraries:

For more robust deep copying, you can use libraries like `lodash`.

```javascript
// Using lodash
const _ = require('lodash');

let originalArray = [1, 2, [3, 4]];
let copiedArray = _.cloneDeep(originalArray);

let originalObject = { a: 1, b: { c: 2 } };
let copiedObject = _.cloneDeep(originalObject);
```

### Example:

```javascript
// Original Object
let originalObject = {
    name: 'John',
    age: 30,
    address: {
        city: 'New York',
        country: 'USA',
    },
    hobbies: ['reading', 'traveling'],
};

// Deep Copy using lodash
let copiedObject = _.cloneDeep(originalObject);

// Modify copied object
copiedObject.address.city = 'Los Angeles';
copiedObject.hobbies.push('coding');

// Original object remains unchanged
console.log(originalObject.address.city); // 'New York'
console.log(originalObject.hobbies); // ['reading', 'traveling']

// Copied object is changed
console.log(copiedObject.address.city); // 'Los Angeles'
console.log(copiedObject.hobbies); // ['reading', 'traveling', 'coding']
```

Each method has its use cases, with `JSON.parse(JSON.stringify())` being the simplest for basic scenarios, and recursive functions or libraries like `lodash` being more versatile for complex data structures.

---

## Asynchronous programming

### <span style="color:red;">Concurrency & Event loop, webapis, task queue</span>

**call stack**  
one thread = one call stack = one thing at a time

**event loop**  
JavaScript has a runtime model based on an event loop, which is responsible for executing the code, collecting and processing events, and executing queued sub-tasks

### <span style="color:red;">Callbacks, Promise, Async / await</span>

https://www.youtube.com/watch?v=PoRJizFvM7s

**Callbacks**  
A callback is a function that is passed as an argument to another function and is executed at a later time

**Promise:**  
Fetch API / Axios ...  
Promise.all()

**Fetch API (Promise)**

Sure! Here are some examples of using the `fetch` API in JavaScript for various use cases:

### Basic GET Request:

Fetching data from an API endpoint.

```javascript
fetch('https://jsonplaceholder.typicode.com/posts')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

### GET Request with Query Parameters:

Appending query parameters to the URL.

```javascript
const params = new URLSearchParams({ userId: 1 });
fetch(`https://jsonplaceholder.typicode.com/posts?${params.toString()}`)
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

### POST Request:

Sending data to the server.

```javascript
fetch('https://jsonplaceholder.typicode.com/posts', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify({
        title: 'foo',
        body: 'bar',
        userId: 1,
    }),
})
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

### PUT Request:

Updating existing data on the server.

```javascript
fetch('https://jsonplaceholder.typicode.com/posts/1', {
    method: 'PUT',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify({
        id: 1,
        title: 'foo',
        body: 'bar',
        userId: 1,
    }),
})
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

### DELETE Request:

Deleting data from the server.

```javascript
fetch('https://jsonplaceholder.typicode.com/posts/1', {
    method: 'DELETE',
})
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

### Handling Errors:

Properly handling errors in fetch requests.

```javascript
fetch('https://jsonplaceholder.typicode.com/invalid-endpoint')
    .then(response => {
        if (!response.ok) {
            throw new Error('Network response was not ok ' + response.statusText);
        }
        return response.json();
    })
    .then(data => console.log(data))
    .catch(error => console.error('Fetch error:', error));
```

### Using Async/Await:

A cleaner way to handle fetch requests with async/await syntax.

```javascript
async function fetchData() {
    try {
        const response = await fetch('https://jsonplaceholder.typicode.com/posts');
        if (!response.ok) {
            throw new Error('Network response was not ok ' + response.statusText);
        }
        const data = await response.json();
        console.log(data);
    } catch (error) {
        console.error('Fetch error:', error);
    }
}

fetchData();
```

### Fetch with Credentials (e.g., for authentication):

Sending credentials with requests.

```javascript
fetch('https://example.com/api/data', {
    method: 'GET',
    credentials: 'include', // or 'same-origin'
})
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

These examples cover basic usage of the `fetch` API, handling different HTTP methods, and demonstrating error handling and the use of `async/await` for cleaner syntax.

---

### <span style="color:red;">Currying 函数柯里化</span>

Matryoshka doll (俄罗斯套娃)
https://juejin.cn/post/6844903882208837645

Currying is a transformation of functions that translates a function from callable as f(a, b, c) into callable as f(a)(b)(c).

Currying doesn’t call a function. It just transforms it.

---

### <span style="color:red;">Array methods</span>

-   map
-   filter

```javascript
let myArray = [1, 2, 0, 3, 4, 5];

myArray.map(ele => ele < 3);

myArray.filter(ele => ele < 3);

myArray.map(ele => {
    if (ele < 3) return ele;
});
```

-   reduce

```javascript
function sum(arr) {
    const reducer = (sum, val) => sum + val;
    const initialValue = 0;
    return arr.reduce(reducer, initialValue);
}

sum([1, 3, 5, 7]); // 16
```

The `reduce` method in JavaScript is used to iterate over an array and accumulate a single value based on the elements of the array. It executes a provided function for each value of the array (from left to right), resulting in a single output value.

### Syntax:

```javascript
array.reduce(callback(accumulator, currentValue[, index[, array]])[, initialValue])
```

-   **callback**: A function that is executed on each element of the array, taking four arguments:
    -   `accumulator`: The accumulator accumulates the callback's return values.
    -   `currentValue`: The current element being processed in the array.
    -   `index` (optional): The index of the current element being processed.
    -   `array` (optional): The array `reduce` was called upon.
-   **initialValue** (optional): A value to use as the first argument to the first call of the callback. If no initial value is supplied, the first element in the array will be used as the initial accumulator value, and the iteration will start from the second element.

### Example:

Summing the elements of an array.

```javascript
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, currentValue) => {
    return accumulator + currentValue;
}, 0);

console.log(sum); // Output: 15
```

### Explanation:

1. **Initial State**: The `reduce` method is called on the `numbers` array with a callback function and an initial value of `0`.
2. **First Iteration**:
    - `accumulator` = 0 (initial value)
    - `currentValue` = 1 (first element of the array)
    - The callback returns `0 + 1 = 1`
3. **Second Iteration**:
    - `accumulator` = 1 (result from the previous iteration)
    - `currentValue` = 2 (second element of the array)
    - The callback returns `1 + 2 = 3`
4. **Third Iteration**:
    - `accumulator` = 3
    - `currentValue` = 3
    - The callback returns `3 + 3 = 6`
5. **Fourth Iteration**:
    - `accumulator` = 6
    - `currentValue` = 4
    - The callback returns `6 + 4 = 10`
6. **Fifth Iteration**:
    - `accumulator` = 10
    - `currentValue` = 5
    - The callback returns `10 + 5 = 15`
7. **Final Result**: The `reduce` method returns the final accumulated value, which is `15`.

### Additional Example:

Finding the maximum value in an array.

```javascript
const numbers = [1, 2, 3, 4, 5];

const max = numbers.reduce((accumulator, currentValue) => {
    return currentValue > accumulator ? currentValue : accumulator;
}, numbers[0]);

console.log(max); // Output: 5
```

In this example, the `reduce` method is used to find the maximum value in the `numbers` array by comparing each element with the current accumulated maximum.

---

### <span style="color:red;">Difference between ( for... in ) and ( for... of ) statements?</span>

The `for...in` and `for...of` statements are both used for iteration in JavaScript, but they serve different purposes and work with different types of collections. Here's a detailed comparison:

### `for...in` Statement

-   **Purpose**: Iterates over the enumerable properties of an object (including its prototype chain).
-   **Use Case**: Typically used to loop through the properties of an object.

**Example**:

```javascript
const obj = { a: 1, b: 2, c: 3 };

for (let key in obj) {
    console.log(key); // Logs "a", "b", "c"
    console.log(obj[key]); // Logs 1, 2, 3
}
```

### `for...of` Statement

-   **Purpose**: Iterates over the values of an iterable object (e.g., arrays, strings, maps, sets, etc.).
-   **Use Case**: Typically used to loop through the values of an array or other iterable objects.

**Example**:

```javascript
const arr = [1, 2, 3];

for (let value of arr) {
    console.log(value); // Logs 1, 2, 3
}
```

### Key Differences

1. **Iteration Target**:

    - `for...in` iterates over the enumerable properties of an object.
    - `for...of` iterates over the values of an iterable object.

2. **Output**:

    - `for...in` returns the keys (property names) of the object.
    - `for...of` returns the values of the iterable object.

3. **Use Cases**:
    - Use `for...in` when you need to work with the properties of an object.
    - Use `for...of` when you need to work with the values of an iterable (like an array or string).

### Example of Misuse

Using `for...in` on an array can lead to unexpected results because it iterates over all enumerable properties, including inherited ones and those added to the prototype.

**Misuse Example**:

```javascript
const arr = [1, 2, 3];
arr.foo = 'bar';

for (let key in arr) {
    console.log(key); // Logs "0", "1", "2", "foo"
    console.log(arr[key]); // Logs 1, 2, 3, "bar"
}
```

### Proper Use of `for...of` on an Array

```javascript
const arr = [1, 2, 3];
arr.foo = 'bar';

for (let value of arr) {
    console.log(value); // Logs 1, 2, 3
}
```

### Summary

-   **`for...in`**: Use for iterating over the properties of an object.
-   **`for...of`**: Use for iterating over the values of an iterable (like arrays, strings, maps, and sets).

---

# Typescript

### <span style="color:red;">What is TS</span>

TypeScript is JavaScript with syntax for types.
TS is a superset of JS

### <span style="color:red;">Why we need TS</span>

Pros:

-   Make code easier for developers to understand and maintain
-   When the project is developed by several developers, TypeScript helps improve collaboration
-   TypeScript's static type checking helps catch potential errors and bugs during the development phase

Cons:

-   requires additional effort and time to set up

### <span style="color:red;">Typescript class, interface, type</span>

**When to use interfaces:**

-   when you need to create a **contract** of the properties and functions for an object
-   when you want other objects to start with this base set of properties  
    Use them when you need to create a contract of the properties and functions for an object that will be used in more than one place in your code, especially more than one file or function. Also, use when you want other objects to start with this base set of properties, such as having a Vehicle interface that multiple classes implement as specific types of vehicles, like Car, Truck, Boat (e.g. class Car implements Vehicle).
-   Use interface for all object types where using type is not required (see above)
-   Use interface when you want to take advantage of declaration merging.

**When NOT to use interfaces:**  
When you want to have default values, implementations, constructors, or functions (not just signatures).

**When to use class:**  
When you want to create objects that have actual function code in them, have a constructor for initialization, and/or you want to create instances of them with new. Also, for simple data objects, you can use classes for setting up default values. Another time you would want to use them is when you are doing type checking, though there are workarounds for interfaces if needed (see the interface section OS link).

**When NOT to use class:**  
When you have a simple data interface, do not need to instantiate it, when you want to have it implemented by other objects, when you want to simply put an interface on an existing object (think type definition files) or when the space it would take up is prohibitive or unwarranted. As a side note, if you look in .d.ts files you will notice that they only use interfaces and types, and thus this is completely removed when transpiled to TS.

**When to use type:**  
Use type when defining an alias for primitive types (string, boolean, number, bigint, symbol, etc)
Use type when defining tuple types
Use type when defining function types
Use type when defining a union
Use type when trying to overload functions in object types via composition
Use type when needing to take advantage of mapped types

---

### <span style="color:red;">any, unknown</span>

any, unknown:

-   allow assigning any type

any:

-   allows being assigned to any type
-   allows calling any method

unknown:

-   doesn't allow being assigned to any type
-   doesn't allow calling any method

---

# Frameworks

## React

### <span style="color:red;">styled-components</span>

Styled-components is a library that allows you to write CSS in JS while building custom components in Reactjs

```javascript
import styled from 'styled-components';

const H1 = styled.h1`
    color: red;
`;

const DefaultButton = styled.button`
    background-color: #645cfc;
    border: none;
    padding: 10px;
    color: white;
`;

function App() {
    return (
        <div>
            <H1>Styled Components</H1>
            <p>
                Cillum culpa deserunt enim et eiusmod quis proident consequat tempor ipsum sunt
                esse.
            </p>
            <DefaultButton>Click ME!</DefaultButton>
        </div>
    );
}

export default App;
```

### <span style="color:red;">What is react dom?</span>

virtual DOM, diff algorithm

The react-dom package provides DOM-specific methods that can be used at the top level of your app and as an escape hatch to get outside the React model if you need to.

### <span style="color:red;">props, state</span>

-   props are a way to pass the data or properties from parent component to child components
-   state is the real-time data available to use within that only component

Props disadvantages:

-   As the component hierarchy grows deeper, and more components rely on the prop, it becomes harder to trace and manage data flow.
-   If the data gets updated, all the components in the hierarchy also need updating, even if some don't use the data. This can be difficult and time-consuming, and it also increases the risk of introducing bugs.
-   You'll have to update each component in the hierarchy that uses the prop. This process is error-prone, making code maintenance hard and increasing inconsistencies or errors.

Solution: use useContext / Redux / MobX

### <span style="color:red;">Functional Components vs Class Components (pros cons) / when to use each</span>

#### Functional Components

```javascript
import React from 'react';

const FunctionalComponent = () => {
    return <h1>Hello, world</h1>;
};

//---------------------------------

import React from 'react';

function FunctionalComponent() {
    return <h1>Hello, world</h1>;
}
```

#### Class Components

```javascript
import React from 'react';

class ClassComponent extends React.Component {
    render() {
        return <h1>Hello, world</h1>;
    }
}
```

### <span style="color:red;">React component lifecycle</span>

![Alt text](https://i.stack.imgur.com/nTmNe.jpg)
![Alt text](https://i.stack.imgur.com/5LbsY.jpg)

#### <span style="color:red;">useMemo vs useCallback</span>

`useMemo` and `useCallback` are two hooks provided by React that help optimize performance by memoizing values and functions, respectively. Here's a breakdown of their differences and use cases:

### `useMemo`

-   **Purpose**: Memoizes the result of a calculation.
-   **Use Case**: Use `useMemo` to avoid expensive calculations on every render.
-   **Syntax**:
    ```javascript
    const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
    ```
-   **Example**:

    ```javascript
    import React, { useMemo } from 'react';

    function MyComponent({ a, b }) {
        const memoizedValue = useMemo(() => {
            return a + b; // Assume this is an expensive calculation
        }, [a, b]);

        return <div>{memoizedValue}</div>;
    }
    ```

### `useCallback`

-   **Purpose**: Memoizes a callback function.
-   **Use Case**: Use `useCallback` to prevent functions from being recreated on every render, which is useful for passing stable references to child components or avoiding unnecessary re-renders.
-   **Syntax**:
    ```javascript
    const memoizedCallback = useCallback(() => {
        doSomething(a, b);
    }, [a, b]);
    ```
-   **Example**:

    ```javascript
    import React, { useCallback } from 'react';

    function MyComponent({ a, b }) {
        const handleClick = useCallback(() => {
            console.log(a, b); // Assume this is an event handler
        }, [a, b]);

        return <button onClick={handleClick}>Click me</button>;
    }
    ```

### Key Differences

1. **What They Memoize**:

    - `useMemo`: Memoizes the result of a function (a computed value).
    - `useCallback`: Memoizes a function itself.

2. **Return Value**:

    - `useMemo`: Returns the memoized value.
    - `useCallback`: Returns the memoized function.

3. **Primary Use Case**:
    - `useMemo`: Optimize expensive calculations that should not be re-computed on every render unless dependencies change.
    - `useCallback`: Optimize by ensuring that the same function instance is passed to child components or event handlers to avoid unnecessary re-renders.

### When to Use Each

-   **`useMemo`**: When you have an expensive computation that should not be recalculated unless its dependencies change.
-   **`useCallback`**: When you need to pass a stable function reference to a child component or an event handler, to avoid causing unnecessary renders.

### Example Using Both:

```javascript
import React, { useMemo, useCallback, useState } from 'react';

function App() {
    const [count, setCount] = useState(0);
    const [number, setNumber] = useState(1);

    const factorial = useMemo(() => {
        const calculateFactorial = n => {
            console.log('Calculating factorial');
            if (n <= 0) return 1;
            return n * calculateFactorial(n - 1);
        };
        return calculateFactorial(number);
    }, [number]);

    const handleClick = useCallback(() => {
        setCount(prevCount => prevCount + 1);
    }, []);

    return (
        <div>
            <h1>
                Factorial of {number}: {factorial}
            </h1>
            <button onClick={() => setNumber(number + 1)}>Increment Number</button>
            <button onClick={handleClick}>Increment Count</button>
            <p>Count: {count}</p>
        </div>
    );
}

export default App;
```

In this example:

-   `useMemo` is used to memoize the result of the factorial calculation to avoid recalculating it unless `number` changes.
-   `useCallback` is used to memoize the `handleClick` function to ensure that the same function instance is used on each render, avoiding unnecessary re-renders of components that depend on this function.

### <span style="color:red;">useLayouteffect</span>

`useLayoutEffect` is a hook in React that is similar to `useEffect`, but it fires synchronously after all DOM mutations. This means it runs after the DOM has been updated but before the browser has painted the changes to the screen. This makes `useLayoutEffect` useful for tasks that require measuring the DOM or performing updates that need to happen before the browser paints.

### When to Use `useLayoutEffect`

-   **Reading layout**: If you need to read the layout from the DOM (e.g., get the size or position of an element) and then synchronously re-render.
-   **Preventing flickers**: If you need to make changes to the DOM that should be visible immediately without any flicker.
-   **Updating the DOM synchronously**: For scenarios where you need to make DOM updates that are dependent on the layout (e.g., animations or ensuring a scroll position).

### Syntax

```javascript
useLayoutEffect(() => {
    // Your code here (DOM reads and writes)
    return () => {
        // Cleanup if necessary
    };
}, [dependencies]);
```

### Example

Here's an example of how to use `useLayoutEffect` to measure the size of a DOM element and perform an update before the browser paints.

```javascript
import React, { useLayoutEffect, useRef, useState } from 'react';

function LayoutEffectExample() {
    const [height, setHeight] = useState(0);
    const divRef = useRef(null);

    useLayoutEffect(() => {
        if (divRef.current) {
            const newHeight = divRef.current.getBoundingClientRect().height;
            setHeight(newHeight);
        }
    }, [height]);

    return (
        <div>
            <div ref={divRef} style={{ height: '100px', background: 'lightblue' }}>
                This div's height is: {height}px
            </div>
            <button onClick={() => setHeight(height + 10)}>Increase Height</button>
        </div>
    );
}

export default LayoutEffectExample;
```

In this example:

-   `useLayoutEffect` is used to measure the height of a `div` element and update the state with the new height.
-   This ensures that the measurement is done synchronously after the DOM update and before the browser paints, preventing any visual flicker.

### Key Differences Between `useEffect` and `useLayoutEffect`

-   **Execution Timing**:
    -   `useEffect` runs asynchronously after the render is committed to the screen.
    -   `useLayoutEffect` runs synchronously after all DOM mutations but before the paint.
-   **Use Cases**:
    -   `useEffect` is typically used for side effects that don't affect the layout (e.g., fetching data, subscriptions).
    -   `useLayoutEffect` is used for operations that need to happen before the browser repaints (e.g., reading layout, preventing flickers).

### When to Choose `useLayoutEffect` Over `useEffect`

Use `useLayoutEffect` when:

-   You need to perform synchronous DOM operations that must complete before the browser repaints.
-   You need to measure or read the layout of the DOM and make adjustments accordingly to prevent visual inconsistencies.

Use `useEffect` for other side effects that don't need to block the browser's paint process, as it is less performance-critical and doesn't block the visual update of the page.

### <span style="color:red;">What is the disadvantage of useRef()</span>

`useRef` is a powerful hook in React that allows you to create a mutable reference that persists across renders. While `useRef` has many advantages, there are some potential disadvantages or pitfalls to be aware of:

### Disadvantages of `useRef`

1. **Not Reactive**:

    - **Issue**: Changes to the `useRef` object do not trigger re-renders.
    - **Example**: If you update a ref's value, React does not re-render the component to reflect this change.
    - **Impact**: This can lead to scenarios where the UI does not update to reflect the latest state if the value stored in the ref is supposed to be displayed or used for rendering logic.
    - **Example**:
        ```javascript
        const myRef = useRef(0);
        myRef.current = 5;
        // The component won't re-render even though myRef.current has changed.
        ```

2. **Imperative Code**:

    - **Issue**: `useRef` encourages imperative programming, which can sometimes conflict with React's declarative nature.
    - **Example**: Using refs to directly manipulate the DOM can lead to code that is harder to read and maintain.
    - **Impact**: Imperative code can be more error-prone and less predictable than declarative code.
    - **Example**:

        ```javascript
        const myRef = useRef(null);

        useEffect(() => {
            if (myRef.current) {
                myRef.current.style.color = 'red'; // Direct DOM manipulation
            }
        }, []);
        ```

3. **Potential for Memory Leaks**:

    - **Issue**: If refs are not cleaned up properly, they can lead to memory leaks.
    - **Example**: Holding references to DOM elements or large objects that are no longer needed.
    - **Impact**: Memory leaks can degrade performance over time, especially in long-running applications.
    - **Example**:

        ```javascript
        const myRef = useRef();

        // If myRef.current holds a large object or DOM node, it should be cleared when no longer needed.
        ```

4. **Complex Debugging**:

    - **Issue**: Since `useRef` values are mutable, it can be harder to track their changes compared to state variables that trigger re-renders.
    - **Example**: Debugging issues related to refs often requires console logging or other debugging techniques.
    - **Impact**: Mutable values can make the flow of data harder to trace, leading to more complex debugging and maintenance.

5. **Misuse for State Management**:

    - **Issue**: `useRef` is sometimes misused for state management, which can lead to bugs since refs do not trigger re-renders.
    - **Example**: Using refs to store values that should be managed with state.
    - **Impact**: This can result in UI inconsistencies and bugs because changes to refs do not cause re-renders.
    - **Example**:

        ```javascript
        const myRef = useRef(0);

        const handleClick = () => {
            myRef.current++;
            // The component won't re-render, so the UI won't reflect the updated value.
        };
        ```

### Best Practices

-   Use `useRef` for accessing DOM elements directly or for storing values that should not trigger a re-render when changed.
-   Avoid using `useRef` as a substitute for state management. Use `useState` or `useReducer` for values that need to trigger re-renders.
-   Clean up refs when they are no longer needed to prevent memory leaks.
-   Use `useEffect` or `useLayoutEffect` in conjunction with refs when performing side effects that depend on refs.

### Conclusion

While `useRef` is a valuable tool in React for managing mutable references, it is essential to use it appropriately and be aware of its limitations and potential pitfalls. Proper use and understanding of its behavior will help maintain the clarity, performance, and reliability of your React applications.

### <span style="color:red;">useState() / useState 里的 State 和 class component 里的 State 有什么区别</span>

In React, both `useState` (used in functional components) and `this.state` (used in class components) are mechanisms for managing state. However, there are several key differences between them:

### Syntax and Usage

1. **Functional Components with `useState`**:

    - **Syntax**:

        ```javascript
        import React, { useState } from 'react';

        function MyComponent() {
            const [count, setCount] = useState(0);

            return (
                <div>
                    <p>You clicked {count} times</p>
                    <button onClick={() => setCount(count + 1)}>Click me</button>
                </div>
            );
        }
        ```

    - **Usage**: `useState` returns an array with two elements: the current state and a function to update it. You can call this function to update the state, and React will re-render the component.

2. **Class Components with `this.state`**:

    - **Syntax**:

        ```javascript
        import React, { Component } from 'react';

        class MyComponent extends Component {
            constructor(props) {
                super(props);
                this.state = {
                    count: 0,
                };
            }

            handleClick = () => {
                this.setState({ count: this.state.count + 1 });
            };

            render() {
                return (
                    <div>
                        <p>You clicked {this.state.count} times</p>
                        <button onClick={this.handleClick}>Click me</button>
                    </div>
                );
            }
        }
        ```

    - **Usage**: State is initialized in the constructor using `this.state`. The `this.setState` method is used to update the state, which triggers a re-render.

### Key Differences

1. **Initialization**:

    - **useState**: Initializes state directly within the functional component.
    - **this.state**: Initializes state within the constructor of the class component.

2. **State Updates**:

    - **useState**: State updates are performed using the state updater function returned by `useState`.
    - **this.state**: State updates are performed using the `this.setState` method.

3. **State Merging**:

    - **useState**: The state updater function does not automatically merge the old and new state. You need to manually merge the state if you have multiple pieces of state.

        ```javascript
        const [state, setState] = useState({ count: 0, text: '' });

        setState(prevState => ({ ...prevState, count: prevState.count + 1 }));
        ```

    - **this.state**: `this.setState` automatically merges the old state with the new state.
        ```javascript
        this.setState({ count: this.state.count + 1 });
        ```

4. **State Handling**:

    - **useState**: Encourages the use of multiple state variables for different pieces of state.
        ```javascript
        const [count, setCount] = useState(0);
        const [text, setText] = useState('');
        ```
    - **this.state**: Typically manages all state in a single state object.
        ```javascript
        this.state = {
            count: 0,
            text: '',
        };
        ```

5. **Lifecycle Methods**:

    - **useState**: Functional components do not have lifecycle methods. Instead, hooks like `useEffect` are used to perform side effects.

        ```javascript
        import React, { useState, useEffect } from 'react';

        function MyComponent() {
            const [count, setCount] = useState(0);

            useEffect(() => {
                document.title = `You clicked ${count} times`;
            }, [count]);

            return (
                <div>
                    <p>You clicked {count} times</p>
                    <button onClick={() => setCount(count + 1)}>Click me</button>
                </div>
            );
        }
        ```

    - **this.state**: Class components have lifecycle methods like `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount`.

        ```javascript
        class MyComponent extends Component {
            componentDidMount() {
                document.title = `You clicked ${this.state.count} times`;
            }

            componentDidUpdate() {
                document.title = `You clicked ${this.state.count} times`;
            }

            render() {
                return (
                    <div>
                        <p>You clicked {this.state.count} times</p>
                        <button onClick={this.handleClick}>Click me</button>
                    </div>
                );
            }
        }
        ```

### Summary

-   **Initialization**: `useState` directly in the function, `this.state` in the constructor.
-   **Updating State**: `useState` uses a setter function, `this.setState` in classes.
-   **State Merging**: `useState` does not merge automatically, `this.setState` does.
-   **Lifecycle**: `useEffect` replaces lifecycle methods for `useState`, class components have built-in lifecycle methods.
-   **State Handling**: `useState` promotes splitting state into multiple variables, class state is typically a single object.

### <span style="color:red;">useEffect => class fn 的生命周期</span>

以下代码会输出什么结果？

```javascript
num = 0;

useEffect(() => {
    setNum(num + 1);
    setNum(num + 1);
});

console.log(num);
```

0

The console.log(num); statement is executed before the useEffect hook runs, because useEffect runs after the initial render and any updates.

### <span style="color:red;">setState()</span>

### <span style="color:red;">How to force react to render? How to prevent re-render? / How can I trigger rerender?</span>

In React, rendering behavior can be controlled in several ways. Here are methods to force a render, prevent unnecessary re-renders, and trigger re-renders.

### Forcing React to Render

1. **Using `useState`**:

    - Changing the state with `useState` forces a re-render.
    - Example:

        ```javascript
        const [_, setRender] = useState(0);

        const forceRender = () => {
            setRender(prev => prev + 1);
        };
        ```

    - Call `forceRender()` whenever you need to force a re-render.

2. **Using `useReducer`**:

    - Similar to `useState`, but provides more control and is useful for complex state logic.
    - Example:

        ```javascript
        const [ignored, forceUpdate] = useReducer(x => x + 1, 0);

        const forceRender = () => {
            forceUpdate();
        };
        ```

### Preventing Re-renders

1. **Using `React.memo`**:

    - Wrap your functional component with `React.memo` to prevent re-renders if props haven’t changed.
    - Example:
        ```javascript
        const MyComponent = React.memo(props => {
            // component code
        });
        ```

2. **Using `shouldComponentUpdate`**:

    - In class components, override `shouldComponentUpdate` to control when a component should re-render.
    - Example:

        ```javascript
        class MyComponent extends React.Component {
            shouldComponentUpdate(nextProps, nextState) {
                // return false to prevent re-render
                return nextProps.someProp !== this.props.someProp;
            }

            render() {
                return <div>My Component</div>;
            }
        }
        ```

3. **Using `useCallback` and `useMemo`**:

    - Optimize performance by memoizing functions and values.
    - Example:

        ```javascript
        const memoizedCallback = useCallback(() => {
            // function logic
        }, [dependencies]);

        const memoizedValue = useMemo(() => {
            // compute and return value
        }, [dependencies]);
        ```

### Triggering Re-renders

1. **State Updates**:

    - Changing state using `useState` or `useReducer` triggers a re-render.
    - Example:

        ```javascript
        const [count, setCount] = useState(0);

        const increment = () => {
            setCount(count + 1);
        };
        ```

2. **Props Changes**:

    - Passing new props to a component triggers a re-render.
    - Example:
        ```javascript
        <ChildComponent someProp={someValue} />
        ```

3. **Context Updates**:
    - Using `useContext` hook to read from a context. Any change in the context value triggers a re-render.
    - Example:
        ```javascript
        const value = useContext(MyContext);
        ```

### Example of Force Render and Prevent Re-render in a Functional Component

```javascript
import React, { useState, useReducer, useCallback, useMemo } from 'react';

const ForceRenderComponent = React.memo(({ someProp }) => {
    const [count, setCount] = useState(0);
    const [, forceRender] = useReducer(x => x + 1, 0);

    const handleClick = () => {
        setCount(count + 1);
    };

    const forceReRender = () => {
        forceRender();
    };

    const memoizedValue = useMemo(() => {
        return count * 2;
    }, [count]);

    const memoizedCallback = useCallback(() => {
        console.log('Memoized callback:', count);
    }, [count]);

    return (
        <div>
            <p>Count: {count}</p>
            <p>Memoized Value: {memoizedValue}</p>
            <button onClick={handleClick}>Increment Count</button>
            <button onClick={forceReRender}>Force Re-render</button>
            <button onClick={memoizedCallback}>Log Count</button>
        </div>
    );
});

export default ForceRenderComponent;
```

In this example:

-   `ForceRenderComponent` is wrapped in `React.memo` to prevent unnecessary re-renders unless `someProp` changes.
-   `useState` and `useReducer` are used to manage state and force re-renders.
-   `useMemo` and `useCallback` are used to memoize values and functions, optimizing performance.

### <span style="color:red;">Redux</span>

A state mangement tool

When should you use?

-   You have large amounts of application state that are needed in many places in the app
-   The app state is updated frequently
-   The logic to update that state may be complex
-   The app has a medium or large-sized codebase, and might be worked on by many people
-   You need to see how that state is being updated over time

### <span style="color:red;">What is redux middleware? middleware vs action, pros and cons</span>

Middleware in Redux provides a way to extend Redux with custom functionality. Redux middleware operates between dispatching an action and the moment it reaches the reducer. It's used for logging, crash reporting, performing asynchronous tasks, and more.

### <span style="color:red;">react-saga vs react-thunk</span>

The core difference between redux thunk and redux saga lies in their approach to handling side effects. Thunks are great for simple asynchronous behavior, while sagas offer more control over complex side effects.

Thunk: Promises  
Saga: Generators

### <span style="color:red;">如何优化 react 性能</span>

https://blog.logrocket.com/optimizing-performance-react-app/#component-state-local

### <span style="color:red;">IIFE function</span>

A JavaScript IIFE (Immediately Invoked Function Expression) is a function that runs the moment it is invoked or called in the JavaScript event loop

### <span style="color:red;">Enzyme Vs React Testing Library</span>

---

# Angular

TodoList:  
https://www.youtube.com/watch?v=hdxaL551G_Q

---

# Nextjs

### <span style="color:red;">Server side rendering, client side rendering</span>

Certainly! In the context of Next.js, which is a popular React framework, let's differentiate between Server-side Rendering (SSR) and Client-side Rendering (CSR):

### Server-side Rendering (SSR):

1. **Definition**:

    - Server-side Rendering refers to the technique where the initial HTML of a webpage is generated on the server for each request.

2. **Process**:

    - When a user requests a page, the server fetches the necessary data, renders the React components into HTML, and sends a fully rendered HTML page to the client.

3. **Advantages**:

    - **Improved SEO**: Search engines can crawl and index content easily since the page content is available in the initial HTML response.
    - **Faster Initial Load**: Users see content quicker because they receive a fully rendered page from the server.

4. **Usage in Next.js**:
    - Next.js supports SSR out of the box. Pages with SSR are created using `getServerSideProps` or `getInitialProps` methods to fetch data on the server before rendering the page.

### Client-side Rendering (CSR):

1. **Definition**:

    - Client-side Rendering involves rendering web pages in the browser using JavaScript after the initial HTML is received from the server.

2. **Process**:

    - The server sends a basic HTML shell with minimal content. The browser then executes JavaScript, fetches data, and renders the page dynamically.

3. **Advantages**:

    - **Interactive User Interfaces**: Supports highly interactive applications where content changes frequently without full page reloads.
    - **Reduced Server Load**: The server sends lightweight initial responses, reducing load and cost.

4. **Usage in Next.js**:
    - Next.js can also be used for CSR. Pages can be statically generated (`getStaticProps`) or client-side rendered (`useEffect`, `useState`) based on your application needs.

### Choosing Between SSR and CSR in Next.js:

-   **SEO and Performance**:

    -   Use SSR for content-heavy pages that require good SEO and initial load performance.
    -   Use CSR for dynamic content or applications where interactivity and frequent updates are crucial.

-   **Hybrid Approaches**:
    -   Next.js allows hybrid approaches where you can statically generate most pages (`getStaticProps`) and use SSR or CSR for specific pages or components as needed.

### Summary:

-   **Server-side Rendering (SSR)**: Initial HTML generated on the server, better for SEO and initial load times.
-   **Client-side Rendering (CSR)**: HTML sent to the client, rendered via JavaScript, suitable for dynamic and interactive applications.

Next.js provides flexibility to choose the rendering strategy based on your project requirements, balancing between SEO, performance, and interactivity.

Certainly! Here are five classic interview questions related to Next.js along with their answers:

### 1. What is Next.js and what are its key features?

**Answer:**
Next.js is a React framework that enables server-side rendering (SSR), static site generation (SSG), and client-side rendering (CSR). Its key features include:

-   **Automatic Code Splitting**: Optimizes performance by splitting JavaScript bundles into smaller files.
-   **Routing**: Simplifies page-based routing with automatic code loading.
-   **File-based Routing**: Allows routing based on the file system structure.
-   **CSS and Sass Support**: Built-in support for CSS modules and Sass.
-   **API Routes**: Enables building API endpoints inside the same Next.js framework.

### 2. Explain the difference between `getStaticProps` and `getServerSideProps` in Next.js.

**Answer:**

-   **`getStaticProps`**: Used for static site generation (SSG). Fetches data at build time and pre-renders pages with the fetched data. Ideal for content that doesn't change frequently and can be pre-rendered.
-   **`getServerSideProps`**: Used for server-side rendering (SSR). Fetches data on each request to the server. Useful for dynamic data that changes frequently or requires authentication before rendering.

### 3. How does Next.js handle routing?

**Answer:**
Next.js handles routing in two primary ways:

-   **File-based Routing**: Pages in the `pages` directory automatically map to routes based on their file names (e.g., `pages/about.js` maps to `/about`).
-   **Dynamic Routing**: Allows for dynamic routes using brackets `[]` to define dynamic segments in the URL (e.g., `pages/posts/[id].js` maps to `/posts/:id`).

### 4. What are some advantages of using Next.js for SEO?

**Answer:**
Next.js provides several advantages for SEO:

-   **Server-side Rendering (SSR)**: Generates HTML on the server, making content immediately visible to search engines.
-   **Pre-rendering**: Supports static site generation (SSG), allowing pages to be pre-rendered with content before deployment.
-   **Meta Tags**: Easily manage and update meta tags for improved SEO.

### 5. How can you optimize performance in a Next.js application?

**Answer:**
Performance optimization in Next.js involves several techniques:

-   **Code Splitting**: Automatically splits JavaScript bundles into smaller files for faster load times.
-   **Image Optimization**: Use Next.js's built-in `Image` component for automatic image optimization and lazy-loading.
-   **Static Site Generation (SSG)**: Pre-render pages at build time with `getStaticProps` to serve content quickly.
-   **Caching**: Implement caching strategies for API responses and static assets to reduce server load and improve load times.

These questions and answers cover fundamental aspects of Next.js, highlighting its features, routing mechanisms, SEO capabilities, performance optimization techniques, and data fetching methods.

# Others

### <span style="color:red;">ES6 good things</span>

### <span style="color:red;">Node.js 的优点与缺点</span>

### <span style="color:red;">webpack configeration 的问题，比如 file-loader, version 问题的处理方法</span>

---

# Code challenge

```javascript
class display extends Component {
    constructor(props) {
        // super(props)
        this.state = {
            username: 'a',
        };
    }

    handlechange() {
        this.setState({
            username: 'b',
        });
    }

    /*
    handleChange(value) {
        this.setState({
            username: value,
        });
    }
    */

    render() {
        return (
            <div>
                <span>{this.state.username}</span>

                {/*onClick={()=>{this.handlechange('c')}}*/}
                <button onClick={handleChange('c')}></button>
            </div>
        );
    }
}

/*
1. 没有 super(props)
2. onClick={()=>{this.handlechange('c')}}

Q: 在 componentDidUpdate 中调用 setState 会发生什么?
A: setState creates an infinite loop when used in ComponentDidUpdate when there is no break condition in the loop.

Q: 如何避免持续刷新?
A: add condition, or move to shouldComponentUpdate
*/
```

---

这次是一个 take home task，给了一个 api，里面有一些数据，最终想实现三个分别可以点击的 card，每个 card 里面包含了那些数据，我一开始使用 react 做的，后来想起老板的教诲，于是加入了 redux。本来想直接就交的，但是仔细读了一下 jd（一开始没有自己都 jd 是因为我看到一个 entry level 的岗位就投了），看到他们说 bonus to have: typescript 和 styled-components，于是我就用 styled-components 写的 css，然后加入了 ts，我也是第一次给 redux 加 ts，中间卡了一天，连查带改的，最后发现问题出现在要给 reducer 添加返回的 type，于是就没有报错可以运行了。

---

现场 debug：
第一题考了 async await。 一个 button 在的 onClick fn 中 this.setState({isloading:xxx}) ，api call 没有 await 在那里，所以整个 function 瞬间执行完了。

第二题是在 useeffect 去 call api 但是没有+ depend array 导致 infinity loop

第三题 是一个 react component 里， 对一个 button 点击会对一个 object 类型的数据进行值的修改，但是没有触发渲染，如何修改。（我的解决办法是深复制一下。）

---

三个正方形的盒子，一个比一个小，大的套小的，盒子居中。 当鼠标 hover 在最小的盒子上时候，外圈最大的盒子背景色会变成绿色，鼠标移出后背景色自动变回默认颜色。

考点：
如何创建一个 react app。
react 基础的配置，package.json，等等。
state 和 props 的传递。（其实他们想考前段的 state 管理工具比如 redux /mobx, 我因为时间太短配置不好 mobx 就写了一个 setState 功能传到子元素里，实现了从子元素到父元素的数据回传）
state 和 props 如何改变元素的样式（styled component or Less and SASS）
需要你尽量用 TypeScript 写

---
