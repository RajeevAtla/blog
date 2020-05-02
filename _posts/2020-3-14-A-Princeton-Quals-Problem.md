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
Its a well-known fact that when this occurs, this quantity is constant:


$$
\mathcal{L} - y'(x) \frac{\partial \mathcal{L}}{\partial y'(x)} = C
$$


### Part 3
Let the constant be $a$.
Substituting the Lagrangian we've already found into this equation, we see that it saves us some time compared to the Euler-Lagrange equation.
Evaluating and simplifying, we see that


$$
\left ( \frac{y'(x)}{a} \right ) - (y(x))^2 = 1
$$


We recognize the similiarity with the hyperbolic trigonometric functions $\sinh{(x)}$ and $\cosh{(x)}$ due to them being derivatives of each other and the identity $\sinh^2 {x} - \cosh^2 {x} = 1$.
We guess a solution in the form of $y(x) = a \cosh{bx}$.
This works as long as $a = \frac{1}{b}$.

We first consider our symmetry constraint. 
Since a hyperbolic cosine is an even function $y(w) = y(-w)$.

Finally, we must consider our length constraint.
Evaluating the length integral


$$2L = 2a \sinh{\left (\frac{w}{a} \right)}$$


This is a transcendental equation that $a$, $L$, and $w$ must satisfy.

## Aftermath
This was a fun problem!!!

The curve we just solved for is called a (catenary)[https://en.wikipedia.org/wiki/Catenary].
Also, using hyperbolic trig functions are a common thing in physics, especially in special relativity.
