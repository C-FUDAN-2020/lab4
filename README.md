# Lab 4

    本节目标：
      1. 巩固算术运算有关知识
      2. 学会宏定义常量
      3. 熟练使用循环语句与判断语句
      4. 了解浮点数比较

## 获取及提交lab

**获取**：通过 `https://github.com/C-FUDAN-2020/lab4` 获取。

**提交物**：将你完成目标 1 思考题的文档和目标 2，3，4 的源代码文件作为 lab4 的提交物。

**提交**：将提交物文档命名为学号_姓名 （如20302010000_王明），提交至超星学习通对应的作业中。

**截止时间**：北京时间 2020年9月18日 23:59:59 

## 你真的会算术运算吗？

根据之前课程的学习和小学二年级的经验，大家一定能熟练使用算术运算符(`+`, `-`, `*`, `/`, `+=`, `-=`, `++`, `--`)进行整数、浮点数的运算了。但是，你真的学会使用算术运算符了吗？

如果你认为完全了解了算术运算，请回答助教提出的两个问题

> 这两个问题请提交书面答案的文档

#### 问题一：自增

观察下面一段代码，思考控制台会有何种输出，并解释原因。

```c
#include <stdio.h>

int main() {
  int x = 1;
  // level 1
  x++;
  printf("%d\n", x);
  ++x;
  printf("%d\n", x);
  // level 2
  int a1 = x++;
  printf("%d\n", a1);
  int a2 = ++x;
  printf("%d\n", a2);
  // level 3
  int b1 = x++ + x++;
  printf("%d\n", b1);
  int b2 = x++ + ++x;
  printf("%d\n", b2);
  int b3 = ++x + ++x;
  printf("%d\n", b3);
  return 0; 
}
```

#### 问题二：简单的类型转换

观察下面几段代码，它们能否通过编译，如果不能，请解释原因，如果能，x 的值为多少？并解释原因。

```c
char x = 'a';
x++;
```

```c
char x = 1;
x += 256;
```

```c
char x = 1.9f;
x = x * 1.9f;
```

```c
char a = 16.5f;
double PI = 3.14159;
short x = (float)(4 / 3) * PI * (int)a * a * (double)a;
```

## 编程题

Write a program to approximate the value of π using the following formula：

<img src="./formula">

Please answer how many items must the program calculate to get the values 3.14159.

> 注意：
> 1. 请使用宏定义（`#define`）定义数值常量
> 2. 浮点数并非真正意义上的实数，只是其在某个范围内的近似。因此两个浮点数判断是否相等时，不能简单地使用等号进行比较，应该判断两个浮点数差值的绝对值是否近似为0。
> 3. 绝对值计算可以调用 `<math.h>` 的库函数 `fabs()`
