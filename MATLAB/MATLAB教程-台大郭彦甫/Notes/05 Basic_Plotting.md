# 05Basic_Plotting

## Contents

- Basic plotting
- Graphical object properties

## Basics

MATLAB有着十分强劲的绘图引擎，可以生成广泛类型的图表。但MATLAB不能理解函数

### Plot from “Data”

Strategies:

1. Generate the numeric values of a function over a  specific range  收集函数在特定区间的数值
2. Display the data “points” in a graphical way  用图像方法将数据点展示

## `plot()`

[二维线图 - MATLAB plot - MathWorks 中国](https://ww2.mathworks.cn/help/matlab/ref/plot.html?s_tid=doc_ta)

未规定坐标时，横纵坐标数就是点的数量

### `hold on/off`

不使用指令时，后生成的图会覆盖原先的图

Use `hold on` to have both plots in one figure

### Plot Style

控制data markers/line type/colors等

#### `legend()` 图例

#### `title()` and `?label()` 标题和标签

#### `text()` and `annotation()`

Text with mathematical expression using <u>LaTex</u>. `$$...$$`

给予用户在图表上添加数学表达式的能力

### Figure Adjustment

字体，字体大小，线宽，坐标范围等（tick指坐标轴上坐标点垂直突出的一小段线）

#### Graphical Objects

#### 图形的各个组成部分

![image-20220319130159626](C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220319130159626.png)

```matlab
x = linspace(0, 2*pi, 1000); y = sin(x);
plot(x,y); set(gcf, 'Color', [1 1 1]);
```

hierarchy [ˈhaɪəˌrɑrki] 层次体系

#### Figure Properties 属性

Figure - Edit - Figure Property -More Properties 调出属性菜单 

技术文档支持：[MATLAB Documentation (mathworks.com)](https://www.mathworks.com/help/matlab/ref/figure-properties.html)

#### Modifying Properties of An Object

1. Identify the “handle” of an object 找到对象的”句柄“
   1. Upon creation 在创建时找到
   2. Utility functions 使用函数寻找
2. Fetch or modify the object’s properties 获取并修改其属性
   1. To fetch properties, use `get()`
   2. To modify properties, use `set()`

可以通过完整的寻找属性方式最后通过set函数修改，也可以直接提取特定函数直接修改想要修改的对象。

不再支持symbol字体

#### Multiple Figures

Be careful when using the `gcf` handle where  there exists multiple figures.

- Figure Position and Size 图像尺寸
- Several Plots in One Figure `subplot(m, n,1); `
- Control of Grid, Box, and Axis 指令参考
- Saving Figures into Files 保存=