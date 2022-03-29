# 12Linear_Equations

## Contents

- Linear equation
- Linear system

## Linear equation

### Matrix Form

使用矩阵形式求解会更加方便（e.g.: Formulation for the Electrical Network）

Usually when solving linear equations:

1. 𝑨 and 𝒃 are know
2. 𝒙 is unknown

### Solving Linear Equations

1. Successive elimination (through factorization)
2. Cramer’s method

### Gaussian Elimination  高斯消元法

增广矩阵，化为

#### `rref()`

### LU Factorization

- Suppose we want to solve: 𝑨𝒙 = 𝒃, where 𝑨 ∈ ℜ𝑚×�
  假设 A 为矩阵的情形
- Decompose 𝑨 into 2 triangular matrices: 𝑨 = 𝑳 −1𝑼
  将 A 分解为两个三角矩阵
- The problem become: 𝑨𝒙 = 𝒃 ⇒ $L^{-1}Ux=b$
- Strategies:
  - Solve 𝑳 −1𝒚 = 𝒃 to obtain 𝒚
  - Then solve 𝑼𝒙 = 𝒚

#### `lu()`

### Matrix Left Division: `\` or `mldivide()`

- 可以直接计算
- 使用的是 successive elimation
- （所以前面的都是引入

### Matrix Decomposition Functions

- 指令详见Slides

### Cramer’s (Inverse) Method

- 求逆
- Inverse Matrix  逆矩阵

#### Singular

- 逆矩阵不存在的特殊矩阵

#### Problem with Cramer’s Method

#### Functions to Check Matrix Condition

- 解决不确定矩证是否适用卡尔曼法的方法
- 

|      |                         |
| ---- | ----------------------- |
| cond | Matrix condition number |
| rank | Matrix rank             |

## Linear System

系统与等式的区别

系统，着重输出与系统矩证的关系

How does the output impact by the system matrix

![image-20220327142951919](C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220327142951919.png)

### Eigenvalues and Eigenvectors  特征值与特征向量

用特征向量代表的实数代替矩证，从而化简

#### Interpretation of Eigenvalues and Eigenvectors

- 作用的形象描述

#### Solving Eigenvalues and Eigenvectors

- 化简

#### `eig()`

### Matrix Exponential: `expm()`

线性时不变系统的求解