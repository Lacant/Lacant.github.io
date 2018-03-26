---
title: 文科小白Hexo建站
date: 2016-7-17 08:55:29
tags: [hexo,小白]
categories: 网络技术
toc: true
---

作为一个毫无代码经验的理科生，得幸有些扎实的互联网基础，这篇文章是为了分享在建站的过程可会遇到一些的基本概念，撑握了这些概念，便能方便地使用Github来搭建个人博客。同时也是回应在Wechat公众号里发布的收费课程，在我的概念里，互联网的精神是分享，将这类简单的技术做成收费视频，是我坚决抵制的，毕竟我们只为了搭建一个可以自由写作的平台，仅此而已。
<!-- more -->

## 基础篇

* 在当今这个年代，如果你还停留在认为**百度**是最牛的搜索工具，那后面的内容可以忽视了，互联网作为最大的免费资源社区，使用**Google**是最基本的技能，在国内，能否使**Google**在某种意义上已经可以代表了互联网知识的一类水平。
* **CMD**是windows系统自带的命令行窗口，它长这个样子：

  <img src="https://xuanwo.org/imgs/opinion/Nodejs-test.png" alt="GitHub" title="GitHub,Social Coding" width="500" height="350" />

* **Git Bash** 是Github提供的命令行工具，我是在“HEXO的本地配置”完成后，才开始使用Git Bash 工具的。但要注意的是Git Bash必须要在HEXO的根目录下执行命令，否则会失败。
* 在完成HEXO的本地配置后，第一个要做的当然是换主题，后面的教程里提供了主题下载的地址，我使用的是Next主题，因为有写得比较简单的教程。首先是打开**Git Bash**命令行窗口，(**记得一定得是在HEXO根目录下面**)输入如下指令：
>git clone https://github.com/iissnan/hexo-theme-next themes/next

 主题会自动下载，后面就是[配置主题](http://theme-next.iissnan.com/getting-started.html)，这里只讲概念，具体操作参考后面提供的教程。

* **Hexo**中必用的四个指令，我也只会这四个。

 清除冗余的意思
>hexo clean     

 生成文档的意思
 >hexo g        

 生成在本地预览
 >hexo server   

 将本地文档上传至GitHub
 >hexo deploy

 以上四个指令是最常用的，在主题配置完成后，每次只需执行**文档上传**的指令就能自动完成博文的更新。

 ## 教程篇
* 网络上提供的教程有很多，我转载一篇写得很入门级的，适合零基础的人的使用方法。这篇文章来自 [**Xuanwo'blog**](https://xuanwo.org/2015/03/26/hexo-intor/)

  今天花了一天的时间，总算是把站给搭出来了，还是有些小成就的，虽然很是简陋，但是有了最础的功能，对我来说就够了，因为这个站原本就是希望做成为一个记录自已学习成长的小世界，记录点滴，在未来给自己还原一个更加生动的回忆。
