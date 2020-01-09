---
layout: post
title: Kernel Density estimation
---
##Estimating Probability Density Functions
**Density Estimation** is the problem of recovering the probability distribution of a random variable $\mathbf{X}$ from a set of realizations $x_{1},x_{2},x_{3},...x_{n}$.
The simplest approach to estimate the distribution is to split the sample space up into bins and count how many samples fall into each bin. The intuition behind this estimator is that as we hold the bins fixed and take more data, the relative frequency will converge on the bin's probability. A crude way to get the pdfs is to assume uniform probability density within each bin. This is essentialy trying to approximate the pdf by a piecewise-constant density function. Unfortunately, the binning can have dire consequences on the reconstruction as it obeys the traditional bias-variance trade-off. Using more bins will lead to a decrease in the bias of our estiamtes but will increase the variance and vice-versa.
For $M$ bins uniformly spaced, the optimal number (bandwidth selection) minimising the MSE leads to:
\begin{equation}
M_{opt}=(\frac{nL^{2}}{p(x^{*})})^{1/3}
\end{equation}

Where $L$ bounds the derivative of the probability density function $p(x)$. Although these two quantities are unknown, this gives insights on how we should change the number of bins as the sample size $n$ changes.

![_config.yml]({{ site.baseurl }}/images/config.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
