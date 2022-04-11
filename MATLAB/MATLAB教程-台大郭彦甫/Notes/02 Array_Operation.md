# 02 Array_Operation

# 数组操作

## Contents

- Introduction
- MATLAB as calculator
- Array operation

## Introduction

### MATLAB Programming Modes

MATLAB有两种程序运行模式：

- Command line (in command window) 命令行
- Scripts (.m files) 脚本

## MATLAB as calculator

### 运算符

结果自动运算，显示为 `ans` 

### Elementary Math Functions

### Embedding Functions

函数可以嵌套使用，将多行代码写到一行

### Variables

变量在使用之前不需要声明

`=` 赋值运算符

区分大小写

### Numeric Variable (Data) Type

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220318123001714.png" alt="image-20220318123001714" style="zoom:50%;" />

#### Special Variables and Constants

一些特殊符号的表示

### MATLAB Calling Priority

$$
\begin{matrix}
\textup{Priority\ From\ High\ to\ Low}\\
Variable\rightarrow Built-in\ function\rightarrow Subfunction\rightarrow Private function(MEX/P/M-file)
\end{matrix}
$$

### Numeric Display “Format”

数字的数据类型

### Command Line Terminal 命令行终端

在命令的结尾加上；使其不输出结果

$\uparrow$ 显示历史命令

#### Some Useful Functions

- `clc`: clear command window display
- `clear`: remove all variables in the workspace
- `who`: variables in the workspace
- `whos`: variable information of the workspace

## Array (Vector and Matrix)

### Indexing

### Replacing Entries

### Colon Operator

### Indexing Using Colon Operator

### Concatenation

### Manipulation

### Some Special Matrix

### Some Matrix Related Functions