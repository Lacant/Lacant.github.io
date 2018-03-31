---
title: machine learning ex2
toc: true
date: 2018-03-31 10:45:14
tags: [机器学习,作业,练习]
categories: 学习成长
---

机器学习编程练习ex2学习小结

<!-- more -->

## exm2.m总纲

<div align=center>
<img src="https://github.com/Lacant/blogimg/raw/master/180331/exm2.PNG" alt="git" title="Job exm2" width="500" height="300" />
</div>

### code from exm2.m

- add intercept term to martix X, output $X_{m*(n+1)}$;

    ```javascript
[m, n] = size(X);
X = [ones(m, 1) X];    % Add 1 colum to marix X
	```

- initialize fitting parameters, output $\theta_{(n+1)*1}$;

    ```javascript
initial_theta = zeros(n + 1, 1);
	```

- Predict probability:$h_{\theta}(x^{(i)}) =\frac{1}{1+e^{-X\theta}}$

- define initial cost and gradient function;

- output initial cost and gradient;

- Set options for fminunc function;
	```javascript
	options = optimset('GradObj', 'on', 'MaxIter', 400);
	[theta, cost] = fminunc(@(t)(costFunction(t, X, y)), initial_theta, options); % @(t)(costFunction(t, X, y)) 'short-hand' for costFunction;
	```

- output $\theta$ and cost with 400 gradients;

