# 06Advanced_Plotting
## Contents
- Advanced 2D plots
- Color space
- 3D plots

## 引入
根据统计数据的目的，选用不同类型的图表呈现
## Advanced 2D plots
### Special Plots
#### Logarithm Plots 对数图像
加入网格 `grid on` 使图像更清晰
#### `plotyy()`
 两条曲线，两种Y坐标系

###  统计类型

 #### Histogram
 Bin的设置 ／区间
 偏向整体
 #### Bar Chart 条形图
 偏向个体
 分组／3D

Stacked and Horizontal Bar Charts

 #### Pie Chart 饼状图
 分割
 #### Polar 极坐标？
 #### Stairs and Stem 阶梯图
 联系 固定时间取样？

#### Boxplot and Error Bar
箱线图 误差线

#### `fill()`
## Color Space
[R G B]色域表示
0～1拓展到255
8-bit equivalence
[FF FF FF]-[255 255 255]十六进制

## Visualizing Data as An Image: `imagesc()`
Dispaly values of a matrix as an "image"
Color Bar and Scheme 色值图例和色调
`colormap()` 本质为一个矩阵，储存定义好的颜色数值


## 3D Plots

2D图使用工具栏中的rotate会有3D的效果
`plot3()` line plot
### Principles of 3D Surface Plots
P26 图例
- Usually for plotting functions: 𝑧 = 𝑓(𝑥, 𝑦)
- Need to provide MATLAB a set of (𝑥,𝑦,𝑧) points
- Use `meshgrid` to create matrices X and Y for a given range
### Surface Plots
`mesh()`  `surf()`
#### `contour`  
在x-y平面上投影出等高／值线图
多种格式

`meshc()`  `surfc()` 结合投影contour


#### View Angle: `view()`
camera 视角设置

Light: `light()`
- set light 调整已有的光
- DiffuseStrength / AmbientStrength

`patch()`
画多边形 polygon

