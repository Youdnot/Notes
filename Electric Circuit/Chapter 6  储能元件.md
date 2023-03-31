# 第六章 储能元件

## 目录

- 6-1 电容元件 Capacitor
- 6-2 电感元件 Inductor
- 6-3 电容、电感元件的串联与并联

# 第六章  储能元件

## 1.电容元件 Capacitor[^1]

- 能储存电荷or储存电场能量
- 电压参考极性和极板存储电荷极性一致时的**元件特性**： $ q=Cu $  (F)
- VCR： $ \displaystyle i=\frac{dq}{dt}=\frac{d(Cu)}{dt}=C\frac{du}{dt} $



* 在直流状态下，u恒定，相当于开路，即隔直
* $ \displaystyle q=\int i\rm{d}t=\int_{-\infty}^{t}i\rm{d}\xi=\int_{-\infty}^{t_0}i\rm{d}\xi+\int_{t_0}^{t}i\rm{d}\xi=q(t_0)+\int_{t_0}^{t}i\rm{d}\xi$

* $\displaystyle u=\frac{q}{C} \to u(t)=u(t_0)+\frac{1}{C}\int_{t_0}^{t}i\rm{d}\xi$

* $\displaystyle p=ui=Cu\frac{\rm{d}u}{\rm{d}t}$

* $\displaystyle W_c=\frac{1}{2}Cu^2(t)=W_c(t_2)-W_c(t_1)$

* 无源元件：不会释放出多于它吸收或储存的能量
* 电容效应     分布电容     杂散电容

## 2.电感元件

* 磁通链$\Psi$  磁通$\Phi$  匝数N          $\Psi =N\Phi$

* $\displaystyle u=\frac{\rm{d}\Psi _L}{\rm{d}t}$
* 元件特性：$\displaystyle \Psi =Li$     ($Wb$  韦伯，韦)     (L:自感系数、电感)
* $\displaystyle u=L\frac{\rm{d}i}{\rm{d}t}   $
* $i=\frac{1}{L}\int u\rm{d}t=i(t_0)+\frac{1}{L}\int_{t_0}^{t}u\rm{d}\xi$

* $\displaystyle \Psi _L=\Psi _L(t_0)+\int_{t_0}^{t}u\rm{d}\xi$

* $\displaystyle p=ui=Li\frac{\rm{di}}{\rm{d}t}$
* $\displaystyle W_L(t)=\frac{1}{2}Li^2(t)=\frac{1}{2}\frac{\Psi^2_L(t)}{L}=W_L(t_2)-W_L(t_1)$

* 无源元件

## 3.电容、电感串并联

##### 1.电容串联

* $u(t)=u(t_0)+\frac{1}{C}\int_{t_0}^{t}i\rm{d}\xi$

* 等效电容：$\displaystyle \frac{1}{C_{eq}}=\frac{1}{C_{1}}+\frac{1}{C_{2}}+......+\frac{1}{C_{n}}$

* 等效初始条件:$u(t_0)=u_1(t_0) +u_2(t_0)+......+u_n(t_0)$

##### 2.电容并联

* $i=C\frac{du}{dt} $

* 等效电容：$C_{eq}=C_{1}+C_{2}+......+C_{n}$

* 等效初始条件:$i(t_0)=i_1(t_0) +i_2(t_0)+......+i_n(t_0)$

##### 3.电感串联：

* $u=L\frac{\rm{d}i}{\rm{d}t}   $

* 等效电感：$\displaystyle L_{eq}=L_{1}+L_{2}+.......+L_{n}$

* 等效初始条件：$u(t_0)=u_1(t_0) +u_2(t_0)+......+u_n(t_0)$

##### 4.电感并联：

* $i(t)=i(t_0)+\frac{1}{L}\int_{t_0}^{t}u\rm{d}\xi$
* 等效电感：$\displaystyle \frac{1}{L_{eq}}=\frac{1}{L_{1}}+\frac{1}{L_{2}}+......+\frac{1}{L_{n}}$
* 等效初始条件：$i(t_0)=i_1(t_0) +i_2(t_0)+......+i_n(t_0)$




[^1]: 仅讨论理想线性电容元件
