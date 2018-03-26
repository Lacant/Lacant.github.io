---
title: rebuilt hexo on github
date: 2018-3-20 21:55:29
tags: [hexo,小白]
categories: 网络技术
toc: true
---
托管在github上的blog有两年没用了，今天在旧文件的基础上，重新用hexo进行deploy。同时也是对git和hexo的一次重新梳理。
<!-- more -->

### 准备
- Node.js
- Git

用以下指令查看是否安装,正确安装的情况下会显示版本号（PS:选最新的版本）
	    
	$ node -v
	$ npm -v

### Git配置
#### 用户信息
- 这里的“username"是可以任意填写的

		$ git config --global user.name "username"
		$ git config --global user.email "johndoe@example.com"

- 查看配置信息

		$ git config --list
		
#### 密钥配置
- 查看是否已经有了密钥
	- 在 Windows 系统上，Git 会找寻用户主目录下的 .gitconfig 文件。主目录即 $HOME 变量指定的目录，一般都是 C:\Documents and Settings\$USER;
	- 在主目录下找到 .ssh 文件夹，进去之看查看下有没有 id_rsa 和 id_rsa.pub 这两个文件分别对应私钥与公钥;
	- 生成密钥
		
			$ git ssh-keygen -t rsa -C “username@example.com”
			
	- 添加密钥到ssh
			$ ssh-add id_rsa.pub
	- 添加密钥到github
	- 测试密钥是否成功添加
			
			$ ssh git@github.com

### Hexo配置
#### 安装Hexo

- Hexo的安装，可以理解为安装了一个hexo的独立程序，视自己需求，是否新建一个文件夹，建议新建;
		
		$ npm install hexo-cli -g
		$ npm install hexo --save
- 查看是否成功安装

		$ hexo -v
		
#### 配置Hexo

- 如果hexo的安装是一个独立程序的话，hexo配置的过程就是安装一个完整网站的全部内容，所以此时是要新建一个空文件夹的。
理论上我觉得可以多次进行hexo的配置，每次的配置就是重新建一个blog，新建的文件夹就是blog的全部内容。

		$ hexo init
		$ npm install

#### 试运行hexo 

	$ hexo clean
	$ hexo g
	$ hexo d
	$ hexo s       % 运行本地服务 http://localhost:4000
