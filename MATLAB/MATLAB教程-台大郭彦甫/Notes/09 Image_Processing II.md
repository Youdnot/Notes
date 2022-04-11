# 09Image_Processing II
## Contents
- Image thresholding
- Background image estimation
- Component-connected labeling
## Problem Setup
eg: count the rice grains and identify their sizes in this image

### strategies:

- Binarize the image
  - white rice, black background
- Calculate connected rice

## Image Thresholding 图像二值化

A gray-level image can be turned into a binary image by using a threshold.
将一张灰阶图像转化为一张二进制图片

threshold 门槛？
### `graythresh()`
- computes an optimal threshold level
- Find the optimal threshold

### `im2bw()`

- `im2bw()` converts an images into binary image

## Background Estimation

- 提取不规则的背景并减去，从而得到较好的 threshold 效果
- Estimation for the gray level of the background
  - 估计背景的灰阶
- Background Subtraction
  - 背景提取
- Thresholding on Background Removed Image
  - 在减去背景的图片上 Threshold

## Connected-component Labeling

- A procedure for assigning a unique label to each object
  - 一种算法，对每个独特对象打上标签，用于识别图像中的物体/Component
- 将相邻且颜色相同/近的像素打上相同的标签，对不同的 Component（即相邻的一片同色像素）打上不同的标签
- Iterative process until all the pixels are checked
  - 迭代直至所有像素都检查完毕

### `bwlabel()`

- Built-in connected-component labeling algorithm
- 输出名为`labeled`的矩阵

### Color-coding Objects: `label2rgb()`
- Converts a label matrix into an RGB color image
  - 用色彩标号/color coded 
- Visualize the labeled regions

### Object Properties: `regionprops` 
- Provide a set of properties for each connected component

### Interactive Selection: `bwselect`
- Let you select objects using the mouse

