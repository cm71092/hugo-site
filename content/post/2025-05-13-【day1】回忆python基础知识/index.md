---
title: 【Day1】回忆python基础知识
date: 2025-05-13T10:55:00+08:00
lastmod: 2025-05-13T10:55:00+08:00
tags:
  - python
categories:
  - 技术
---
* 安装了AI编程助手Fitten Code
* Python 通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠 \来实现多行语句
* 字符串切片 str\[start:end]，其中 start(包含)是切片开始的索引，end(不包含)是切片结束的索引，即start到end-1
* 字符串的切片可以加上步长参数 step，语法格式如下:str\[start:end:step]
* Python 中的字符串有两种索引方式，从左往右以0开始，即0，1，2，....，从右往左以 -1 开始，即...，-3，-2，-1
* Python 可以在同一行中使用多条语句，语句之间使用分号`;`分割：
* ```
  import sys; x = 'runoob'; sys.stdout.write(x + '\n')
  ```
* print 默认输出是换行的，如果要实现不换行需要在变量末尾加上 end=""
*
