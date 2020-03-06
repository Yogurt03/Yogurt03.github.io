---
title: '"AutoMux"更方便、便捷的为你的Termux安装所需工具'
cover: 'https://cdn.jsdelivr.net/gh/Bcap03/AutoMux@master/Module/automux.png'
coverWidth: 1440
coverHeight: 960
categories: Termux
tags:
  - github
  - Termux
  - AutoMux
abbrlink: 4457f156
date: 2020-02-28 22:35:07
---
AutoMux专门为懒人设计,帮懒人一键安装所需工具.
作者就是我自己,本来呢是为了我和酸奶两个懒人所写,上传到github后想了想,都上传到github了那就独乐乐不如众乐乐吧!
<!--more-->
## 截图

{% asset_img automux.jpg 工具截图 %}

## Github地址
https://www.github.com/Bcap03/AutoMux/

## 安装和使用方法
没啥好说的，安装完直接在终端输入`automux`就能启动，还有一种就是克隆下来后，cd进AutoMux然后python automux.py,第一次启动必定报错，先给权限，再安装termcolor依赖就可以启动了

给予权限：`chmod +x automux.py`
依赖安装：`pip install termcolor`

### 懒人一键安装
> sh -c "$(curl https://raw.githubusercontent.com/Bcap03/AutoMux/master/script/install.sh)"

### 懒人手动安装
1. git clone https://www.github.com/Bcap03/AutoMux.git
2. cd AutoMux
3. chmod +x install.sh
4. ./install.sh
5. automux

