---
title: 概率论与数理统计基本概念
date: 2016-9-12 22:55:29
tags: [概念,概率论与数理统计]
categories: 高等数学
toc: true
---
数理统计学习基础概念明析

<!-- more -->

## 随机变量  
* 定义：设随机试验E的样本空间为 **Ω** ={ω}，如果对每一个 ω ∈ **Ω**，都有唯一的实数X(ω)与之对应，并且对任意实数x，{ω：X(ω)≤ x}是随机事件，则称定义在 **Ω**上的实单值函数X(ω)为随机变量，简记为随机变量 <large>**X**。
 * 离散型随机变量(discrete random variables)：如果随机变量 <large>**X**只可能取有限个或可列个值x<sub>1</sub>,x<sub>2</sub>,...,则称 <large>**X**为离散型随机变量。
 * 连续型随机变量(continuous random variables)：对于某一随机变量 <large>**X**，若存在非负可积函数f(x)，使得F(x)=∫<sup>x</sup> f(t)dt,(-∞< x <+∞) , 则称 <large>**X**为连续型随机变量。
 * 上面三条是从书上抄的定义，按老师的讲法，这是纯苏联式的思维，抽象，不好理解。这里再附上一个美国式的数学思维，也就是我个人的理解。① 随机变量是函数，而非一个确定的数值；② 进一步理解，随机变量可看做是一个人为定义的事件，如：throwing dice，5次里面2次得2的概率；③ 连续型随机变量的理解可以用下雨的例子，如明天下雨记为1，不下则记0，这是离散的；但如果把X的描述定义为明天的降雨量，则就变成连续的了。因为要定义降雨量，可以有无数种可能，比如20mm,30mm,40mm,40.001mm...是无法穷尽的。  

## 分布函数(Cumulation distribution function)  
* 定义：随机变量 <large>**X**，x是任意实数，称函数F(x)=P{<large>**X**≤ x} (x∈R)为随机变量 <large>**X**的分布函数，或称 <large>**X**服从分布F(x)，记为 <large>**X**～ F(x)。  
 * 分布函数是PDF的累加，是为了测算连续型随机变量的概念密度的一个数学工具。  

## 8种重要分布
* 0-1分布  
* 二项分布(Binomial Probability Distribution)
* 几何分布(Geology Distribution)(等待型分布)
* 超几何分布(古典概型)
* 泊松分布(Poisson Distribution)
* 均匀分布
* 指数分布
* 正态分布