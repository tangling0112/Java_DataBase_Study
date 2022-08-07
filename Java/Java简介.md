# 一 Java概述

## 1 Java语言的特点

## 2 Java语言运行机制与过程

## 3 Java垃圾回收机制

## 4 内存泄漏与内存溢出

# 二 Java安装与环境配置

## 1 `JRE`与``JDK``

### `JRE`

> `JRE`包含`JVM`与`Java`允许必须的核心类库,如果想运行`Java`程序就需要安装`JRE`,但是仅仅只安装`JRE`是无法让我们自己来设计`Java`程序的

### `JDK`

> `JDK`中包含了`JRE`,并且还包含了用于`Java`开发人员使用的开发工具
>
> - 编译工具(`javac.exe`)
> - 打包工具`jar.exe`

<img src="F:\A_Java_DataBase_Study_FIle\Java\重点汇总.assets\image-20220714211528904.png" alt="image-20220714211528904" style="zoom:67%;" />

<img src="F:\A_Java_DataBase_Study_FIle\Java\重点汇总.assets\image-20220714211552658.png" alt="image-20220714211552658" style="zoom: 65%;" />

### `Java`安装流程

- `JDK`的安装
- 环境变量的配置
  - 配置`JDK`的`bin`目录的`PATH`环境变量
    - 直接配置或`%JAVA_HOME%`方式配置

### `JDK`的`bin`目录部分程序介绍

- `javac.exe`:编译工具
- `java.exe`:对编译好的程序进行运行的工具
- `javadoc.exe`:生成以网页形式呈现的文档是使用

### `JDK`的`include`文件夹

> 其中存放有一些`C`语言形式的代码,用于支持我们的`Java`的运行

### `JDK`的`lib`文件夹

> 其中存放我们的`.jar`格式的类库

### `JDK`的`src.zip`文件

> 其中存放了一些`.jar`格式存储的类库

## 三 `Java`程序从编译到运行的流程解析

- `Java`程序编写在`.java`后缀的文件中
- `Java`通过调用`javac.exe`程序对我们的`.java`程序文件进行编译
  - **编译生成`.class`后缀的字节码文件**
- `Java`通过调用`java.exe`程序对我们的`.class`字节码文件在`JVM`上进行运行

<img src="F:\A_Java_DataBase_Study_FIle\Java\重点汇总.assets\image-20220714214419233.png" alt="image-20220714214419233" style="zoom: 80%;" />

### 字节码文件介绍

