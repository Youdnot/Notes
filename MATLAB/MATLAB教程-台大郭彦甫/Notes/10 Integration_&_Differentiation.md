# 10Integration_&_Differentiation 微分与积分

## Contents

- Polynomial differentiation and integration
- Numerical differentiation and integration

## Differentiation 微分

$$
f\prime(x)\ or \ \frac{df(x)}{dx}
$$

## Polynomial Differentiation 多项式

- Polynomials are often used in numerical  calculations

### Representing Polynomials in MATLAB

- Polynomials were represented as row vectors
- 系数以行向量的方式表示

### Values of Polynomials: `polyval()`

### Polynomial Differentiation: `polyder()`

### Polynomial Integration: `polyint()`

## Numerical Differentiation

The simplest method:  finite difference approximation 有限误差近似？

### Differences: `diff()`

- calculates the differences between adjacent elements of a vector
- 计算向量中相邻元素的差

```matlab
%Exercise: obtain the slope of a line between 2 points (1,5) and (2,7)
%计算曲线的斜率
x = [1 2]; y = [5 7];
slope = diff(y)./diff(x)
```

### eg：How to Find the 𝑓′ over An Interval [0,2𝜋]?

#### Strategy

1. Create an array in the interval [0, 2𝜋] 
2. The step is the ℎ 
3. Calculate the 𝑓′ at these points
4. 观察 Various Step Size 的影响

### Second and Third Derivatives 二次与三次微分

- 再次 difference 即可
- 注意数据的阶数

### Numerical Integration

#### Quadrature method

- approximating the integral by using a finite set of points

- Basic quadrature rules

  - Midpoint rule (zeroth-order approximation)

    - Using `sum()`

    - ```matlab
      midpoint = (x(1:end-1)+x(2:end))./2;
      ```

  - Trapezoid rule (first-order approximation)

    - Using `trapz()`

    - ```matlab
      trapezoid = (y(1:end-1)+y(2:end))/2;
      ```

  - econd-order Rule: 1/3 Simpson’s

	  - 更精确

![image-20220324194251460](C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220324194251460.png)

### `integral()`

- Numerical integration on a function from using  global adaptive quadrature and default error  tolerances

### Review of Function Handles (@)

- 函数不能作为函数的输入
- 使用 @ 的指针方式

### Double and Triple Integrals