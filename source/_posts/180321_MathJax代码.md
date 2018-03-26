---
title: Hexo中数学公式的表达
date: 2018-3-21 16:55:29
tags: [数学公式，机器学习]
categories: 网络技术 
toc: true
---

MathJax 在Hexo中的渲染问题

<!-- more -->
## BugFree
- hexo默认使用 hexo-renderer-marked 引擎去渲染网页，它会把利用Markdown语法写的文本去转换为相应的html标签。在利用Markdown写MathJax公式的时候，经常会用到下划线 *"__"* 表示下标，但是下划线 *"__"* 会被hexo的默认引擎 hexo-renderer-marked 渲染成html中的**"&lt;em&gt;"**标签，表示斜体，这样一来，我们写的MathJax公式就被错误渲染了，也就没办法正确显示出来。
- 解决方方案：替换渲染引擎（如果出错，尝试将npm升至最新版本）
		$ npm uninstall hexo-renderer-marked --save
		$ npm install hexo-renderer-kramed --save
- 定位到你的博客根目录，找到../node_modules/kramed/lib/rules/inline.js文件，作如下修改：
		$ //escape: /^\\([\\`*{}\[\]()#$+\-.!_>])/,                           第11行，将其修改为
		$   escape: /^\\([`*\[\]()#$+\-.!_>])/,
		$ //em: /^\b_((?:__|[\s\S])+?)_\b|^\*((?:\*\*|[\s\S])+?)\*(?!\*)/,    第20行，将其修改为
		$   em: /^\*((?:\*\*|[\s\S])+?)\*(?!\*)/,
## 代码实现案例

- sigmoid function：$g(z)=\frac{1}{e+e^{-z}}$
		$ g(z)=\frac{1}{e+e^{-z}}
- sum function: $\sum_{i=1}^n a_i=0$ ($ 表示行内公式)
		$ \sum_{i=1}^n a_i=0
- sum function: $$\sum_{i=1}^n a_i=0$$ ($$ 表示整行公式)
		$ \sum_{i=1}^n a_i=0
- 多元函数：$f(x_1,x_2,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2$
		$ f(x_1,x_2,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2

$$\frac{\partial u}{\partial t}= h^2 \left( \frac{\partial^2 u}{\partial x^2} +\frac{\partial^2 u}{\partial y^2} +\frac{\partial^2 u}{\partial z^2}\right)$$ 



- 微分:$$\frac{\mathrm d}{\mathrm d x} \left( k g(x) \right)$$