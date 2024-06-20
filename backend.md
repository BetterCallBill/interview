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

### What is the difference between "continue" and "break" statements in C#?

break: you can jump out of a loop \
continue: you can jump over one iteration and then resume your loop execution

### Filter out the first 3 even numbers from the list using LINQ

var temp = list.where(x => x % 2 == 0).Take(3)

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

### <span style="color:red;">Func & Action</span>

-   Func - non-void function
-   Action - return void function

---

### <span style="color:red;">Delegate</span>

---

## C# new feature

---

# .NET

### Dependency Inversion Principle - D in SOLID

-   Direct Dependency: higher level modules depend on lower level modules
-   High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).
-   Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.

### Inversion of Control

is a design principle in which a software component is designed to receive its dependencies from an external source, rather than creating them itself

### Dependency Injection

is a design pattern, a technique for achieving 'Inversion of Control' between clients and dependencies

### Transient, Scoped, Singleton

-   Transient: per injection
    short-lived services

-   Scoped: per scope (browser request)  
    for db connection

-   Singleton: for entire application lifetime  
    store data temporarily, such as cache, in memory collection

## EF Core

### Fluent API

---

# SQL

### 关系型数据库和非关系型数据库的区别, 如果使用时写操作多于读操作，应该选用哪个数据库。 sql 的三种事务安全级别。

---

# OAuth 2.0, JWT

### 如果设计一个系统, 前端和后端怎么安排, 在安全方面, 如果使用 jwt, 那么 jwt 会不会有 csrf concern, 如果明文被劫持，你有什么办法解决这个问题吗?

---

# DOCKER

### What is Docker? docker image, file

---

# TEST

### How to test

xUnit test

---

# MICROSERVICES

### pros cons，可能和他们保险业务的结合，聊了一下 message queue，聊了一下 serverless

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
