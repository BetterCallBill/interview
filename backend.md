# Backend (C# & SQL) Interview Questions

# C#

### Value Types and Reference Types

![Alt text](https://i.stack.imgur.com/dBmFr.png)
value type: stack
reference type: heap

### struct vs class

![Alt text](https://www.ottorinobruni.com/wp-content/uploads/2018/03/StructClassDifference.jpeg)

### field vs property

![Alt text](https://miro.medium.com/v2/resize:fit:4800/format:webp/1*YSWAXo1qsKeZDCSA2OT1kw.png)

field:

-   can't be used on Interface
    property:
-   capital

### static vs const

### What are property accessors? / getter and setter

-   idea of encapsulation
-   add security to fields

### basic data structure in C#

### What is the difference between "continue" and "break" statements in C#?

break: you can jump out of a loop \
continue: you can jump over one iteration and then resume your loop execution

### Filter out the first 3 even numbers from the list using LINQ

var temp = list.where(x => x % 2 == 0).Take(3)

### race condition

## Thrashing

## Multi threading programming

## what programming locks have you used

Multi threading programming

## dead lock

## C# new feature

## map

## unordered map

# Design pattern

### 设计模式和框架. 单例，工场，委托，订阅模式的例子， 问了依赖注入的概念

### 软件开发周期，当有新的 feature 的时候是采用的什么流程， 拿到 task 具体怎么拆分，什么思路

### Restful API;

# SQL

### 关系型数据库和非关系型数据库的区别， 如果使用时写操作多于读操作，应该选用哪个数据库。 sql 的三种事务安全级别。

---

# OAuth 2.0, JWT

### 如果设计一个系统， 前端和后端怎么安排， 在安全方面， 如果使用 jwt， 那么 jwt 会不会有 csrf concern， 如果明文被劫持，你有什么办法解决这个问题吗。

# Docker

### Docker 的基本概念， docker image， file

# Test

### How to test

# microservices

### pros cons，可能和他们保险业务的结合，聊了一下 message queue，聊了一下 serverless

# Code chanllenge

给了一个类似 youtube 主页的截图，让我说整体 react 布局思路以及参数传递

Leetcode 第 1 题 和 第 121 题

Worst case Big O for quick sort algorithm

如何优化数据库性能

如何优化后端性能

如何优化高并发请求

如过有一个组巨大的数据要取到前端（EG：10w 条）你会怎么处理优化它。

aws 和 azure 的经验
