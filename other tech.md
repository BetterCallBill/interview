### <span style="color:red;">你喜欢做前端多一点还是后端多一点？</span>

Backend

### <span style="color:red;">developer 不分前后端有什么好处？</span>

"Being proficient across both front-end and back-end development offers several advantages:

Versatility: Can work on full-stack projects independently or collaborate seamlessly with team members across different layers of the application.

Understanding the Full Picture: Gain insights into the entire development lifecycle, from user interface design and client-side interactions to server-side logic and database management.

Problem-solving: Able to diagnose and troubleshoot issues comprehensively, whether they arise in the user interface, business logic, or data layer.

Efficiency: Streamline development processes and reduce dependencies on others for integration tasks or bug fixes.

Career Growth: Opens opportunities for roles requiring broader technical expertise and leadership in software development projects."

### <span style="color:red;">What is good code and what is bad code, in your opinion?</span>

Good code is clean, easy to read, and maintainable. It follows best practices, is well-documented, and has meaningful variable names. Good code is also efficient and performs well.

Bad code, on the other hand, is messy, hard to understand, and difficult to maintain. It often lacks comments, has poor naming conventions, and is inefficient. In short, good code makes life easier for developers, while bad code creates headaches and problems.

### <span style="color:red;">一些关于 OOP 的理解，自己在写代码时候会怎么遵守 oop 的原则</span>

OOP, or Object-Oriented Programming, involves organizing code into objects with properties and methods.

I follow OOP principles by using encapsulation to protect data, inheritance to reuse code, and polymorphism to allow flexibility. I ensure each class has a single responsibility, making the code easier to maintain and extend. These practices help me write clean, efficient, and scalable code.

### <span style="color:red;">How to deal with conflicts / 怎么处理冲突啊，怎么跟不同 role 的人交流，怎么去 debug / 如何和同事进行合作?</span>

How do you deal with conflicts, communicate with different roles, debug, and collaborate with colleagues?

To deal with conflicts, I listen actively and find common ground. I communicate clearly and respectfully with different roles, ensuring everyone understands the goals.

For debugging, I follow a systematic approach: reproducing the issue, analyzing logs, and isolating the problem.

Collaboration involves regular check-ins, sharing knowledge, and being open to feedback. This ensures a productive and harmonious work environment.

### <span style="color:red;">你未来的规划是什么？/ 你未来打算再学一门什么样的语言？/ 未来 5-10 年的规划</span>

3-Year Plan to Become a Senior Software Architect

Year 1: Skill Building and Foundations

-   Master .NET Core: Deepen knowledge in .NET Core, ASP.NET Core, and C#.
-   Learn Architecture Basics: Study design patterns, SOLID principles, and basic architecture concepts.
-   Certifications: Obtain certifications like Microsoft Certified: Azure Developer Associate.
-   Mentorship: Seek guidance from senior developers.

Year 2: Broadening Experience and Leadership

-   Full-Stack Development: Gain skills in front-end (React/Angular) and databases (SQL/NoSQL).
-   Cloud Expertise: Learn Azure/AWS, focusing on cloud architecture.
-   Architectural Design: Participate in designing small projects.
-   Leadership Roles: Lead features and mentor junior team members.

Year 3: Specialization and Transition

-   Advanced Architecture: Specialize in areas like microservices or cloud architecture.
-   Project Leadership: Manage larger projects, honing communication and leadership skills.
-   Certifications: Achieve advanced certifications, e.g., Azure Solutions Architect Expert.
-   Networking and Learning: Attend conferences, write technical blogs, and continuously update skills.

### <span style="color:red;">你如何理解 integrity?</span>

Integrity means consistently adhering to strong ethical principles and professional standards. As a software developer, it involves writing honest, maintainable code, respecting user privacy, being transparent about capabilities and limitations, and ensuring security. Integrity fosters trust, collaboration, and quality in software development, ensuring reliable and ethical products.

# PROJECT

### <span style="color:red;">Experience</span>

CRM

Project Overview: "I worked on a web-based CRM system aimed at improving customer relationship management for a mid-sized company. The project involved building features to track customer interactions and automate sales processes."

Your Role: "As a backend developer, I was responsible for designing and implementing APIs using .NET Core, integrating third-party services, and optimizing database queries."

