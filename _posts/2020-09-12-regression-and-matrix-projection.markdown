---
layout: post
mathjax: true
title:  "Least squares regression and matrix projection"
date:   2020-09-12 21:52:07 -0500
categories: jekyll update
---
{% include mathjax.html %}

Let's view the data $\mathbf{X}_{N\times p}$ as a $p$-dimensional plane in in $\mathbb{R}^N$, i.e. a subspace spanned by $p$ basis vectors.

$\mathbf{X}\beta=\mathbf{y}$ may (likely) not have a solution, so we instead project $\mathbf{y}$ onto the subspace described above and get $\mathbf{X}\hat{\beta}=\hat{\mathbf{y}}$.

Why project? Because $\hat{\mathbf{y}}$ is the closest vector on the subspace in terms of euclidiean distance, which means norm of $\mathbf{e}$ is minimized where $\mathbf{e} = \mathbf{y}-\hat{\mathbf{y}}$, which minimizes the least squares.

$\mathbf{e}$ is orthogonal to the plane (by definition of projection, i think), and hence 

$$
\mathbf{x_1}^T\mathbf{e} = 0
\\
...
\\
\mathbf{x_p}^T\mathbf{e} = 0
$$

or in matrix form,

$$
\mathbf{X}^T\mathbf{e} = 0
\\
\mathbf{X}^T(\mathbf{y} - \mathbf{X}\hat{\beta}) = 0
\\
\mathbf{X}^T\mathbf{X}\hat{\beta} = \mathbf{X}^T\mathbf{y}
\\
\hat{\beta} = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{y}
\\
\mathbf{X}\hat{\beta} = \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{y}
$$

and the projection matrix is $\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T$

References
* [Matrix projection][matrix-projection] 

[matrix-projection]: {{ site.baseurl }}/pdfs/MatrixProjection.pdf

