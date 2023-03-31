# 从Excel导入数据并绘图

输出类型：数值矩阵

表格中： `ctrl`+`shift`+`down`  快捷选中一列

 `ctrl`+`shift`+`right`  快捷选中一行



# 绘制散点图

`scatter` 

[散点图 - MATLAB scatter - MathWorks 中国](https://ww2.mathworks.cn/help/matlab/ref/scatter.html)

在MATLAB中，绘制散点图可以使用scatter这个函数，其中scatter是用来绘制二维的散点图，scatter3是用来绘制三维的散点图，他们的用法大致相同，因此这里主要拿scatter这个绘制二维散点图的函数来举例。

用法形式为scatter(X,Y,S,C)，X、Y分别是横纵坐标向量，他们的长度必须是一样的。S可以是一个和X、Y等长的向量，也可以是一个标量，这个参数决定了散点标志符的大小，如果是向量的话，就分别决定每一个标志点的大小，如果是一个标量的话，就一次性确定了这次绘制的标志符的大小。C代表的是颜色，它同样可以是一个和上述X、Y等长的向量，或者长度x3的矩阵（RGB调色），也可以是一个颜色符号（一次确定了所有点的颜色）。

除了这些之外，我们还可以指定标志符的种类，还有标志内是不是填充。下面的表格中介绍了标志代号与颜色代号：

| 标识符       | 说明     | 颜色 | 说明   |
| ------------ | -------- | ---- | ------ |
| +            | 加号     | r    | 红色   |
| o            | 空心圆   | g    | 绿色   |
| *            | 星号     | b    | 蓝色   |
| .            | 点       | c    | 青色   |
| x            | 叉号     | m    | 洋红色 |
| s(square)    | 正方形   | y    | 黄色   |
| d            | 菱形     | k    | 黑色   |
| ^            | 上三角形 | w    | 白色   |
| >            | 右三角形 |      |        |
| <            | 左三角形 |      |        |
| p(pentagram) | 五角形   |      |        |
| h(hexagram)  | 六角形   |      |        |

## 使用方法：

1. scatter(X,Y) 使用默认的标志大小、颜色与符号绘制散点图。
2. scatter(X,Y,S) 使用指定的标志大小与默认的颜色、符号绘制散点图。
3. scatter(X,Y,...,C) 使用指定的颜色绘制散点图。
4. scatter(X,Y,...,M) 使用指定的符号绘制散点图。
5. scatter(X,Y,...,'filled') 填充标志符。

## 例子：

①默认：

```matlab
x=-8:1:8;
y=x.^2;
scatter(x,y);
```

<img src="https://pic3.zhimg.com/80/v2-0ad3f02026166c72b19ba450d6e5a6ba_720w.jpg" alt="img" style="zoom:33%;" />

②改变大小

```matlab
x=-8:1:8;
y=x.^2;
scatter(x,y,500);
```

<img src="https://pic4.zhimg.com/80/v2-6c4e56136bde339677cd97b99d47b9fb_720w.jpg" alt="img" style="zoom:33%;" />

③改变颜色

```matlab
x=-8:1:8;
y=x.^2;
scatter(x,y,500,'r');
```

<img src="https://pic2.zhimg.com/80/v2-881ea7d075dc96956af4b4ce79af80b1_720w.jpg" alt="img" style="zoom:33%;" />

④改变符号

```matlab
x=-8:1:8;
y=x.^2;
scatter(x,y,500,'r','p');
```

<img src="https://pic2.zhimg.com/80/v2-7a880fd2a484bf87fe8376ca2c42d2a9_720w.jpg" alt="img" style="zoom:33%;" />

⑤填充

```matlab
x=-8:1:8;
y=x.^2;
scatter(x,y,500,'r','p','filled');
```

<img src="https://pic3.zhimg.com/80/v2-6dee4cea4b6aa66c43382c2bb47ebbb6_720w.jpg" alt="img" style="zoom:33%;" />

⑥绘制多个

```matlab
x=-2:0.1:2;
y=x.^4;
scatter(x,y,50,'r','p','filled');
hold on;
y=x.^3;
scatter(x,y,30,'k','+');
hold on;
y=-x.^3;
scatter(x,y,30,'b','s');
```

<img src="https://pic1.zhimg.com/80/v2-4942a09303a3fa744c39455d59c96340_720w.jpg" alt="img" style="zoom:33%;" />

## 三维散点图的绘制方法：

大部分同上述所讲解的，只不过多了一列向量Z，scatter3(X,Y,Z,...)，X、Y、Z分别确定了每个点的坐标，这三个向量要求必须长度一致。

下面是一个例子：

```matlab
u=-9:0.3:9;
v=-9:0.3:9;
[x,y]=meshgrid(u,v);
z=exp(-(x.^2+y.^2)/(2*3^2))/(2*pi*3^2);
[m,n]=size(x);
for i=1:m
    scatter3(x(i,:),y(i,:),z(i,:),10,'m','p');
    hold on;
end
title('测试');
xlabel('X');ylabel('Y');zlabel('Z');
```

<img src="https://pic4.zhimg.com/80/v2-fa4bc9ef7eb9bf35336acaa5fc838c17_720w.jpg" alt="img" style="zoom:33%;" />



# 绘制平滑曲线

自然状态下，用plot画的是折线，而不是平滑曲线。

有两种方法可以画平滑曲线，第一种是拟合的方法，第二种是用spcrv，其实原理应该都一样就是插值。下面是源程序，大家可以根据需要自行选择，更改拟合的参数。

```matlab
clc,clear;
%%
x=[30,20,10,-10,-20];
f=[603.633,593.333,588.033,587.732,590.432];
plot(x,f);  %自然状态的画图效果
hold on;
%%
%第一种，画平滑曲线的方法
c = polyfit(x, f, 2); %进行拟合，c为2次拟合后的系数
d = polyval(c, x, 1); %拟合后，每一个横坐标对应的值即为d
plot(x, d, 'r');    %拟合后的曲线
lot(a, b, '*');    %将每个点 用*画出来
hold on;
%%
%第二种，画平滑曲线的方法
values = spcrv([[x(1) x x(end)];[f(1) f f(end)]],3);
plot(values(1,:),values(2,:), 'g');
hold on;
```

 个人感觉后一种方法要好一些