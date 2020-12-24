---
layout: post
mathjax: true
title:  "Various variance decompositions"
date:   2020-12-21 21:52:07 -0500
categories: jekyll update
---
{% include mathjax.html %}

## Partition of Sums of Squares

Below is just mental model for OLS

$$
\begin{align}
Var(Y) &= E[(Y-\bar{Y})^2] \\ 
(\text{just back of envelope}) &= \underbrace{E[(Y-\hat{Y})^2]}_{\text{Unexplained variance}} + \underbrace{E[(\hat{Y}-\bar{Y})^2]}_{\text{, Explained variance}}\\
( \text{In OLS, $\bar{Y} = E[\hat{Y}]$}) &= E[(Y-\hat{Y})^2] + Var(\hat{Y}) \\
\end{align}
$$

Above is analogous to

$$
\begin{align}
\sum{(Y_i - \bar{Y})^2} = \sum{(Y_i - \hat{Y_i})^2} + \sum{(\hat{Y_i} - \bar{Y})^2}\\
\end{align}
$$

## Bias Variance decomposition

$$
\begin{align}
E[(Y-\hat{Y}^2) | X = x_0] &= E[(Y - E[\hat{y}])^2 | X = x_0] + E[ (E[\hat{Y}] - \hat{Y} )^2 ] \\
(\text{Assuming $Y$ is a deterministic function of $x_0$}) &= \underbrace{(Y-E[\hat{Y}])^2}_{Bias^2} + Var_{\tau}(\hat{Y}) \\
\end{align}
$$

Note that bias doesn't contain any randomness (unless there is random noise added to $Y=f(X)$). $Var_{\tau}(\hat{Y})$ can be interpreted as the sensitivity of our prediction to the sampled training dataset. 

