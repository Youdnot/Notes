# 07Graphical_User_Interface

# GUI 图形化用户界面

## Contents

- Graphical User Interface 

## Introduction

User interface (UI) is a method of interaction  between a person and a computer.

## Start A GUI Program

1. Set your “current folder” where you want to store  the GUI program 
   设置工作文件夹
2. Use GUIDE (graphical user interface design  environment) to create a MATLAB GUI  interactively by typing in guide command  window
   Type `guide` (graphical user interface design  environment) to create a MATLAB GUI  interactively
   使用 `guide` 创建
3. 在 GUIDE Quick Start 中选择 “Blank GUI (Default)” 

设置在命令中显示名字

### Align

### Label the Push Buttons

### GUI Script Structure

存在两个文件，一个为图形化文件，一个为系统自动生成的 `.m` 文件

### Callback of An Object

按下按钮的执行程序

机制：检查一个按钮是否有被触发？

### handles – information of the GUI objects

当有多个图像时需要注意

未指定时，按下按钮生成的图像会出现在最新/后创建的图像位上 

两种指定方式

#### Set the axes for Plotting

#### Review – set() and get()

### Handles to Store Variables

将 local variables 转化为 global varibles

### 程序打包输出 `.exe`

已更新为APP设计工具，知识需更新