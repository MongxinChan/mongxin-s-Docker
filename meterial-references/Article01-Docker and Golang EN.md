# Article 01: Docker and Golang

[Click here to switch off Chinese Version](./Article01-Docker%20and%20Golang.md)

## Introduction to Containers

Images allow you to package all system-level dependencies into a single file. All containers share a single **Kernel**, which means you can run containers for various Linux distributions on top of that same Kernel.

![alt text](https://cdn.jsdelivr.net/gh/MeritXin/img@master/20260421200618473.png)

Docker containers have three main characteristics:

* **Lightweight:** Containers on the same **host machine** share the system Kernel. This allows them to start instantly and use very little memory. Images are built using a **layered file system**, which allows them to share common files, improving disk efficiency and download speeds.
* **Open:** Docker containers are based on open standards, which allows them to run on all major Linux distributions and Windows operating systems.
* **Secure:** Containers isolate applications from one another, providing an additional layer of security for all your apps.

---

**Virtual Machines (VMs)** include the user’s program, necessary libraries, and an entire **Guest Operating System**.

![alt text](https://cdn.jsdelivr.net/gh/MeritXin/img@master/20260421200618474.png)

**Containers** include the user’s program and all its dependencies, but they share the Kernel with other containers.

![alt text](https://cdn.jsdelivr.net/gh/MeritXin/img@master/20260421200618475.png)

### Three Key Advantages:
1.  Speed up development.
2.  Empower creativity.
3.  Eliminate environment inconsistency ("It works on my machine" issues).

## How Containers Work

Docker images can be stored in **Docker Hub**. Team members can manage and share these images through Docker Store or Docker Hub. All changes and version history are visible across the organization, making it easy to share and reference containers.

Docker also allows you to **dynamically change applications**. You can quickly scale up to increase capacity or fix bugs in real-time. Because Docker containers can **start and stop in seconds**, they can rapidly scale out to handle high-concurrency traffic spikes whenever necessary.

## Golang

**Go** (or Golang) is a statically typed, compiled, and concurrent programming language developed by Google. It also features built-in **Garbage Collection (GC)**.

While Go's syntax is similar to C, there are notable differences. For example, variable declarations are structured differently, and `for` loops or `if` statements do not require parentheses. Go's concurrency model is based on **Communicating Sequential Processes (CSP)**. It draws inspiration from languages like Occam and Limbo but also features elements of Pi-calculus, such as **channel** communication.

Compared to C++, Go does not include features like exception handling, inheritance, generics, assertions, or virtual functions. Instead, it provides language-level support for **slices**, concurrency, channels, garbage collection, and **interfaces**.

While Google has remained open toward the idea of generics, they have generally maintained a negative stance toward assertions and have defended the decision not to provide type inheritance. Unlike Java, Go has built-in support for **associative arrays** (also known as hash tables or dictionaries), treating them as a fundamental type just like strings.

```golang
package main

import "fmt"

func main(){
    fmt.Println("Hello, World")
}
```

---