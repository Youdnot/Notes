# 第十六章 二端口网络

## 目录

- 16-1 二端口网络
- 16-2 二端口的方程和参数
- 16-3 二端口的等效电路
- 16-4 二端口的转移函数
- 16-5 二端口的连接*
- 16-6 回转器和负阻抗变换器*



## Y参数

$$
\begin{matrix}
 \dot I_1=Y_{11}\dot U_1+Y_{12}\dot U_2
 \\
 \dot I_2=Y_{21}\dot U_1+Y_{22}\dot U_2
\end{matrix}
$$

导纳性质

互易：$Y_{12}=Y_{21}$

对称：$Y_{11}=Y_{22}$

节点电压法

## Z参数

回路电流法

## T参数

$$
\begin{matrix}
 \dot U_1=A\dot U_2-B\dot I_2
 \\
 \dot I_1=C\dot U_2-D\dot I_2
\end{matrix}
$$



### 参数求法

1. 根据定义计算，辅以对称性和互易性
2. 列出方程即得
3. 根据参数之间的关系利用已知参数求解



## 等效电路

一个无源二端口网络可以用一个简单的二端口等效模型来代替，要注意的是：

1. **等效条件**：等效模型的方程与原二端口网络的方程相同；
2. 根据不同的网络参数和方程可以得到结构完全不同的等效电路；
3. 等效目的是为了分析方便。



1. 直接由参数方程得到等效电路
2. 进行等效变换

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220311104843101.png" alt="image-20220311104843101" style="zoom: 80%;" />

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220311104954334.png" alt="image-20220311104954334" style="zoom:80%;" />

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220311105218346.png" alt="image-20220311105218346" style="zoom:80%;" />





## 二端口网络连接

1. 级联/链联
   - $T=T\prime+T\prime\prime$
2. 并联
   - $Y=Y\prime+Y\prime\prime$
3. 串联
   - $Z=Z\prime+Z\prime\prime$