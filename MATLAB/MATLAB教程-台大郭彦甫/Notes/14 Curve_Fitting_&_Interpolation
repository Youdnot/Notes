# 14Curve_Fitting_&_Interpolation  曲线回归分析与内插

## Contents

- Polynomial curve fitting
- Multiple regression
- Interpolation

## Simple Linear Regression  简单线性回归

- A bunch of data points (𝑥𝑖 , 𝑦𝑖) are collected. Assume 𝑥 and 𝑦 are linearly correlated
- 对于已有的一组数据点，假设 x y 相关

### Linear Regression Formulation  线性曲线回归方程

- Define sum of squared errors (*SSE*):  误差平方和
  - $SSE=\sum_i\epsilon_i^2=\sum_i(y_i-\hat{y})^2$
- Given that the regression model: $\hat{y_i}=\beta_0+\beta_1x_i$   回归模型，代入
  - $SSE=\sum_i(y_i-\beta_0-\beta_1x_i)^2$ 

### Solving Least-squares Problem

- Find Beta0 Beta1 so that SSE is minimized  找到
- 微分
- 𝑆𝑆𝐸 is minimized when its gradient with respect to  each parameter is equal to zero:
- 

#### Least-squares Solution

- Suppose there exists 𝑁 data points:
- 

### Polynomial Curve Ftting: `polyfit()`

- Curve fitting for polynomials of different orders 的内置函数

- `polyfit(x,y,order/阶数)`

- ```matlab
  x =[-1.2 -0.5 0.3 0.9 1.8 2.6 3.0 3.5];
  y =[-15.6 -8.5 2.2 4.5 6.6 8.2 8.9 10.0];
  fit = polyfit(x,y,1);
  
  xfit = [x(1):0.1:x(end)]; yfit = fit(1)*xfit + fit(2);
  plot(x,y,'ro',xfit,yfit); set(gca,'FontSize',14);
  legend(2,'data points','best-fit');
  ```

### Are 𝑥 and 𝑦 Linearly Correlated?

- If not, the line may not well  describe their relationship
- Check the linearity by using
  - `scatter()`: scatterplot
  - `corrcoef()`: correlation coefficient, −1 ≤ 𝑟 ≤ 1  计算相关系数

### Higher Order Polynomials  高阶多项式

- 高阶多项式的曲线拟合效果更好
- 具体代码见Slides

### What If There Exists More Variables?  如果存在多个变量呢？

- Equations associated with more than one  explanatory variables: $y=\beta_0+\beta_1x_1+\beta_2x_2$ 

#### Multiple Linear Regression: `regress()`

## What If the Equations Are NOT Linear?

### DC Motor System Identification

### Curve Fitting Toolbox: `cftool()`

### Interpolation vs Regression  内差与回归

![image-20220331221331755](C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220331221331755.png)

### Common Interpolation Approaches

- [Piecewise linear interpolation](https://fncbook.github.io/fnc/localapprox/pwlin.html)  
- Piecewise cubic polynomial interpolation
- Cubic spline interpolation



- Linear Interpolation: `interp1() `
- [Spline](https://blog.csdn.net/jesseyule/article/details/95246893) Interpolation: [`spline()`](https://ww2.mathworks.cn/help/matlab/ref/spline.html)

### Cubic Spline vs. Hermite Polynomial

- 曲线的震荡/平滑效果选择



- 2D Interpolation: `interp2()`
- 2D Interpolation Using Spline



## 拓展阅读

[SSE,MSE,RMSE,R-square指标讲解 - Django's blog - 博客园 (cnblogs.com)](https://www.cnblogs.com/DjangoBlog/p/9575360.html)

[Sum of squared error (SSE) - Cluster Analysis 4 Marketing](https://www.clusteranalysis4marketing.com/interpretation/sum-of-squared-error-sse/)