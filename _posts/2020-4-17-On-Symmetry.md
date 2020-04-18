---
layout: post
mathjax: true
title: "The True Value of Symmetry"
categories: misc
---

Apparently symmetry really helps in physics problems. I was too close-minded to realize this lol.
Sometimes it stares at you like ( ͡°( ͡° ͜ʖ( ͡° ͜ʖ ͡°)ʖ ͡°) ͡°), and sometimes its more discreet like ┬┴┬┴┤(･_├┬┴┬┴.
Sometimes, its more dependent on your own training materials.
For example, consider this problem:

(I used MathJax to make the $ \LaTeX $)

## Problem Statement:
A point charge of $q$ is placed a distance $ \frac{1}{2} a $ above the geometrical center of a square of charge of uniform surface charge density $\sigma $ and side length $ a $. Find the force on the point charge by the square.

## My Original Solution:
I encountered this problem after a bunch of problems that just used integration as their primary method of solution.
That's my one and only excuse for not seeing the symmetry trick immediately.
We begin by assigning coordinates across the square.
Let the center of the square lie at the origin and let the square lie in the $ xy $ -plane.
Consider an area element $dA = dx \, dy$ located at $(x,y,0)$.
The total charge on this element, since the surface charge density is uniform, is $ \sigma \, dx \, dy$.
The distance from this element to the point charge is $ \sqrt{x^2 + y^2 + \left ( \frac{a}{2} \right)^2 }$.
By Couloumb's Law, the force on the point charge due to this area element is

$$ dF = \frac{\sigma q}{4 \pi \epsilon_0} \frac{dx \, dy}{x^2 + y^2 + \left ( \frac{a}{2} \right)^2} $$

However, we can't just integrate this, but have to account for directions. We can see that the forces proportional to $ \bm{\hat{x}}$ and $\bm{ \hat{y}}$ both vanish, leaving only the force in the $\hat{\bm{z}}$ direction.


## The Solution I Found 2 Minutes Later :')
