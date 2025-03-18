---
title: 基于miniconda的tensorflow安装及如何在pycharm中调用
date: 2025-03-18
image: https://res.cloudinary.com/dwzwo1e1p/image/upload/v1742267802/9ae232904b565006334648e1de2d084_dnau4h.png
tags:
  - python
  - tensorflow
categories:
  - 技术
description: 学习小结
---
参考：
[](https://www.bilibili.com/video/BV1Zt411T7zE?spm_id_from=333.788.videopod.episodes&vd_source=34662320f69a066dd6a6ecb5b16dcd7a)

* [Tensorflow2.0入门与实战 最通俗易懂的入门课程 极简TensorFlow入门_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Zt411T7zE?spm_id_from=333.788.videopod.episodes&vd_source=34662320f69a066dd6a6ecb5b16dcd7a)
* [](https://www.bilibili.com/video/BV1Zt411T7zE?spm_id_from=333.788.videopod.episodes&vd_source=34662320f69a066dd6a6ecb5b16dcd7a)
  [miniconda和pyCharm的安装使用-CSDN博客](https://blog.csdn.net/yk071300/article/details/142590968)



默认已经安装了pycharm

- - -

## 下载miniconda

进入官网
[Index of /](https://repo.anaconda.com/miniconda/)

随便下一个py3.9的版本

![](https://res.cloudinary.com/dwzwo1e1p/image/upload/v1742268085/2bda8eb1268c450290a9edeb47e521c7_ib1pkl.png)

路径记得改到D盘，我是安装到D:/miniconda3

`win+S`搜索环境变量，在用户变量里找到Path，点击编辑，新建这三条：

* D:\miniconda3
* D:\miniconda3\Scripts
* D:\miniconda3\Library\bin

## 安装GPU版本tensorflow

### 安装辅助库

`win+S`搜索anaconda，进入anaconda promt命令行输入以下指令，记得输入y（yes）。

`conda create-n tf env python=3.9           # 创建虚拟环境`

`conda activate tf env                      # 激活虚拟环境`

`conda install cudatoolkit=11.3.1           # 安装辅助包`

`conda install cudnn=8.2.1`

### 安装tensorflow2.0GPU版本及其他辅助包

输入`pip install tensorflow-gpu==2.10.0`安装tensorflow

`pip install pandas matplotlib notebook`安装辅助包

## 在pycharm中调用conda环境

进入pycharm的设置，选中python解释器，点击右边的齿轮，有个添加，选择conda环境，选择现有环境，自动检测刚刚配置的虚拟环境，完成pycharm配置
