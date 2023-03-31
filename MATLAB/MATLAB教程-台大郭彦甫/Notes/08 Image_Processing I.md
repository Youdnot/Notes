# 08Image_Processing I

*Slides在 Introduction 部分有更新，注意结构

## Contents

- Introduction to digital image
- Read and show images
- Image arithmetic  图像计算

## Digital Image and Its Acquisition 数字影像及其获取

传感器摄取 CMOS？

### Types of Digital Image

- **Binary**: Each pixel is just black or white  二进制
- **Grayscale**: Each pixel is a shade of gray, normally from 0  (black) to 255 (white)  灰阶
- **True color** or **RGB**: Each pixel has a particular color  described by the amount of red, green and blue in it  真彩或三色

#### Where Does the Color Come from?

Three kinds of light-sensitive photoreceptor cells  in the human eye (i.e., cone cells) respond most  to red, green and blue

人眼中有三种光敏感的受体细胞，主要对RGB三色响应。

#### Typical RGB Image

三个颜色通道的影像叠加，形成最终的RGB图片。

### Elements of Images

- **Binary**: 0 / 1
- **Grayscale**: 0-255 字长为一字节
  - 1 Byte; 8-bit;  即0-255
- **True color** or **RGB**: 三个矩阵，RGB各为一个Greyscale（Greyscale在RGB中表示**色深**？（印象中出现过的名词

## Read and Show An Image

- Read an image: `imread()`
- Show an image: `imshow()`

```Matlab
%Example:
clear, close all
I = imread('pout.tif'); %read  储存在矩阵I中
imshow(I); %show
```

### Image Variable in Workspace

| Name |  Size   | Bytes | Class |
| :--: | :-----: | :---: | :---: |
|  I   | 291x240 | 68940 | uint8 |

Image matrix

影像处理，即改变 Image matrix 中的数值。

### 指令

Image Info: `imageinfo()`

Image Viewer: `imtool()`

## Image Processing

Any form of signal processing for which the input  is an image.

任何形式的信号处理

### Image Arithmetic 影像的四则运算

`im` 前缀，即 image 和影像有关

|                |                                                              |
| -------------- | ------------------------------------------------------------ |
| imabsdiff      | Absolute difference of two images                            |
| im**add**      | Add two images or add constant to image                      |
| imapplymatrix  | Linear combination of color channels                         |
| imcomplement   | Complement image                                             |
| im**divide**   | Divide one image into another or divide image  by constant   |
| imlincomb      | Linear combination of images                                 |
| im**multiply** | Multiply two images or multiply image by constant            |
| im**subtract** | Subtract one image from another or subtract constant from image |

#### Image Multiplication `immultiply()` 

- 提高照片的亮度

#### Image Addition `imadd()` 

- 叠加照片
- 大小需相同
- 相加后，数值相加，画面会变亮，超出255范围会饱和

#### Image Histogram `imhist()` 

- 提取每个像素的灰阶数据并制成图表

#### Histogram Equalization `histeq()`

- 增加对比度
- 拉开灰阶范围
- ？图像均衡化

### Geometric Transformation

- 改变影像形状，实质为改变像素的位置，如旋转
- 处理指令见Slides

#### Image Rotation `imrotate()`

#### Write Image `imwrite()`

- 储存为不同格式
