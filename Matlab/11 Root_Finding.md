# 11Root_Finding

## Contents

- Symbolic approach
- Numeric root solvers
- Recursive functions

## Problem Statement

Suppose you have a mathematical function 𝑓(𝑥) and you want to find 𝑥0 such that 𝑓 𝑥0 = 0. How do you solve the  problem using MATLAB?

- Analytical Solutions  解析法
- Graphical Illustration  图像
- Numerical Solutions  数学

## Symbolic Root Finding Approach

- Performing mathematics on symbols, NOT numbers  使用变量符号（symbol）进行运算，而不是数字（列方程
- The symbols math are performed using “symbolic  variables”
- Use `sym` or `syms` to create symbolic variables

### Symbolic Root Finding: `solve()`

Function solve finds roots for equations

### Solving Multiple Equations

```matlab
syms x y
eq1 = x - 2*y - 5;  %适当移项使等式右侧等于0
eq2 = x + y - 6;
A = solve(eq1,eq2,x,y)
```

### Solving Equations Expressed in Symbols

𝑥 is always the first choice to be solved

If one wants to express 𝑏 in terms of 𝑎 and 𝑥:

```matlab
syms x a b
solve('a*x^2-b', 'b')  %在solve函数中后置想要求解的变量
```

#### Symbolic Differentiation: `diff()`

#### Symbolic Integration: `int()`

`sub()` 在函数中用给定值代替自变量计算因变量

### Symbolic vs. Numeric

|          | Advantages                                                   | Disadvantages                                             |
| -------- | ------------------------------------------------------------ | --------------------------------------------------------- |
| Symbolic | Analytical solutions<br />Lets you intuit things about  solution form | Sometimes can't be solved <br />Can be overly complicated |
| Numeric  | Always get a solution<br />Can make solutions accurate<br />Easy to code | Hard to extract a deeper  understanding                   |

## Numeric root solvers

### Review of Function Handles (@)

### `fsolve()`

initial guess

### `fzero()`

- Find the zero if and only if  the function crosses the  x-axis
- 只有函数穿过x轴时才能求解
- Options  各种参数的设置

### Finding Roots of Polynomials: `roots()`

- `roots()` 只对多项式成立

### Numeric Root Finding Methods

- Two major types:
  - Bracketing methods
    - Start with an **interval**(包夹区间) that contains the root
    - e.g., bisection method  二分法
  - Open methods
    - Start with one or more initial guess points
    - e.g., Newton-Raphson method
- Roots are found iteratively until some criteria are  satisfied:
  - Accuracy
  - Number of iteration

对两个具体方法的解释详见Slides。

## Recursive Functions

- Functions that call themselves
- A factorial can be defined in terms of another  factorial

### Factorial Recursive Function

- The function includes a recursive case and a base  case
- The function stops when it reaches the base case