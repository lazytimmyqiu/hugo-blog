+++
title = '用Hugo和Github Pages搭建自己的blog'
date = 2024-05-06T01:04:10+08:00
draft = false
tags = ['写作']
+++

时隔多年，又一次重新拾起个人blog，记录一下这次折腾的起点。

这些年陆陆续续尝试过不同的博客方案，按时间排序主要有3种：
1. 博客写作网站
2. wordpress + 云托管
3. hexo/jekyll/hugo + Github Pages托管

第1种方法很快就放弃了，因为总感觉在上面生产的内容不属于自己。基于wordpress的方案相对自主，但对于我这种轻量级写作的人来说，过于笨重了，特别是需要一个云主机进行托管，还要自己折腾域名。

所以最终还是选择第3种方案，原理上还是比较容易理解的，通过第三方库自动生成基于HTML和CSS的静态网站目录，然后通过Github Pages托管部署。hexo和jekyll在很早之前都尝试过了，这次选择了hugo尝尝鲜。

# Hugo的安装和配置
[安装文档](https://gohugo.io/installation/)

和大部分软件一样有3种安装模式
* 下载二进制包
* 通过某些包管理器安装
* 从源码编译
个人感觉直接下载二进制包是最方便的，**注意下载后把二进制文件的目录加入PATH中**

[快速配置](https://gohugo.io/getting-started/quick-start/)

参考该文档可以快速在本地配置和调试文档，还可以测试不同的theme

# Gihub Pages上的部署
[部署文档](https://gohugo.io/hosting-and-deployment/hosting-on-github/)

通过该文档配置github上的workflow即可，以后只需在本地进行文档的编辑和可视化调试，然后
```
git push -u origin main
```
即可。