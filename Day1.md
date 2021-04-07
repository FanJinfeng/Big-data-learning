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

给类、方法、变量、常量等起名字的字符序列

英文大小写字母、数字、下划线、美元符号

- 定义规则（必须要遵守）

不能以数字开头

不能是关键字

严格区分大小写

- 命名规范（大家形成的习惯）（驼峰命名，见名知意）

类和接口：首字母大写，如果有多个单词，每个单词首字母大写

变量和方法：首字母小写，如果有多个单词，从第二个单词开始首字母大写

常量名（自定义常量）：所有字母都大写，多个单词用下划线隔开

包名：全部小写，如果有多级目录，用点号隔开（一般遵循公司域名反写的格式 cn.itcast.demo）


# 4. Java运算符

运算符：对常量和变量进行运算操作的符号

表达式：用运算符把常量或变量连接起来的式子；表达式的类型为表达式运算结果的数据类型

## 4.1 算术运算符

- 基本类型

+ - * / %(取余) ++(自增1) --(自减1)

Java中整数除以整数结果还是整数

%可以用来判断两个数是否能够整除

浮点数参与运算，结果才是浮点类型

- 字符和字符串参与加法运算

字符型数据参与运算时，用该字符在计算机中所表示的数值进行运算

'0' 48  'a' 97  'A'  65

加号两边有任意一边是字符串时，进行字符串的拼接

- 自增/自减

单独使用：放在变量前或者后结果一样

参与运算：++/--在变量前，先自增/自减，再进行其他运算；++/--在变量后，先以原值进行其他运算，再自增/自减

## 4.2 赋值运算符

- 基本赋值运算符

= 

- 扩展赋值运算符

+= -= *= /= %=

省略了强制类型转化的操作

## 4.3 关系运算符

== != >= > 

```s
a = b;  // 赋值
a == b; // 判断
```

## 4.4 逻辑运算符

&& || ! 

两端连接值为boolean类型的表达式（即关系表达式，或逻辑表达式）

## 4.5 三元运算符

表述三个表达式的关系

(关系表达式) ? 表达式1 : 表达式2;

关系表达式结果为true，运算后的结果是表达式1，否则是表达式2

```s
// 求两个整数的最大值
int a = 10;
int b = 20;
int max = (a>b) ? a : b;  // 不要忘记声明max的类型
System.out.println(max)
```

# 5. 流程控制结构之选择结构

- 流程控制结构

通过使用一些特定的语句控制代码的执行顺序，从而完成特定的功能

顺序结构：从上往下、从左至右执行

选择（判断）结构：根据不同的条件选择不同的代码来执行

循环结构：使一部分代码按照次数或一定的条件反复执行

- Scanner的基本使用

扫描器，扫描用户在控制台录入的数据并接收

```s
package cn.itcast.demo;
import java.util.Scanner;

public class ScannerDemo {
    public static void main(String[] args) {
        // 创建键盘录入对象（使用一个类前，要先创建它的对象）
        Scanner sc = new Scanner(System.in);

        // 接收用户输入的整数并赋值给i
        System.out.println("请输入一个整数：");
        int i = sc.nextInt();
        System.out.println("i = " + i);
    }
}
```

## 5.1 if语句

一般用作区间值的判断

```s
if(表达式) {
    // 语句体
}
```

```s
if(表达式) {
    // 语句体1
}  else {
    // 语句体2
}
```

```s
if(表达式1) {
    // 语句体1
} else if(表达式2) {
    // 语句体2
} // ...
else {
    // 语句体n+1
}
```

- 三种导包方式
手动, 鼠标, Alt+Enter

## 5.2 switch语句

一般用作固定值的判断

```s
switch(表达式) {
    case value1:
        语句体1;
        break;
    case value2:
        语句体2;
        break;
    ...
    default:
        语句体n+1;
        break;
}
```

枚举的形式

表达式的取值类型：byte, short, int, char, string

执行break, 结束switch语句

所有case都不匹配, 执行default中的语句体

# 6. 流程控制结构之循环结构



## 6.1 for循环

```s
for(初始化语句; 判断语句; 控制语句) {
    // 循环体
}
```

## 6.2 while循环

```s
初始化语句;
while(判断语句) {
    循环体;
    控制语句;
}
```

初始化语句可以省略；控制语句可以省略

## 6.3 do...while循环

```s
初始化语句;
do {
    循环体;
    控制语句;
} while(判断语句);
```

while小括号后面的分毫不可省略；
do...while循环的循环体至少执行一次；
初始化语句可以省略；控制语句可以省略

## 6.3 死循环和

```s
for(;;) {
    System.out.println("看看我是不是会一直执行！");
}

while(true) {
    System.out.println("看看我是不是会一直执行！");
}
```

## 6.4 关键字break, continue

break: 用于switch语句和循环语句，结束代码块

continue: 用于循环语句，结束本次循环，开始下一次循环

## 6.5 循环的嵌套

一个循环体语句中包含另一个循环语句

## 6.6 带标号的循环结束

标号：循环的名称

应用：常用于多层嵌套循环中

```s
标号: for() {}

break 标号;  // 结束指定标号的循环
continue 标号;  //跳转到指定标号的循环
```

## 6.7 Random类




# 7. 方法和数组


# 8. 面向对象之封装


# 9. 面向对象之继承

# 10.面向对象之多态



