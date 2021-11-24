---
layout: post
title:  "Trigonometric functions"
date:   2021-11-18 21:40:17 -0200
categories: jekyll update
---

The geometric definition of trig functions we learn in school is not rigourous since Euclidean Geometry (the results derived from Euclid's axioms) isn't trully just theorems from the axioms, it involves geometric intuition as well. Moreover, most of Modern Math is done inside the set theoretical framework of ZFC. Thus, even if we had learned geometry from Hilbert, which is rigorous, we would have to abandon it (the formal consequences; the intuition remains the same) when working with Analysis. Hence, the only viable alternative is to give abstract definitions for the trigonometric functions.

One example of such definition would be the power series representation of sine and cossine.

$$\begin{align}
\sin(x) &= \sum_{n=0}^\infty \frac{(-1)^n}{(2n+1)!}x^{2n+1} \\
\cos(x) &= \sum_{n=0}^\infty \frac{(-1)^n}{(2n)!}x^{2n}
\end{align}$$

Another, the solutions to the following differential equation, with initial conditions (...)

$$y'' = -y$$

A third, as these integrals.

A related post on [Stack Exchange](https://math.stackexchange.com/questions/1176098/what-are-some-rigorous-definitions-for-sine-and-cosine).