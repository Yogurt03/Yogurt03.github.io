---
title: 利用Termux和hexo搭建个人博客
categories: Termux
tags:
  - Termux
  - github
abbrlink: 88a3d208
date: 2020-03-01 08:33:54
cover: https://i.loli.net/2019/07/21/5d33d5dc1531213134.png
coverWidth: 1200
coverHeight: 750
---
这几天闲了无聊，就无聊的折腾了一下博客相关的东西。这篇文章就记录一下我自己的搭建过程，防止萌新踩坑。
<!--more-->
## 新建一个github仓库
这个不用多说吧，仓库名字一定要是`github用户名.github.io`

{% asset_img 4.jpg 创建仓库 %}

## 在termux里安装hexo
首先先在termux里安装git，nodejs，hexo

安装git：`apt install git`
安装nodejs：`apt install nodejs`
安装hexo：`npm install -g hexo-cli`

{% asset_img 1.jpg 安装git %}
{% asset_img 2.jpg 安装nodejs %}
{% asset_img 3.jpg 安装hexo %}

## 开始搭建博客
新建一个文件夹，名字随意。这个文件夹里面包含你博客相关的所有东西。我们cd进这个文件夹，然后输入hexo init下载需要的文件。完成后我们安装一个部署到git的插件。

> mkdir blog
> cd blog
> hexo init
> npm install hexo-deploy-git --save

{% asset_img 5.jpg 创建文件 %}
{% asset_img 6.jpg 初始化 %}
{% asset_img 7.jpg 初始化2 %}
{% asset_img 11.jpg 安装部署插件 %}

初始化完成后我们要编辑里面的_config.yml文件，要修改的内容我在图片里已经标注出来了

{% asset_img 8.jpg 修改配置文件 %}
{% asset_img 9.jpg 修改配置文件2 %}

修改完配置文件后，保存退出。接着开始编译博客文件命令为`hexo g`，编译完成后输入`hexo s`在本地开启博客，注意这个时候不要把termux关了，切记，切记。

{% asset_img 10.jpg "hexo g" %}
{% asset_img 12.jpg "hexo s" %}

这时候我们在浏览器输入`http://localhost:4000`就能进去到我们的博客里面了

{% asset_img 13.jpg 进去本地博客 %}
{% asset_img 14.jpg 浏览本地博客 %}

接下来就可以开始写博客了，新建一篇文章`hexo n "文章名字"`，创建完成它会提醒文件在哪里，修改里面的`title: `内容，这个才是你文章的标题。在`---`的下面就可以编辑内容了，注意它使用的是markdown语法

{% asset_img 16.jpg 新建文章 %}
{% asset_img 17.jpg 修改文章 %}

编辑完成后我们重新编译一次，每次更改都需要重新编译一次。建议每次编译前先`hexo clean`清理一下上次编译的内容在编译。

{% asset_img 18.jpg 编译 %}
{% asset_img 19.jpg 开启 %}

这时候我们在访问`http://localhost:4000`就可以看到我们刚才创建的文章了

{% asset_img 20.jpg 浏览 %}

写完文章后输入`hexo d`就可以把文章部署到github了

{% asset_img 15.jpg 部署 %}

部署到github后，让你的朋友在浏览器输入你的仓库名就可以访问你的博客了。

