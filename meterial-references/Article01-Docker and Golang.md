# Article 01: Docker and Golang

[点此切换到英文版](./Article01-Docker%20and%20Golang%20EN.md)

## 介绍容器

镜像可以把系统级依赖都打包成一个文件，所有的容器会共享一个Kernel，因此在同一个Kernel下可以运行各种Linux发行版的容器。

![alt text](https://cdn.jsdelivr.net/gh/MeritXin/img@master/20260421200618473.png)

Docker容器具有以下3个特点。

- 轻量级：在同一台宿主机上的容器共享系统Kernel，这使得它们可以迅速启动而且占用内存极少。镜像是以分层文件系统构造的，这可以让它们共享相同的文件，使得磁盘使用率和镜像下载速度得到提高。

- 开放：Docker 容器基于开放标准，这使得Docker 容器可以运行在主流Linux 发行版和Windows操作系统上。

- 安全：容器将各个应用程序隔离开来，这给所有的应用程序提供了一层额外的安全防护。

---

虚拟机包含**用户的程序**，**必要的函数库**和整个**客户操作系统**

![alt text](https://cdn.jsdelivr.net/gh/MeritXin/img@master/20260421200618474.png)

容器包含用户的程序和所有的依赖，但是容器之间是共享Kernel的。

![alt text](https://cdn.jsdelivr.net/gh/MeritXin/img@master/20260421200618475.png)

---
三个优点：
1. 加速开发
2. 赋能创造力
3. 消除环境不一致

## 容器的工作

Docker 镜像可以存储到Docker Hub中，团队成员可以通过Docker Store、Docker Hub管理分享镜像。所有的变化和历史都可以在整个组织间查看，且可以简单分享引用容器。

而 Docker 允许**<u>动态地改变应用程序</u>**，可以通过扩容快速提高应用程序的能力并及时修复缺陷。Docker容器可以**秒级启动**和**停止**，因此，它可以在需要的时候快速扩容出大量的应用程序，扛住并发的压力。

## Golang

`Go` 是Google开发的一种静态强类型、编译型、并发型并具有垃圾回收功能的编程语言。

Go语言的语法虽然接近C语言，但还是有一些不同，比如两者对于变量的声明是不同的，且Go语言中的for循环和if判断语句不需要用小括号括起来。Go语言的并行模型是以东尼·霍尔的通信顺序进程（CSP）为基础的，并采取了类似模型的其他语言（包括Occam和Limbo）​，但它也具有Pi运算的特征，比如通道传输。

与C++相比，Go语言并不包括如异常处理、继承、泛型、断言、虚函数等功能，但增加了slice型、并发、管道、垃圾回收、接口（Interface）等特性的语言级支持。

当然，Google对于泛型的态度还是很开放的，但在该语言的常见问题列表中，对于断言的存在，则持负面态度，同时也在为自己不提供类型继承辩护。不同于Java，Go语言内嵌了关联数组（也称为哈希表（Hash）或字典（Dictionary）​）​，就像字符串类型一样。

```golang
package main

import "fmt"

func main(){
    fmt.Prtinln("Hello,World")
}
```