---
layout: post
title:  "Extending Operators on Hilbert spaces"
date:   2021-11-18 21:40:17 -0200
categories: jekyll update
---

Let $V$ and $W$ be vector spaces, it's well known that an operator $T: V \to W$ is uniquely defined by its value on the (Hamel)
basis vectors $T(e_\lambda)$. Moreover, the choice of these $T(e_\lambda)$ is arbitrary in the sense that each possible choice corresponds to an operator.

This characterization is very useful when $V$ is finite dimensional, but is less so when it isn't. The reason being Hamel basis themselves become less usefull in infinite dimensional vector spaces, since they tend to blow up fast; e.g., the Hamel basis for $\ell^2$ is uncountable.

In Hilbert spaces, there is an alternative notion of basis: the Hilbert (or orthonormal) basis.

<div class="definition" text='Hilbert basis'>
Let $B$ be a set of orthonormal vectors on a Hilbert space $H$, we say $B$ is a Hilbert basis when it exhausts all axis in the following sense:

$$\forall h \in H: [\forall b \in B: h \perp b] \rightarrow h = 0$$
</div>

Using Zorn's lemma and a bit of additional Set Theory, we are able to prove three fundamental results.

<div class="theorem">
Every Hilbert space has a Hilbert basis.
</div>

<div class="theorem">
All Hilbert basis on a given Hilbert space have the same cardinality.
</div>

<div class="theorem">
Every set of orthonormal vectors can be extended into a Hilbert basis.
</div><br>

With this we are able to define the orthogonal dimensional (as opposed to the usual algebraic dimension) of a Hilbert space.

<div class="definition" text='Orthogonal Dimension'>
The Orthogonal dimension of a given Hilbert space is the cardinal number associated to any given Hilbert basis of this space.
</div><br>

Hilbert basis have all the usual desirable properties

1. Every vector $x \in H$ can be uniquely expressed as $\sum \langle x, e_\lambda \rangle e_\lambda$.
2. Norms can be easily computed: $\lvert\lvert x \rvert\rvert^2 = \sum x_\lambda^2$.
3. Inner products can be easily computed: $\langle x, y \rangle = \sum x_\lambda y_\lambda$.

These expressions are all well defined due to the following theorem.

<div class="theorem" text='Summability'>
Let $H$ be a Hilbert space and $B$ be any set of orthonormal vectors in $H$, then, for every $x \in H$, the next set is countable.

$$E := \{ b \in B: |\langle x, b \rangle| > 0 \}$$
</div><br>

In the most interesting case where $B$ is denumerable, we get plain old series. Lastly, in the usual sense, there is a unique Hilbert space for every cardinal $\kappa$. Indeed, consider the following definition.

<div class="definition" text='Isomorphism'>
Let $T: H_1 \to H_2$ be a bijective linear map between two Hilbert spaces $H_1$ and $H_2$ such that

$$\forall x,y: \langle x, y \rangle = \langle Tx, Ty \rangle$$

then we say $T$ is a Hilbert space isomorphism. Note the resulting map is also an isometry.
</div><br>

With this, we have the expected theorem.

<div class="theorem">
Two Hilbert spaces are isomorphic if, and only if, they have the same Orthogonal dimension.
</div><br>

Now we are ready to discuss extensions of linear operators defined on Hilbert spaces. We begin with the easy case of bounded linear functionals.

<div class="theorem">
$\phi: H \to \mathbb{R}$ is a bounded linear functional on a separable Hilbert space if, and only if, $\phi(e_n) \in \ell^2$.
</div><br>

The proof goes in the lines of: if $\phi(e_n) \in \ell^2$, then $z = \sum_{n=1}^\infty \phi(e_n)e_n$ is a vector of $H$. Thus, $\phi(x) = \langle x, z \rangle$ and linearity/continuity stem from properties of the inner product. If, on the other hand, $\phi$ is a bounded linear function, then it can be shown (using Riesz's Representation Theorem) that $\phi(e_n) \in \ell^2$.

The next case to consider is bounded linear operators from $H$ into itself. Clearly, it is a necessary condition that the individual coordinates of each $T(e_n)$ form a sequence in $\ell^2$, but this is not sufficient. Indeed, if we let $T(e_n) = t$ for any non-zero $t$, then $T(\sum_{n=1}^\infty \frac{1}{n}e_n) = \sum_{n=1}^\infty \frac{1}{n}z$, which clearly diverges.