Challenges and Solutions: "We faced performance issues due to high database load. I optimized the queries and implemented caching strategies, which improved response times by 40%."

Achievements and Impact: "My optimizations reduced server costs by 30% and enhanced user satisfaction. The new features I developed also streamlined the sales team's workflow."

Teamwork and Collaboration: "I worked closely with frontend developers, ensuring seamless integration of APIs. I also coordinated with the QA team to ensure thorough testing."

Learning and Growth: "I learned advanced .NET Core features and improved my database optimization skills. This project taught me the importance of efficient code and proactive problem-solving."

### <span style="color:red;">Challenges and Solutions</span>

**Challenge 1: Integrating Authentication Across Frontend and Backend**

Difficulty:  
Implementing a secure authentication mechanism that works seamlessly between the React.js frontend and the ASP.NET Core backend.

Solution:  
JWT Authentication: Used JWT for stateless authentication. The backend generates a JWT upon successful login, which the frontend stores in local storage or cookies.

Protected Routes: Implemented protected routes in React to ensure that only authenticated users can access certain parts of the application.  
Token Renewal: Managed token expiration and renewal using interceptors in Axios to automatically refresh tokens when necessary.

**Challenge 2: State Management in React**

Difficulty: Managing complex state, especially when it comes to the shopping cart and user sessions.

Solution:
Redux: Used Redux to manage the global state of the application. This helped keep the state consistent and made it easier to manage data flow between components.
Middleware: Implemented middleware to handle asynchronous actions, such as API calls for fetching book data and managing the shopping cart.

**Challenge 3: Handling Asynchronous Data Fetching and Error Handling**

Difficulty: Ensuring smooth user experience with asynchronous data fetching and proper error handling.
Solution:

Axios for API Calls: Used Axios for making HTTP requests to the backend. Configured interceptors for handling responses and errors globally.
Loading States: Implemented loading states and spinners to provide feedback to users while data is being fetched.
Error Boundaries: Used React's error boundaries to catch and display errors gracefully without crashing the whole application.
Challenge 4: Optimizing Performance
Difficulty: Ensuring the application performs well under load, especially when handling large datasets like book catalogs.

Solution:  
Lazy Loading: Implemented lazy loading for components and images to improve initial load times.
Pagination and Infinite Scroll: Used pagination for book listings and implemented infinite scroll for a better user experience.
Caching: Implemented caching strategies on the backend to reduce the number of database calls for frequently accessed data.

**Scalability**
Challenge: Enterprise applications must handle a large number of users and a high volume of transactions without performance degradation.

Solutions:

Microservices Architecture: Break down the application into smaller, manageable services that can be developed, deployed, and scaled independently.
Load Balancing: Distribute the incoming network traffic across multiple servers to ensure no single server becomes a bottleneck.
Caching: Implement caching strategies at various levels (e.g., database, application, and front-end) to reduce the load on the database and improve response times.
Auto-scaling: Use cloud services that provide automatic scaling based on the traffic load.

**User Experience**
Challenge: Creating a user-friendly interface that meets the needs of diverse user groups within an enterprise.

Solutions:
User-Centered Design: Follow user-centered design principles, involving end-users in the design and development process to ensure the application meets their needs.
Accessibility: Ensure the application is accessible to all users, including those with disabilities, by following accessibility standards.
Consistent UI/UX: Maintain a consistent user interface and experience across the application to make it intuitive and easy to use.
Performance Optimization: Optimize the application for performance to ensure fast load times and smooth interactions.

### <span style="color:red;">Share your experience about you previous projects? / 你平时的工作主要负责什么？</span>

-   angular plugin
-   property management

### <span style="color:red;">What is your most successful project?</span>

-   website

### <span style="color:red;">What to do if your project has errors? How to avoid it?</span>

If my project has errors, I first identify the problem by reviewing error messages and logs. I then isolate the issue by testing small parts of the code to find the source. Once identified, I research the error, often checking documentation or forums, and then apply a fix.

To avoid errors, I follow best practices:

-   Write clean, modular code.
-   Use version control (like Git) to track changes.
-   Write unit tests to catch issues early.
-   Perform code reviews to get feedback from peers.
-   Keep dependencies and tools updated to avoid compatibility issues.

By being systematic and proactive, I can quickly resolve and minimize errors in my projects.

