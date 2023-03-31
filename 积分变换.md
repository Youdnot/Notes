# Fourier

## 1

傅里叶变换
$$
\hat f(\omega)=\int_{-\infty}^{\infty}f(t)e^{-jwt}dt
$$
傅里叶逆变换
$$
f(t)=F^{-1}[\hat f(\omega)]=\frac{1}{2\pi}\int_{-\infty}^{\infty}f(t)e^{jwt}dt
$$
对称公式
$$
\hat{\hat{f}}(t)=2\pi f(-t) \\
(=F[\hat f(\omega)]=\int_{-\infty}^{\infty}f(t)e^{-jwt}dt=2\pi f(-t)= )
$$

## 2 $\delta$ 函数的性质

$$
筛选性质：\int_{-\infty}^{\infty}\delta (x-x_0)\phi(x)dx=\phi(x_0)
$$

$$
\delta(x)\leftrightarrow 1
$$

## 3 性质

1. 线性
   $$
   
   $$
   
2. 位移
   $$
   \begin{matrix}
   F[f(t-t_0)]=e^{-jwt_0}\hat f(w)
   \\F^{-1}[\hat f(w-a)]=e^{jat}f(t)
   \end{matrix}
   $$
   
3. 相似
   $$
   F[f(at)]=
   \frac{1}{\begin{vmatrix}
   a
   \end{vmatrix}}
   \hat f(\frac{w}{a})
   $$
   
4. 微分
   $$
   \begin{matrix}
   F[f^\prime(t)]=jw\hat f(w)
   \\\displaystyle F[-jtf(t)]=\frac{d}{dw}\hat f(w)
   \end{matrix}
   $$
   
5. 积分

$$
F[\int_{-\infty}^{t} f(\tau)d\tau]=\frac{1}{jw}\hat f(w)
$$

## 卷积

$$
f(t)*g(t)=\int_{-\infty}^{\infty}f(s)g(t-s)ds
$$

$\delta$ 函数的卷积公式
$$
\delta(t-a)*f(t)=f(t-a)
$$


# Laplace

$$
F(s)=\int^{+\infty}_{0} f(t)e^{-st}dt
$$

反演积分公式
$$
f(t)=F^{-1}[F(s)]=\frac{1}{2\pi j}\int^{\beta+j\infty}_{\beta-j\infty}F[s]e^{st}ds
$$
存在定理

周期函数
$$
F(s)=\frac{1}{1-e^{-sT}}\int^{T}_{0} f(t)e^{-st}dt
$$
性质：

1. 线性
   
2. 相似
   
   $$
   L[f(at)]=\frac{1}{a}F(\frac{s}{a})
   $$
   
3. 微分

   1. 导数的像函数
      $$
      L[f^{\prime}(t)]=sF(s)-f(0)
      $$

      $$
      L[f^{(n)}(t)]=s^{n}F(s)-s^{n-1}f(0)-s^{n-2}f^{\prime}(0)-...-f^{(n-1)}(0)
      $$

   2. 像函数的导数
      $$
      F^{\prime}(s)=-L[tf(t)]
      $$
      

4. 积分

   1. 积分的像函数
      $$
      L[\int^t_0f(t)dt]=\frac{1}{s}F(s)
      $$


   2. 像函数的积分
      $$
      \int^s_0F(s)ds=L[\frac{f(t)}{t}]
      $$
      
5. 位移
   $$
   L[e^{at}f(t)]=F(s-a)
   $$
   
6. 延迟
   $$
   L[f(t-\tau)H(t-\tau))]=e^{-s\tau}F(s)
   $$

# 卷积

$$
   f(t)*g(t)=\int^{\infty}_{-\infty}f(\tau)g(t-\tau)d\tau
   \\=\int^{\tau}_{0}f(\tau)g(t-\tau)d\tau
$$

卷积定理
$$
L[f(t)*g(t)]=F(S)G(S)
$$



展开定理
$$
f(t)=\frac{1}{2\pi j}\int_{\beta-j\infty}^{\beta+j\infty}F(s)e^{st}ds=\sum^n_{k=1}Res[F(s)e^{st},s_k]
$$
