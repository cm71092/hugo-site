---
title: 零基础小白也能免费搭建自己的博客【01】/基于Hugo+Github仓库+Netlify部署+Decap CMS的博客搭建教程
date: 2025-03-11
image: 新建项目.png
tags:
  - 教程
  - hugo
  - github
  - netlify
  - decap
  - cms
categories:
  - 技术
description: 封面是我自己P的
---
## 写在前头

　　本人为了以后找个好工作，目前在学习各种技能中。在这个过程中多次感觉到，如果有一个属于自己的网站，可以方便存放平时的心得体会和整理搜集到的资料，就可以免去重复翻阅复习的繁琐过程，同时还能加深学习印象，因此萌生了自己搭建博客的想法，毕竟在互联网时代，最不缺的就是各种方便的教程，同时还有强大的ai辅助工具。

> *~~当然，真正让我动手的其实是2025年1月神番Ave Mujica，剧情狗屎程度让我破口大骂制作组，然而在每周四看完更新跟群友怒喷到凌晨三点后，我发现不能再折磨群友和自己的作息了，遂决定搭建一个博客让我能够随时写下自己的观后感，以免跟群友大晚上发散剧情到凌晨三点。~~*

## 为什么要写这篇教程？

　　在我学习的过程中，不可避免的碰到许多问题，制作这个博客总共花了我大概一周的时间，实际上以我这种搭建博客的方法，并不需要这么久的时间，毕竟这种方法并不涉及前端或者后端开发。为了记录我在搭建博客中踩到的各种坑，以及方便想要搭建自己博客的小伙伴（真的有吗），我决定动手写一篇教程来记录我的博客搭建过程，起码也留下一个记录方便给自己看嘛。

　　不过因为我不懂前端后端，要是跟着教程走出错了，也只能自己多检查一下前面有哪里出错啦。

## 需要哪些步骤？

　　就像标题写的，这种博客搭建方法**基于Hugo+Github仓库+Netlify部署+Decap CMS**，因此搭建步骤也离不开这些东西，过程大概可以分成以下几步：

1. 事前准备，包括必要软件的下载以及账号注册等
2. hugo本地站点的创建
3. 上传到github远程仓库并进行Netlify部署
4. 使用Decap CMS进行可视化内容管理的搭建

## 事前准备

> 良好的准备让事情成功一半。　　　　　　　　 　　　　　　　　————Ｗ·兹基·硕德

### （一）安装git for windows

　　git终端将是我们后面进行网站创建以及修改推送的重要工具，**必须安装**，具体安装教程可以参考：[](https://blog.csdn.net/middle_age666/article/details/141157518)
[Windows系统上Git详细图文安装及使用教程_git安装及配置教程-CSDN博客](https://blog.csdn.net/middle_age666/article/details/141157518)

### [](https://blog.csdn.net/middle_age666/article/details/141157518)（二）安装VS code（非必须）

　　vscode是一款功能强大的源代码编辑器，虽然是非必须下载，但是有了vscode可以让后续的许多操作变得更方便，包括编辑配置文件等，安装教程可以参考：
[如何安装vscode？看这一篇就够了 - 知乎](https://zhuanlan.zhihu.com/p/687410421)[](https://blog.csdn.net/middle_age666/article/details/141157518)[](https://blog.csdn.net/middle_age666/article/details/141157518)

### [](https://blog.csdn.net/middle_age666/article/details/141157518)（三）安装HUGO

hugo的官方文档给出了详细的的安装教程：
[Windows](https://gohugo.io/installation/windows/)

这里只介绍其中的Chocolatey安装步骤。

1. 打开命令提示符：按`win+R`打开运行框（`win`键就是键盘上那个windows图标），输入`cmd`进入命令提示符。
2. 安装包管理工具Chocolatey，输入：`@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"`
3. 等待安装完成后，安装hugo，输入：`choco install hugo-extended`
4. 成功安装，如果安装Chocolatey出现问题，请查看这篇文章（比较麻烦不推荐）：
   [windows 下安装Chocolatey（强大的软件包管理工具）_chocolatey软件免费么-CSDN博客](https://blog.csdn.net/LOER_C/article/details/116591459)


### （四）注册Github账号

如果你没有Github账号，立即注册一个。打开官网：
[GitHub · Build and ship software on a single, collaborative platform · GitHub](https://github.com/)

点击右上角**Sign up**注册账号。

### （五）注册Netlify账号

Netlify是一个提供远程部署静态站点服务的网站，提供免费二级域名，不用花钱买域名就能远程访问你的私人博客，打开官网：
[Scale & Ship Faster with a Composable Web Architecture | Netlify](https://www.netlify.com/)

点击右上角**Sign up**注册账号。


> 至此，🥰恭喜你已经完成了所有的前期准备工作，下一篇博客将教会你如何在本地部署hugo网站，敬请期待。
>

[](https://blog.csdn.net/middle_age666/article/details/141157518)

[](https://blog.csdn.net/middle_age666/article/details/141157518)
