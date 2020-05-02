---
layout: post
mathjax: true
title: "Princeton Makes Good Problems"
categories: misc
---

First of all, happy Pi Day!!! 
Time to get to the physics.
I found this Princeton problem looking at old quals for fun.

It turned out to be really interesting, so here we are.

## Princeton Physics Preliminary Exams J98M.1 - Hanging Rope
Problem found [here](https://phy.princeton.edu/sites/physics/files/graduate-program/prelims/J98.pdf).

## Problem Statement
A piece of thin uniform unstretchable rope has length $2L$ and mass $M$.
Its ends are attached to points at the same height separated by distance $2 w$ and the rope hangs between them under the influence of gravity (of course $w < L$).
Let us set up coordinates $(x,y)$ in the plane of the rope, so that the end points have equal values of $y$ and $x = \pm w$.
You will be asked to determine the vertical coordinate of the rope, $y$, as a function of $x$.

1. Write down the functional of $y(x)$ that has to be minimized. What is the form of the constraint?
2. One may think of the functional to be minimized as the action as an for a 1-dimensional particle with coordinate $y$ and time $x$. Find a conserved quantity.
3. For a given value of the conserved quantity, find $y(x)$. What is the equation relating the conserved quantity to $w$ and $L$?

## Solution
### Part 1
The potential energy must be minimized.
Letting the reference height be $y=0$, for a small piece of the rope with horizontal projection $dx$ and length 


$$
ds = dx \, \sqrt{1 + \left (\frac{dy(x)}{dx} \right)^2}
$$


Defining the linear mass density of the rope to be $\rho = \frac{M}{2L}$, the potential energy of this piece is


$$dU = g \, y(x) \, dm = \rho g \, y(x) \sqrt{1 + \left (\frac{dy(x)}{dx} \right)^2} \, dx$$


The total potential energy is then


$$
U = \rho g \int \limits_{-w}^{w} y(x) \sqrt{1 + \left (\frac{dy}{dx} \right)^2} \, dx
$$


Finally, we have a constraint on the length.
By definition, $y(x)$ must satisfy


$$
2L = \int \limits_{-w}^{w} \sqrt{1 + \left (\frac{dy}{dx} \right)^2} \, dx
$$



### Part 2
In order to minimize the potential energy, we use the Euler-Lagrange equations.
The Lagrangian is then


$$
\mathcal{L} = y(x) \sqrt{1 + y'(x)^2}
$$


Note that the Lagrangian is independent of $x$.

#### Important Lemma
We briefly discuss some important stuff regarding this type of Lagrangian.
Consider a Lagrangian $\mathcal{L}(y(x), y'(x))$ that is independent of $x$.

We start by multiplying both sides of the Euler-Lagrange equation by $y'(x)$.


$$
y'(x) \frac{\partial \mathcal{L}}{\partial y(x)} = y'(x) \frac{d}{dx} \frac{\partial \mathcal{L}}{\partial y'(x)}
$$



### Part 3
We use the Euler-Lagrange equation now, with time coordinate $x$.


$$
\frac{\partial \mathcal{L} }{\partial y(x)} = \frac{d}{dx} \left (\frac{\partial \mathcal{L} }{\partial \left (\frac{dy}{dx} \right)} \right)
$$





