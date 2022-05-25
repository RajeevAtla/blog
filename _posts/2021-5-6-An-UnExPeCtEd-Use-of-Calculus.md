---
layout: post
mathjax: true
title: "uNeXpEcTeD uSeS oF mAtH"
categories: misc
comments: true
---

Suppose we want to find

$$
\sum \limits_{k=0}^{k=\infty} k e^{-13} \frac{13^k}{k!}
$$

Seeing the $13$ in two distinct locations within the summand, 
we define the generating function $F(z)$ as

$$
F(x) = \sum \limits_{k=0}^{\infty} k e^{-x} \frac{x^k}{k!}
$$

We first pull out the $e^{-x}$ factor,

$$
F(x) = e^{-x} \sum \limits_{k=0}^{\infty} \frac{k x^k}{k!}
$$

Looking at the summand now,
we see that it resembles the Maclaurin series for $g(x) = e^x$.
The only problem is that there is an additional factor of $k$.

$$
F(x) = e^{-x } \sum \limits_{k=0}^{\infty} \frac{x^k}{(k-1)!} = x e^{-x} \sum \limits_{k=0}^{\infty} \frac{x^{k-1}}{(k-1)!} = x
$$

This means that

$$
F(13) = \sum \limits_{k=0}^{k=\infty} k e^{-13} \frac{13^k}{k!} = 13
$$

Note that $F(x)$ is basically finding the expected value of a Poisson distribution with Poisson parameter $\lambda = x$.
A well-known fact about the Poisson distribution is that its expected value and variance are both equal to the Poisson parameter $\lambda$.
