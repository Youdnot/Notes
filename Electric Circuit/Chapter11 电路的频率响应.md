# 第十一章 电路的频率响应

## 目录

- 11-1 网络函数
- 11-2 RLC串联电路的谐振
- 11-3 RLC串联电路的频率响应
- 11-4 RLC并联谐振电路
- 11-5 波特图
- 11-6 滤波器简介



## 网络函数

在线性正弦稳态网络中，当只有一个独立激励源作用时，网络中某一处的响应（电压或电流）与网络输入之比，称为该响应的网络函数。
$$
H(j\omega)\overset{\underset{\mathrm{def}}{}}{=}\frac{\dot{R}_k(j\omega)}{\dot{E}_{sj}(j\omega)}
$$



$$
品质因数：
Q\overset{\underset{\mathrm{def}}{}}{=}
\frac{\omega_0L}{R}
=\frac{1}{\omega_0CR}=\frac{1}{R}\sqrt{\frac{L}{C}}
$$

$$
RLC串联电路的频率响应中，Q=\frac{\omega_0}{\Delta \omega}
$$

## 11-4 RLC并联谐振电路

$$
\omega_0=\frac{1}{\sqrt{LC}}
$$

$$
Q=\frac{\omega_0C}{Y}
=\frac{1}{\omega_0GL}=\frac{1}{G}\sqrt{\frac{C}{L}}
$$

### 电感线圈与电容器的并联谐振

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220311163717462.png" alt="image-20220311163717462" style="zoom:50%;" />
$$
Q=\frac{\omega_0C}{G}=\frac{\omega_0C}{R/(\omega_0L)^2}(=\frac{\omega_0^3CL^2}{R})
=\frac{\omega_0L}{R}=Q_L，即线圈的品质因数
$$


## 问题

电感和电阻串联等效为并联

无功功率的计算（用Q）？