### <span style="color:red;">How do you start with a project already started and how to deal with other developers' source code?</span>

-   For the entire project:
    If there is a documentation then that would be a good place to start with. Normally I would start by the design docs, to get a big picture of the project architecture.  
    Before I read the code, I actually would run it first.
    If I must read the code, I would like to have someone walk me through it rather than read it by myself coz that would be more efficient.
-   For specific function:
    read git commit / pull request

### <span style="color:red;">What is Quality Control?</span>

Quality Control in software development refers to the systematic processes and techniques used to ensure that software products meet predefined quality standards and requirements. It involves activities such as rigorous testing, code reviews, and quality assurance measures to identify and rectify defects early in the development lifecycle. By maintaining high standards of quality throughout the software development process, Quality Control aims to deliver reliable, secure, and user-friendly software solutions that meet customer expectations and adhere to industry best practices.

### <span style="color:red;">What is Version Control?</span>

### <span style="color:red;">OOP vs Functional Programming (FP)</span>

Object-Oriented Programming (OOP) focuses on modeling software entities as objects with state and behavior, promoting code reusability and modularity through classes and inheritance.

Functional Programming (FP) treats computation as the evaluation of mathematical functions, emphasizing immutability, higher-order functions, and function composition for concise and predictable code.

OOP emphasizes stateful objects and encapsulation, while FP prioritizes immutable data and avoids side effects, making it suitable for parallelism and complex transformations. Both paradigms offer distinct approaches to solving software design and implementation challenges.

### TDD - Test Driven Development

---

# Agile

### <span style="color:red;">agile 的理解？agile 的好处坏处？</span>

"Agile is an approach in software development where teams work in short cycles called sprints to deliver frequent, incremental releases. It emphasizes flexibility, collaboration, and continuous improvement.

Pros: Agile enables quicker adaptability to changing requirements, fosters better teamwork and communication, and delivers value to users faster.

Cons: It can be challenging to maintain predictability in project timelines, especially with evolving requirements. Also, Agile requires active involvement from stakeholders, which can sometimes lead to conflicting priorities."

In essence, Agile is about being adaptive, collaborative, and iterative in software development, aiming to deliver customer value efficiently.

### <span style="color:red;">你平时的 agile team 里有哪些人？ / 你的 team 里有哪些 role</span>

### <span style="color:red;">How do you commit your code? / 你平时代码如何 merge 到 master？（git rebase，如何 pick squash， pull request）</span>

### <span style="color:red;">你如何做 responsive design</span>

"Responsive design ensures that a website or application adapts to different screen sizes and devices. Here’s how I approach it:

Flexible Grids: Use CSS Grid or Flexbox to create layouts that adjust based on screen size.

Media Queries: Implement CSS media queries to apply styles based on device characteristics like screen width.

Viewport Meta Tag: Set the viewport meta tag in HTML to ensure content scales properly on mobile devices.

Images and Media: Use responsive images and scalable vector graphics (SVGs) that adjust based on screen resolution.

Testing: Regularly test across various devices and screen sizes using browser developer tools or dedicated testing platforms.

### <span style="color:red;">如何 prioritise 工作</span>

Prioritizing work involves assessing tasks based on deadlines, impact on project goals, and urgency.

I start by understanding the requirements and deadlines. Then, I prioritize tasks that are critical to meeting immediate goals or have dependencies.

I use tools like task lists or project management software to keep track of priorities and adjust them as needed based on project progress.

### <span style="color:red;">你遇到困难怎么办 / 遇到解决不了的问题怎么办</span>

When faced with difficulties or a problem I can't solve, I approach it by first breaking down the problem into smaller parts to understand it better. I research online resources, documentation, or seek advice from colleagues or mentors. If needed, I'm not afraid to ask for help to gain new perspectives or insights. Persistence and collaboration often lead to finding effective solutions

### <span style="color:red;">遇到快到 deadline 了，工作没做完怎么办</span>

If nearing a deadline with unfinished work, I prioritize tasks based on impact and urgency. I focus on completing essential features or critical aspects first, ensuring they meet minimum requirements. I communicate with my team or stakeholders about the progress and any potential adjustments needed. I also consider if additional resources or adjustments to scope can help meet the deadline without compromising quality.

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
