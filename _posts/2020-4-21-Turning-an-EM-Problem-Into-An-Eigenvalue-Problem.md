---
layout: post
mathjax: true
title: "A Nice(ish) Eigenvalue Problem"
categories: misc
---

So I cam across a problem when I was doing some EM that I want to share with you today.

## Problem (BAUPC 1997)

Consider a region of space in which there is a magnetic field $\boldsymbol{B} = B \boldsymbol{\hat{z}}$. A particle of charge $q$ and mass $m$ is given an initial velocity $\boldsymbol{v}_0 = v_0 \boldsymbol{\hat{y}}$.
Find the final position of the particle if it is also subject to a damping force $\boldsymbol{F} = - \alpha \boldsymbol{v}$.


## My Solution

First off, a disclaimer: this won't be the most elegant solution. As always, there are multiple ways to do this problem.

Let's start by finding the magnetic force. Denote the velocity vector by $\boldsymbol{v} = v_x \boldsymbol{\hat{x}} + v_y \boldsymbol{\hat{y}} + v_z \boldsymbol{\hat{z}}$. Magnetic force is given by $\boldsymbol{F} = q \boldsymbol{v} \times \boldsymbol{B}$.
Evaulating the cross products, or using the right hand rule, we can see that the force in the $\boldsymbol{\hat{z}}$-direction vanishes.
Therefore, we only need to consider the x and y-directions in order to use Newton's Second Law. We can't use conservation of energy here because both the magnetic force is perpendicular to the velocity, resulting in 0 work being done by it. Moreover, both forces are nonconservative.

Using Newton's Second Law in the x-direction,


$$
\dot{v_x} = \frac{qB}{m} v_y - \frac{\alpha}{m} v_x
$$


and in the y-direction,


$$
\dot{v_y} = - \frac{qB}{m} v_x - \frac{\alpha}{m} v_y
$$

This is a system of differential equations, so we use the method of normal modes, arising from linear algebra. We start by guessing a solution in the form of $ \boldsymbol{v} = \begin{pmatrix} A \\ B \\ \end{pmatrix} e^{\lambda t}$. 
