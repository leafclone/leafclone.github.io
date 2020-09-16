---
layout: post
mathjax: true
title:  "Least squares regression and matrix projection"
date:   2020-09-12 21:52:07 -0500
categories: jekyll update
---
{% include mathjax.html %}

One way to view the data $\mathbf{X}_{N\times p}$ as a $p$-dimensional plane in in $\mathbb{R}^N$, i.e. a subspace spanned by $p$ basis vectors. Remember that definition of dimension is the cardinality of the bases. The number of coordinates, $N$, is not important. When thinking of projection, think of just working inside the abstract vector space framework. We just happened to treat the vector as that in the $n$-Euclidean space.

In such context, $\hat{\mathbf{y}}$ is the projection on the plane. This has two implications. $\hat{\mathbf{y}}$ is the linear combination of the basis vectors $\mathbf{x_1},..,\mathbf{x_p}$, and $\hat{\mathbf{y}}$ is the closest point on the plane to $\mathbf{y}$, in a euclidean distance sense. This means norm of $\mathbf{e}$ is minimized where $\mathbf{e} = \mathbf{y}-\hat{\mathbf{y}}$, which minimizes the least squares.

Outside of the regression context, why do people use projections in general? $\mathbf{X}\beta=\mathbf{y}$ may (likely) not have a solution, so we instead project $\mathbf{y}$ onto the subspace described above and solve $\mathbf{X}\hat{\beta}=\hat{\mathbf{y}}$.

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

