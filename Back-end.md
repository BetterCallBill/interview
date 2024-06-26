# Backend (C# & SQL) Interview Questions

# C#

### <span style="color:red;">Value Types and Reference Types</span>

value type: stack  
reference type: heap  
![Alt text](https://i.stack.imgur.com/dBmFr.png)

### <span style="color:red;">struct vs class</span>

![Alt text](https://www.ottorinobruni.com/wp-content/uploads/2018/03/StructClassDifference.jpeg)

### <span style="color:red;">field vs property</span>

-   field: can't be used on Interface
-   property: capital

```c#
public class MyClass
{
    // this is a field.  It is private to your class and stores the actual data.
    private string _myField;

    // this is a property. When accessed it uses the underlying field,
    // but only exposes the contract, which will not be affected by the underlying field
    public string MyProperty
    {
        get
        {
            return _myField;
        }
        set
        {
            _myField = value;
        }
    }

    // This is an AutoProperty (C# 3.0 and higher) - which is a shorthand syntax
    // used to generate a private field for you
    public int AnotherProperty { get; set; }
}
```

![Alt text](https://miro.medium.com/v2/resize:fit:4800/format:webp/1*YSWAXo1qsKeZDCSA2OT1kw.png)

### <span style="color:red;">What are property accessors? / getter and setter</span>

-   idea of encapsulation
-   add security to fields

### <span style="color:red;">static vs const</span>

-   const:  
    is defined at compile time and cannot be changed at runtime. Constants are declared as a field, using the const keyword and must be initialized as they are declared. They are good for things that are truly constant (i.e. pi)
-   static:
    means it is a value not related to an instance, and it can be changed at run-time (since it isn't readonly).

### <span style="color:red;">Abstract vs Interface</span>

Data abstraction is the process of hiding certain details and showing only essential information to the user.
Abstraction can be achieved with either abstract classes or interfaces (which you will learn more about in the next chapter).

-   **Abstract class**: is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).
-   **Abstract method**: can only be used in an abstract class, and it does not have a body. The body is provided by the derived class (inherited from).

**Key Differences**

Abstract classes:

-   can contain implemented methods
-   can have constructors
-   can have fields and properties
-   Classes can inherit from only one abstract class
-   typically used for creating a base class for other classes to inherit from

Interface:

-   only contain method signatures
-   no constructors
-   can only have properties
-   Classes can implement multiple interfaces
-   used for defining a contract that classes must implement

**When to use**  
abstract class: when creating a base class that needs to be inherited by other classes in a class hierarchy.  
interface: if you need to define a behavior that can be implemented by multiple unrelated classes.

### Basic data structure in C#

-   Array
-   Dictionary / Map:  
    used to store key/value pairs

```c#
// create a dictionary
Dictionary<string, string> student = new Dictionary<string, string>();

// add items to dictionary
student.Add("Name", "Susan");
student.Add("Faculty", "History");

// access the value having key "Name"
Console.WriteLine(student["Name"]);

// access the value having key "Faculty"
Console.WriteLine(student["Faculty"]);

// iterate through the car dictionary
foreach (KeyValuePair<string, string> items in car)
{
    Console.WriteLine("{0} : {1}", items.Key, items.Value);
}

// change
student["Name"] = "Maruti";

// remove
student.Remove("Name");
```

-   Stack
-   Queue
-   Hashtable
-   Linked List

### <span style="color:red;">What is the difference between "continue" and "break" statements in C#?</span>

break: you can jump out of a loop \
continue: you can jump over one iteration and then resume your loop execution

### <span style="color:red;">Filter out the first 3 even numbers from the list using LINQ</span>

var temp = list.where(x => x % 2 == 0).Take(3)

### <span style="color:red;">Func & Action</span>

-   Func - non-void function
-   Action - return void function

### <span style="color:red;">Delegate</span>

---

## Multithreading programming

### <span style="color:red;">What is 'Multithreading programming'?</span>

进程 Process > 线程 Thread

### <span style="color:red;">Why we need?</span>

Multithreading can improve application performance by performing tasks concurrently.

### <span style="color:red;">When we need?</span>

-   **Multithreading programming**: 计算密集（compute-intensive，或 CPU-bound）, such as image processing and numerical simulations
-   **Asynchronous programming**: I/O 密集（I/O-intensive，或 I/O-bound）, such as Making web requests, interacting with other services, and other I/O-bound operations as reading from and writing to files or databases

### <span style="color:red;">How to write?</span>

-   Multithreading

```c#
class ThreadTest
{
  static void Main()
  {
    // 创建新线程
    Thread t = new Thread (WriteY);

    // 启动新线程，执行WriteY()
    t.Start();

    // 同时，在主线程做其它事情
    for (int i = 0; i < 1000; i++) Console.Write ("x");
  }

  static void WriteY()
  {
    for (int i = 0; i < 1000; i++) Console.Write ("y");
  }
}
```

-   Async / Await

### <span style="color:red;">ThreadPool 线程池</span>

异步编程默认使用线程池

### <span style="color:red;">Race condition</span>

A race condition happens when 2 or more threads are trying to access and modify the same variable  
race condition（竞态条件）是指在多线程或多进程程序中，由于执行顺序不确定或者操作系统对共享资源的调度方式不同，导致程序的结果出现不可预期的错误。

### <span style="color:red;">What programming locks have you used</span>

排它锁/互斥锁 exclusive lock

```c#
class ThreadSafe
{
  static bool done;
  // add lock
  static readonly object locker = new object();

  static void Main()
  {
    new Thread (Go).Start();
    Go();
  }

  static void Go()
  {
    lock (locker)
    {
      if (!done) { Console.WriteLine ("Done"); done = true; }
    }
  }
}

```

### <span style="color:red;">dead lock</span>

---

## Async / await programming

---

## C# new feature

C# version 7.0:  
Tuple types (C# reference)

C# version 8:

-   Default interface methods
-   Nullable reference types

C# version 9:  
Record Types

C# version 10:

-   Global using directives

C# version 11:

-   Raw string literal

C# version 12:

-   Primary constructors
-   Collection Literals

---

# .NET

### <span style="color:red;">Dependency Inversion Principle - D in SOLID</span>

-   Direct Dependency: higher level modules depend on lower level modules
-   High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).
-   Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.

### <span style="color:red;">Inversion of Control</span>

is a design principle in which a software component is designed to receive its dependencies from an external source, rather than creating them itself

### <span style="color:red;">Dependency Injection</span>

is a design pattern, a technique for achieving 'Inversion of Control' between clients and dependencies

### <span style="color:red;">Transient, Scoped, Singleton</span>

-   Transient: per injection
    short-lived services

-   Scoped: per scope (browser request)  
    for db connection

-   Singleton: for entire application lifetime  
    store data temporarily, such as cache, in memory collection

## EF Core

### Fluent API

### .Net new features

---

# SQL

### <span style="color:red;">SQL vs NoSQL</span>

The five critical differences between SQL and NoSQL are:

SQL databases are relational  
NoSQL databases are non-relational

SQL databases use structured query language (SQL) and have a predefined schema  
NoSQL databases have dynamic schemas for unstructured data

SQL databases are vertically scalable  
NoSQL databases are horizontally scalable

SQL databases are table-based  
NoSQL databases are document, key-value, graph, or wide-column stores

SQL databases are better for multi-row transactions  
NoSQL is better for unstructured data like documents or JSON

SQL:

-   Build an application structured around a relationship between data tables
-   Ensure your data is consistent across tables
-   NOT the best choice regarding flexibility or scaling

NoSQL:

-   uses flexible schemas for unstructured data storage
-   gives you more ability to scale your project as needed & less control over consistency and data relationships
-   You need high performance, particularly read performance
-   You need high availability (HA)

在频繁进行数据库操作时，选择合适的数据库是非常重要的。根据实际需求和应用场景，可以考虑以下几种数据库：

关系型数据库（RDBMS）：  
关系型数据库以表格的形式存储数据，使用 SQL 语言进行操作。常见的关系型数据库包括 MySQL、Oracle、SQL Server 等。优点是数据结构清晰，支持复杂的查询操作，适用于需要事务支持和数据一致性的场景。

非关系型数据库（NoSQL）：  
非关系型数据库采用键值对、文档、列族等非结构化的方式存储数据，不需要使用 SQL 语言进行操作。常见的非关系型数据库包括 MongoDB、Redis、Cassandra 等。优点是扩展性好，能够处理海量数据和高并发请求，适用于需要灵活性和高性能的场景。

内存数据库（In-Memory Database）：  
内存数据库将数据存储在内存中，读写速度非常快。常见的内存数据库有 Redis、Memcached 等。优点是响应速度快，适用于对读写性能要求较高的场景，如缓存、会话管理等。

图数据库（Graph Database）：  
图数据库以图的形式存储数据，适用于处理复杂的关系和网络数据。常见的图数据库有 Neo4j、ArangoDB 等。优点是能够高效地处理复杂的关系查询，适用于社交网络、推荐系统等场景。

在选择数据库时，需要综合考虑以下几个方面：

数据规模：  
根据数据量的大小选择适合的数据库，关系型数据库适合存储结构化数据，非关系型数据库适合存储半结构化或非结构化数据。

访问模式：  
根据应用的读写比例选择适合的数据库，如果读操作较多，可以选择内存数据库或缓存数据库；如果写操作较多，可以选择关系型数据库或非关系型数据库。

数据一致性：  
根据业务需求选择适合的数据库，如果需要强一致性和事务支持，可以选择关系型数据库；如果对一致性要求较低，可以选择非关系型数据库。

扩展性和性能：  
根据应用的并发量和数据规模选择适合的数据库，非关系型数据库和内存数据库在扩展性和性能方面具有优势。

### <span style="color:red;">SQL 的三种事务安全级别</span>

Transactions (事务)

-   Dirty Read 脏读
-   NonRepeatable Read 不可重复读
-   Phantom Read 幻读

Transaction Isolation Levels

-   Read uncommitted 未提交
-   Read committed 读提交
-   Repeatable read 可重复读
-   Serializable 串行化

---

# OAuth 2.0 & JWT

### 如果设计一个系统, 前端和后端怎么安排, 在安全方面, 如果使用 jwt, 那么 jwt 会不会有 csrf concern, 如果明文被劫持，你有什么办法解决这个问题吗?

JWT (JSON web token) is a compact and self-contained object for securely transmitting information between parties as a JSON object

Unlike Cookie or Session, JWT/Token has NO csrf concern

所有的 token 都有这个问题啊，有个简单的解决方案就是签发 token 的时候把用户的 ip 也放到 jwt 的 payload 里，每次交易 token 的同时也校验 ip

最極端的情況也只有用戶本人的電腦被人入侵並盜取 Token
不過這種漏洞不容易發生大規模的危害，頂多就是 1. 2 個用戶會發生，因解析及簽發 JWT 的 Secret 仍在你的 Server 上
要防範的話可能得紀錄使用者每次登入的 IP，若有差異即通知使用者，由使用者決定是否要加強帳號安全性

![Alt text](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9d4df1ea327940c685be6c8970708a20~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

---

# DOCKER

### What is Docker? docker image, file

container

---

# TEST

### How to test / 你如何做 unit test

Front-end: Jasmine + Karma
Back-end: xUnit test






---

# MICROSERVICES

### pros cons，可能和他们保险业务的结合，聊了一下 message queue，聊了一下 serverless

### message queue

---

# Code chanllenge

给了一个类似 youtube 主页的截图，让我说整体 react 布局思路以及参数传递

Leetcode 第 1 题 和 第 121 题

Worst case Big O for quick sort algorithm

如何优化数据库性能

如何优化后端性能

如何优化高并发请求

如过有一个组巨大的数据要取到前端（EG：10w 条）你会怎么处理优化它。

aws 和 azure 的经验
