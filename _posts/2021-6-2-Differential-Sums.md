---
layout: post
mathjax: true
title: "Differential Sums?!?!?!?!?!"
categories: misc
comments: true
---

We would like to find

$$
\sum \limits_{n=1}^{\infty} \frac{(-1)^{n+1}}{n(n+1)}
$$

We use the generating series

$$
F(z) = \sum \limits_{n=1}^{\infty} \frac{z^{n+1}}{n(n+1)}
$$

We then take two derivatives to remove the $n(n+1)$, 
finding that

$$
F''(z) = \sum \limits_{n=1}^{\infty} z^{n-1} = 1 + z + z^2 \dots
$$

Then, 
using the geometric series formula

$$
F''(z) = \frac{1}{1-z}
$$

We see that $F (0) = 0$ and its well-known that $F(1) = \sum \limits_{n=1}^{\infty} \frac{1}{n(n+1)} = 1$.
Using these boundary conditions, 
we can easily compute two integrals using some pretty standard methods

$$
F(z) = z + (1-z)\ln(1-z)
$$

We then see that

$$
\boxed{F(-1) = 2 \ln (2) - 1}
$$

Notice here how we've turned the computation of a sum into the solution of a differential equation with certain boundary conditions.
We've basically turned a problem from one area of math (series) into another, albeit very closely related, area of math (differential equations).
