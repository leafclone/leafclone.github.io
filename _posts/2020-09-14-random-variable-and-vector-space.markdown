---
layout: post
mathjax: true
title:  "Random variables, abstract vector space, and norm"
date:   2020-09-14 21:52:07 -0500
categories: jekyll update
---
{% include mathjax.html %}

Some definitions

* _vector space_ is a set of objects such that the 8 axioms apply. (addition, scalar multiplication, existence of the "zero vector", etc.)
* _vector_ is just a fancy term for those objects. They don't even need coordinates (tuples)! One example is that functions are also vectors.
* _dimension_ is the cardinality of the linearly independent bases.
* _norm_ is a measure of magnitude. It needs to satisfy the 3 properties (triangle inequality, etc.)
  * vector spaces where its vectors have a defined norm is _normed vector space_
* _inner product_ measures the angle of directions between vectors. (In inner product space, a norm is defined to be $\lvert\lvert x \rvert\rvert := <x, x>$, so that we can see inner product also carries the information of magnitude, not only direction).
  * Inner product space should satisfy the 3 properties (Conjugate symmetry, positive-definiteness). A inner product space that is _complete_ is a _Hilbert space_. Random variables are in the Hilbert space (I think)

What is a vector? The answer is I don't care. Vector is a very abstract notion. Do not get tied up to the specifics when dealing with vectors, such as the number of coordinates (length of the tuple). 

Thinking of random variables in the context of inner product space is quite useful, since we can apply geometric intuitions like orthogonality, projection, and angles.

The pythagorean theorem also holds in inner product space, for orthogonal $x$ and $y$. (Trivial to prove)

$$
\lvert\lvert x \rvert\rvert^2 + \lvert\lvert y \rvert\rvert^2 = \lvert\lvert x + y \rvert\rvert^2
$$

References
* [Random variables in hilbert space][x] 

[x]: {{ site.baseurl }}/pdfs/berkeley_ee126.pdf

