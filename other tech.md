# Network

### <span style="color:red;">what happens behind the scenes after you click google.com</span>

https://www.youtube.com/watch?v=dh406O2v_1c

1. On clicking www.google.com
2. the client will send a request to DNS recursor (Domain Name Server)
3. the DNS will in return send a response containing the IP address (216.58.217.206) of www.google.com back to the browser
4. at this stage nothing has been displayed yet.
5. the browser again sends another HTTP/HTTPS request to the web server
6. the web server responds with the actual website this time around.

**Protocols:**

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

### <span style="color:red;">What is Quality Control?</span>

Quality Control in software development refers to the systematic processes and techniques used to ensure that software products meet predefined quality standards and requirements. It involves activities such as rigorous testing, code reviews, and quality assurance measures to identify and rectify defects early in the development lifecycle. By maintaining high standards of quality throughout the software development process, Quality Control aims to deliver reliable, secure, and user-friendly software solutions that meet customer expectations and adhere to industry best practices.

### <span style="color:red;">What is Version Control?</span>

### <span style="color:red;">OOP vs Functional Programming (FP)</span>

Object-Oriented Programming (OOP) focuses on modeling software entities as objects with state and behavior, promoting code reusability and modularity through classes and inheritance.

Functional Programming (FP) treats computation as the evaluation of mathematical functions, emphasizing immutability, higher-order functions, and function composition for concise and predictable code.

OOP emphasizes stateful objects and encapsulation, while FP prioritizes immutable data and avoids side effects, making it suitable for parallelism and complex transformations. Both paradigms offer distinct approaches to solving software design and implementation challenges.

### TDD - Test Driven Development

---

# DESIGN PATTERN

### <span style="color:red;">设计模式和框架. 单例，工场，委托，订阅模式的例子</span>

Singleton Pattern (单例模式):

Factory Pattern (工厂模式):

Delegate Pattern (委托模式):

Observer Pattern (订阅模式):

### <span style="color:red;">软件开发周期，当有新的 feature 的时候是采用的什么流程, 拿到 task 具体怎么拆分，什么思路</span>

When there's a new feature in the software development cycle, the process typically involves several steps.

First, I review the task to understand its requirements and scope.

Then, I break it down into smaller, manageable tasks or user stories. This helps in planning and estimating the work needed.

Next, I prioritize these tasks based on their importance and dependencies. During implementation, I follow Agile practices like Scrum or Kanban, where tasks are assigned and progress is tracked in sprints. Regular communication with the team ensures alignment and adjustments if needed.

Finally, after coding and testing, the feature is deployed and monitored for any issues or improvements needed.

### <span style="color:red;">Restful API</span>

is an architecture style  
defines to create HTTP services that receives HTTP request such as GET, POST, PUT, DELETE  
perform CRUD operations on the application data source  
returns JSON / XML data as response to client

### <span style="color:red;">Repository pattern</span>

Pros:

-   loosely-coupled business logic (service) & datas access
-   changing data store
-   ez for unit tesing, do not need to mock db context

Cons:

-   Increased Complexity: Introducing a repository layer adds complexity to the application, especially in smaller projects where direct data access might suffice.
-   Performance Overhead: In some cases, the additional layer of abstraction (especially with complex querying or large datasets) can impact performance.
-   Not Always Necessary: For simple CRUD (Create, Read, Update, Delete) operations, the Repository pattern might introduce unnecessary complexity compared to direct database access.

### <span style="color:red;">Code first VS Db First</span>

-   code: for newer database, smaller application / prototype-level application
-   db: if you have existing database or DB designed by DBA team, developed separately. Large application / high data-intense application

write tests first before implementation

### <span style="color:red;">SOLID</span>

5 design patterns

reduce dependencies of various classes / modules of the application

S - Single responsibility principle

O - Open-close principle

L -

I - Interface seggregaion principle

D - Dependency Inversion Principle

-   Direct Dependency: higher level modules depend on lower level modules
-   High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).
-   Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.

### <span style="color:red;">Clean architecture</span>

UI -> Core & Domian <- Infrastructure

### <span style="color:red;">Web API</span>

---



---

# Git

### <span style="color:red;">Do you have experience in GIT</span>

---
