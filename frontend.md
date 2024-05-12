# Network

### <span style="color:red;">what happens behind the scenes after you click google.com</span>

https://www.youtube.com/watch?v=dh406O2v_1c

1. On clicking www.google.com
2. the client will send a request to DNS recursor (Domain Name Server)
3. the DNS will in return send a response containing the IP address (216.58.217.206) of www.google.com back to the browser
4. at this stage nothing has been displayed yet.
5. the browser again sends another HTTP/HTTPS request to the web server
6. the web server responds with the actual website this time around.

**protocols:**

-   Stateful Protocol: TCP/IP  
    Stateful Protocol require server to save the status and session information.

-   Stateless Protocol: HTTP/HTTPS = HTTP+SSL.  
    Stateless Protocol does not require the server to retain the server information or session details.

### <span style="color:red;">HTTP requests methods</span>

-   GET  
    The GET method requests a representation of the specified resource. Requests using GET should **only retrieve data**

-   POST - create  
    The POST method submits an entity to the specified resource, often causing a change in state or side effects on the server.

-   PUT - update  
    The PUT method replaces all current representations of the target resource with the request payload.

-   PATCH - update partially  
    The PATCH method applies partial modifications to a resource.
-   DELETE  
    The DELETE method deletes the specified resource.

### <span style="color:red;">CORS</span>

Cross-Origin Resource Sharing (CORS) is **an HTTP-header based mechanism** allows restricted resources on a web page to be requested from another domain outside the origin domain.

For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts. For example, XMLHttpRequest and the Fetch API follow the same-origin policy. This means that a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.

### <span style="color:red;">What does proxy mean?</span>

### <span style="color:red;">cookie, session, localstorage</span>

![Alt text](https://i.stack.imgur.com/sMNoo.png)

---

# HTML

### <span style="color:red;">How to increase SEO? semantic html?</span>

# CSS

### <span style="color:red;">CSS preprocessor</span>

-   sass: scss & sass
-   sass: indentation
-   scss: curly braces to nest statements, and newlines instead of semicolons to separate them
-

### <span style="color:red;">CSS modules - webpack</span>

This approach is designed to fix the problem of the global scope in CSS.

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

-   globally scoped / function/locally scoped

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

---

### <span style="color:red;">pass by value & pass by reference</span>

---

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

---

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

### <span style="color:red;">Closure</span>

#### What is Closure

A closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

#### Why we need Closure / pros & cons

pros

-   Data Encapsulation: With a function closure you can store data in a separate scope, and share it only where necessary.

#### Examples

-   JavaScript closures can be used to implement throttle and debounce functionality in your application.

#### When to use

-   Closures are very helpful to hide the implementation details in javascript. Closures can be useful to create private variables and functions.

function scope, glodbal scope, bloack scope, module scope,

Lexical Scope  
Lexical Scoping means the variable that are defined outside your scope are automatically available in inner scope, which means you don’t need to pass those to inner scope.

---

### <span style="color:red;">ES6</span>

-   arrow function
-   spread operator ...
-   modules

### <span style="color:red;">Shallow copy, deep copy, spread operator / 基础类型，复杂数据类型，array 和 object 如何深度复制</span>

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
fetch API / Axios ...  
Promise.all()

**Fetch API**

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

---

### <span style="color:red;">Difference between ( for... in ) and ( for... of ) statements?</span>

---

# Typescript

### <span style="color:red;">What is TS</span>

TypeScript is JavaScript with syntax for types.
TS is a superset of JS

### <span style="color:red;">Why we need TS</span>

pros:

-   Make code easier for developers to understand and maintain
-   When the project is developed by several developers, TypeScript helps improve collaboration
-   TypeScript's static type checking helps catch potential errors and bugs during the development phase

cons:

-   requires additional effort and time to set up

### <span style="color:red;">Typescript class, interface, type</span>

**When to use interfaces:**

-   when you need to create a **contract** of the properties and functions for an object
-   when you want other objects to start with this base set of properties  
    Use them when you need to create a contract of the properties and functions for an object that will be used in more than one place in your code, especially more than one file or function. Also, use when you want other objects to start with this base set of properties, such as having a Vehicle interface that multiple classes implement as specific types of vehicles, like Car, Truck, Boat (e.g. class Car implements Vehicle).

**When NOT to use interfaces:**  
When you want to have default values, implementations, constructors, or functions (not just signatures).

**When to use classes:**  
When you want to create objects that have actual function code in them, have a constructor for initialization, and/or you want to create instances of them with new. Also, for simple data objects, you can use classes for setting up default values. Another time you would want to use them is when you are doing type checking, though there are workarounds for interfaces if needed (see the interface section OS link).

**When NOT to use classes:**  
When you have a simple data interface, do not need to instantiate it, when you want to have it implemented by other objects, when you want to simply put an interface on an existing object (think type definition files) or when the space it would take up is prohibitive or unwarranted. As a side note, if you look in .d.ts files you will notice that they only use interfaces and types, and thus this is completely removed when transpiled to TS.

**When to use type:**  
Use type when defining an alias for primitive types (string, boolean, number, bigint, symbol, etc)
Use type when defining tuple types
Use type when defining function types
Use type when defining a union
Use type when trying to overload functions in object types via composition
Use type when needing to take advantage of mapped types

**When to use interface:**  
Use interface for all object types where using type is not required (see above)
Use interface when you want to take advantage of declaration merging.

---

### any, unknown

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
            <p>Cillum culpa deserunt enim et eiusmod quis proident consequat tempor ipsum sunt esse.</p>
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

#### useMemo useCallback diff / uselayouteffect

### What is the disadvantage of useRef()

### useState()

useState 里的 State 和 class component 里的 State 有什么区别

### useEffect => class fn 的生命周期

```javascript
num = 0;

useEffect(() => {
    setNum(num + 1);
    setNum(num + 1);
});

console.log(num); // 会输出什么结果
```

### <span style="color:red;">setState()</span>

### <span style="color:red;">How to force react to render? How to prevent re-render? / How can I trigger rerender?</span>

-   forceUpdate()  
    force react to render
-   useMemo()  
    prevent re-render

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

---

#### IIFE function

A JavaScript IIFE (Immediately Invoked Function Expression) is a function that runs the moment it is invoked or called in the JavaScript event loop

### Enzyme Vs React Testing Library

---

# Angular

TodoList:  
https://www.youtube.com/watch?v=hdxaL551G_Q

---

# Nextjs

### <span style="color:red;">Server side rendering, client side rendering</span>

# Other techs

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
