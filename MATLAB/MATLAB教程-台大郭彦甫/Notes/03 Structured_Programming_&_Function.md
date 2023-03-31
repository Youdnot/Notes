# 03 Structured_Programming_&_Function 

# 结构化编程与功能

## Contents

- Script writing  脚本编写
- Structured programming  编程结构 
- User-defined function  用户定义函数

## Script writing 

### Script Editor

#### Function

% 注解/注释 Comment

%% 区块 Section

#### 断点的设置

右键菜单 smart ident 自动缩进

### Script Flow 程序流？

通常程序自上而下运行，接近于流 即 Flow 的状态（吗

Structured programming, 即结构化编程，这里指通过子程序、循环、条件等等结构使程序整洁。下列 Flow Control 即是程序的实现。

#### Flow Control 指令

|         Operator         |                        Meaning                         |
| :----------------------: | :----------------------------------------------------: |
|     if, elseif, else     |        Execute statements if condition is true         |
|           for            |      Execute statements specified number of times      |
| switch, case,  otherwise |      Execute one of several groups of statements       |
|        try, catch        |     Execute statements and catch resulting errors      |
|          while           | Repeat execution of statements while condition is true |
|          break           |        Terminate execution of for or while loop        |
|         continue         |  Pass control to next iteration of for or while loop   |
|           end            | Terminate block of code, or indicate last array index  |
|          pause           |               Halt execution temporarily               |
|          return          |          Return control to invoking function           |



## Structured programming 

### Relational(Logical) Operators 关系（逻辑）运算符

$$
\begin{matrix}
\textup{Operator}  &  \textup{Meaning}\\
<  &  小于\\
<=  &  小于或等于\\
>  &  大于\\
>=  &  大于或等于\\
==  &  等于\\
~=  &  不等于\\
\&\& & 和\\
||  &  或
\end{matrix}
$$



### 使用

#### if elseif else

```matlab
if condition1
		statement1
elseif condition2
		statement2
else
		statement3
end
```

#### switch

```matlab
switch expression
case value1
		statement1
case value2
		statement2
.
.
otherwise
		statement
end
```

#### while

```matlab
while expression
		statement
end
```



```matlab
exercise
使用while循环计算1-999的和

n = 1;
sum1 = 0;
while n <= 999
		sum1 = sum1 + n
		n = n + 1
end
```



#### for
```matlab
for variable=start : increment : end
		commands
end
```


![image-20220317191005535](C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220317191005535.png)



#### break

与python同理



### 程序写作的技巧

开始之前：

- `clear all `清除所有变量
- 关闭所有图像
- `clc` 
- 使用 `；` 不让代码执行显示在 command window中
- 使用 `...` 换行，便于阅读（比如建立数组时）
- `ctrl + c` 中断运行



### Scripts vs. Functions 脚本与函数

脚本与函数都是包含Matlab命令的 .m 文件

脚本自己写，函数内置

### 内置函数的结构

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220317192401205.png" alt="image-20220317192401205" style="zoom: 67%;" />

## User-defined function

实例：自由落体 freebody

> \* 与 \.\* 的区别
>
> ​		当输入是向量时，\.\* 将每一个数据分组分别计算。在本例中，如果改为 \* ，输入向量则会发生错误



### 多输入输出函数

### 函数的默认变量
| 函数名    | 意义                                    | Chinese          |
| --------- | --------------------------------------- | ---------------- |
| inputname | Variable name of function input         | 输入参数名       |
| mfilename | File name of currently running function | 运行中函数的名字 |
| nargin    | Number of function input arguments      | 输入参数数量     |
| nargout   | Number of function output arguments     | 输出参数数量     |
| varargin  | Variable length input argument list     | 输入参数长度*    |
| varargout | Variable length output argument list    | 输出参数长度*    |

### Function Handles

是一个 pointer

一种创建匿名函数的方法

单行
