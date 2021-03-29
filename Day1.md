# 1. 计算机基本概念和JDK的安装

## 1.1 计算机的基本概念

- 什么是计算机

笔记本、台式机、大型服务器

- 计算机的组成

计算机硬件（物质基础）：运算器、控制器（中央处理单元CPU），存储器（内部存储器、外部存储器），输入设备（鼠标、键盘），输出设备（显示器、打印机）

计算机软件：系统软件（windows, mac, linux, android, ios），应用软件（JDK）

- 计算机语言（与计算机进行交互）

机器语言：由0和1组成，阅读和编写很麻烦

汇编语言：由特殊符号组成，用来标识0和1，计算机不能直接识别，编码量依然很大

高级语言：使用英语编写，大大降低了开发的难度，例如Java, C, C++

- 软件开发

借助开发工具与计算机语言制作软件的过程。

- 计算机常用功能键

Tab：缩进

Shift：上档键

Ctrl：控制键

Windows：调出系统菜单

Alt：调用窗口菜单

Space：空格键

Enter：换行键

- 计算机常用快捷键

Ctrl + **

## 1.2 JDK相关的基本概念

- JDK

Java Development Kit, Java开发工具包, 包括开发Java程序所需要的工具及JRE

用于开发Java程序

- JRE

Java Runtime Environment, Java运行环境, 包含运行Java程序所需要的核心类库和JVM

用于运行Java程序

- JVM

Java Virtual Machine, Java虚拟机

将Java程序翻译成机器语言，交给底层操作系统执行，并保证运行效果，实现Java程序的跨平台性

- Java跨平台性原理

可以在windows, linux, mac系统中运行，安装相应版本的JVM

Java程序可以跨平台，，由JVM保证，但是JVM本身不能跨平台的

- JDK的安装配置

https://www.oracle.com/java/technologies/javase-jdk16-downloads.html

配置环境变量：新建一组系统变量JAVA_HOME, 在Path变量中加入%JAVA_HOME%, 便于在版本更新时使用

测试：在命令行输入java或者javac


# 2. Java入门


开发工具：JDK, 集成开发工具IDEA（集程序编写、编译、测试、运行、调试等多项功能为一体的开发软件，需要将JDK集成到IDEA）


## 2.1 第一个JAVA程序

- IntelliJ IDEA

Java程序可以写在普通记事本、高级记事本Notepad++, 也可以写在集成开发环境IDE（eclipse, IntelliJ IDEA）



