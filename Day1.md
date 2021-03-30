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


## 2.1  IntelliJ IDEA

Java程序可以写在普通记事本、高级记事本Notepad++, 也可以写在集成开发环境IDE（eclipse, IntelliJ IDEA）

## 2.2 HelloWorld程序

一个project = 一个java程序

在src中创建类（java程序的最小单位是类，一个java程序至少拥有一个类）

在类中创建main方法（java程序的入口）

- project中各个目录的作用

.idea和.iml是配置文件，可以隐藏

.src存放源代码，即后缀为.java的文件

.out为程序输出目录，java程序运行的时候，自动生成字节码文件（编译），即.class文件

External Libraries为扩展类库，即java程序编写和运行所依赖的JDK中的类

## 2.3 java程序开发与运行原理

源文件.java --javac.exe编译--> 字节码文件.class --java.exe运行--> 控制台输出

javac.exe和java.exe是jdk中的命令

## 2.4 IDEA配置

file --> setting --> editor

font

color schema

file encodings: global encoding, project encoding, default encoding均设置为UTF-8，勾选transparent native-to-ascii convertion（.properties文件不会中文乱码）

file types: 隐藏.iml和.idea配置文件

## 2.5 IDEA常用快捷键

查看println()源代码：ctrl+B或者ctrl+单击

复制选中的内容：ctrl+D

删除选中的内容：ctrl+Y

通过类名定位文件：ctrl+n, 在搜索框中输出

注释：ctrl+/

格式化：ctrl+alt+L

退回上次操作位置：ctrl+alt+←

前进到下一个操作位置：ctrl+alt+→

移动代码行：shift+alt+上下箭头

## 2.6 java语言编码规范

大括号成对、对齐写（右大括号）

左大括号前面有空格

大括号中代码缩进

方法块和程序之间要有空行

并排语句加空格（;表示语句的结束，在;后面加空格）

运算符两侧加空格


# 3. java常量、变量

## 3.1 注释

用于介绍、解释说明程序；帮助调试错误（通过将部分代码注释掉）

单行注释 //

多行注释 /*  */

文档注释（对类和方法做解释） /**  */

## 3.2 关键字

被java语言赋予特定含义的单词

组成关键字的字母全部小写，有特殊颜色标记

- 用于定义数据类型的关键字

class interface enum @interface byte short int long char float double boolean void 

- 用于定义数据类型值的关键字

true false null

- 用于定义流程控制的关键字

if else switch case default for while do break continue return

-  用于定义访问权限修饰符的关键字

public protected private

- 用于定义类、函数、变量修饰符的关键字

abstract final static synchronized

- 用于定义类与类之间关系的关键字

extends implements

- 用于定义建立实例、引用实例、判断实例的关键

new this super instanceof

- 用于处理异常的关键字

try catch finally throw throws

- 用于包的关键字

package import 

- 其他关键字

native strictfp transient volatil assert

## 3.3 常量

在程序运行过程中，其值不可以发生改变的量。

- 字面值常量

字符串常量 ""

字符常量 ''

整数常量 

小数常量 

布尔常量 true false

空常量 null

- 自定义常量

在变量的语法格式前面添加个关键字 final 

## 3.4 变量

在程序执行过程中，其值可以在某个范围内发生改变的量

变量的本质，是内存中的一小块区域

数据类型 变量名 = 初始化值;

- 数据类型
限定变量变化的范围
- 变量名
方便存取
- 初始化值
使用变量前，赋予的初值

直接通过变量名来使用

## 3.5 数据类型

### 基本类型

（1）整数型

字节型 byte 1个字节

短整型 short 2个字节

整型 int 默认 4个字节

长整型 long 8个字节

（2）浮点型

单精度 float 4个字节

双精度 double 默认 8个字节

（3）字符型 char 2个字节

（4）布尔型 boolean 1个字节


- 计算机存储数据的形式

计算机中最小的存储单元是字节(Byte), 每个字节包含8个位(bit, 值位0或1)

b, B, KB, MB, GB, TB


### 引用类型

（1）类 class

（2）接口 interface

（3）数组 []


## 3.6 数据类型转换

不同类型的数据之间可能会进行运算，而这些数据的取值范围不同，存储方式不同，直接进行运算可能会造成数据损失。所以需要将一种类型转换成另一种类型再进行运算。

- 自动类型转换

小类型转大类型，自动提升为大类型，运算结果是大类型

byte -> short -> int -> long -> float -> double

char -> int

- 强制类型转换

手动将大类型转换成小类型，运算结果是小类型

小类型 变量名 = (小类型)大类型数据


## 3.7 标识符






