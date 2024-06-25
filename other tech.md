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

# Projects

### Share your experience about you previous projects? / 你平时的工作主要负责什么？

-   angular plugin
-   property management

### What is your most successful project?

-   website

### What to do if your project has errors? How to avoid it? / Any challenges in project?

### How do you start with a project already started and how to deal with other developers' source code?

-   For the entire project:
    If there is a documentation then that would be a good place to start with. Normally I would start by the design docs, to get a big picture of the project architecture.  
    Before I read the code, I actually would run it first.
    If I must read the code, I would like to have someone walk me through it rather than read it by myself coz that would be more efficient.
-   For specific function:
    read git commit / pull request

### What is Quality Control?

### What is Version Control?

### OOP vs 面向函数编程

### TDD - Test Driven Development

---

# DESIGN PATTERN

### 设计模式和框架. 单例，工场，委托，订阅模式的例子

### 软件开发周期，当有新的 feature 的时候是采用的什么流程, 拿到 task 具体怎么拆分，什么思路

### Restful API

is an architecture style  
defines to create HTTP services that receives HTTP request such as GET, POST, PUT, DELETE  
perform CRUD operations on the application data source  
returns JSON / XML data as response to client

### Repository pattern

-   pros:
    loosely-coupled business logic (service) & datas access  
    changing data store  
    ez for unit tesing, do not need to mock db context

-   cons:

### Code first VS Db First

-   code: for newer database, smaller application / prototype-level application
-   db: if you have existing database or DB designed by DBA team, developed separately. Large application / high data-intense application

write tests first before implementation

### SOLID

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

### Clean architecture

UI -> Core & Domian <- Infrastructure

### Web API

---

# Agile

agile 的理解？agile 的好处坏处？

### 你平时的 agile team 里有哪些人？

### Feature plan / 你未来的职业规划是什么？

### How do you commit your code? / 你平时代码如何 merge 到 master？（git rebase，如何 pick squash， pull request）

一个 agile team 有多少人会比较合适
你的 team 里有哪些 role
你如何做 unit test
你如何做 responsive design

developer 不分前后端有什么好处？

如何 prioritise 工作

你遇到困难怎么办
遇到解决不了的问题怎么办
遇到快到 deadline 了，工作没做完怎么办

---

# Git

### do you have experience in GIT

---

# Others

### 你喜欢做前端多一点还是后端多一点？

### 什么是好的代码，什么是不好的代码，自己的看法。

### 一些关于 OOP 的理解，自己在写代码时候会怎么遵守 oop 的原则

### How to deal with conflicts / 怎么处理冲突啊，怎么跟不同 role 的人交流，怎么去 debug

### 你未来的规划是什么？

### 为什么选择我们公司？对于我们公司的产品有什么了解？

### 你未来打算再学一门什么样的语言？

你如何理解 integrity?
你对我们公司的 culture 有什么了解?
你认为我们为什么要 hire 你?
未来 5-10 年的规划
如何和同事进行合作?

### Any questions ? /

他们公司现在用什么技术栈，什么框架，团队里有多少人，工作模式是什么等
