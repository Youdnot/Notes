# 09Image_Processing II
## Contents
- Image thresholding
- Background image estimation
- Component-connected labeling
## Problem Setup
eg: count the rice grains and identify their sizes in this image
## Image Thresholding
A gray-level image can be turned into a binary image by using a threshold.
一张灰阶图像可以通过该操作转化为一张二进制图片

threshold 门槛？
### `graythresh()` and `im2bw()`
`graythresh()` computes an optimal threshold level
`im2bw()` converts an images into binary image
## Background Estimation
Estimation for thegray level of the background
Background Subtraction
Thresolding on Background Removed Image

## Connected-component Labeling
希望识别图像中的特殊物体

A procedure for assigning a unique label to each object
对每个独特对象打上标签的过程
Finish labeling of a component
Iterative process until all the pixels are checked

`bwlabel()`

### Color-coding Objects `label2rgb()`
Converts a label matrix into an RGB color image
Visualize the labeled regions
### Object Properities `regionprops` 
Provide a set of properties for each connected component
### Interactive Selection `bwselect`
Let you select objects using the mouse

