---
layout: post
mathjax: true
title: "Using the Equipartition Theorem on Photons"
categories: misc
---

I've realized that there are very few topics of physics covered on this site, so this post is meant to fix it a little bit.
Let's do a thermodynamics problem today then.
So let's start with some discussion of the equiparition theorem: what exactly is it and why should you really care?
After all, equipartition is a pretty big word and you would have probably tuned out by now if a professor was lecturing about this.
This is important some problems, like the one we will solve today!
Let's get started, shall we?

## Problem

The energy of a photon is $E=pc$.
Treating the photon as a classical object, compute the average energy of a photon at temperature $T$.
In addition, find $\gamma$ for a 3D photon gas.

## Solution

We start by using the title of this post to help us out a lot.
Using the Pythagorean theorem because we need to work in 3 dimensions,

$$
E = c \sqrt{p_x^2 + p_y^2 + p_z^2}
$$

Next, using the equipartition theorem, we can find the following expressions.

$$
k_B T = \left \langle p_x \frac{\partial E}{\partial x} \right \rangle = c \left \langle \frac{p_x^2}{\sqrt{p_x^2 + p_y^2 + p_z^2}} \right \rangle
$$

$$
k_B T = \left \langle p_y \frac{\partial E}{\partial x} \right \rangle = c \left \langle \frac{p_y^2}{\sqrt{p_x^2 + p_y^2 + p_z^2}} \right \rangle
$$

$$
k_B T = \left \langle p_z \frac{\partial E}{\partial x} \right \rangle = c \left \langle \frac{p_z^2}{\sqrt{p_x^2 + p_y^2 + p_z^2}} \right \rangle
$$

Using linearity after adding all three equations up, we have

$$
3k_B T = c \left \langle \frac{p_x^2+p_y^2+p_z^2}{\sqrt{p_x^2+p_y^2+p_z^2}} \right \rangle = c \left \langle \sqrt{p_x^2 + p_y^2 + p_z^2} \right \rangle
$$

This is a big yayyyyy because we recognize the expression on the far right: the energy of a photon.
Therefore,

$$
\boxed{\left \langle E \right \rangle = 3 k_B T}
$$

Finally, we can use this to finish off the problem
