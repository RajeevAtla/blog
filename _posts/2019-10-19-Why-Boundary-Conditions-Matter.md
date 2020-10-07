---
layout: post
mathjax: true
title: "Why Boundary Conditions Matter"
categories: misc
---

In this article, we are going to talk about some boundary conditions. I sound (▀̿Ĺ̯▀̿ ̿) when I'm talking about this lol.
But in reality, I just go like ༼ つ ◕_◕ ༽つ with the physics and hope for something to happen. (~_^)

Anayways, what we are going to think about today is the following: suppose we have a region of uniform volumetric charge density $ \rho$.

## Using the Integral Form of Gauss's Law

Consider a Gaussian sphere of radius $r$.
Let $Q$ be the charge enclosed in this sphere, which has a volume $\frac{4}{3} \pi r^3$.
The definition of volumetric charge density is that $\rho$ is the ratio between the enclosed charge and the volume of the sphere.
That is

$$
\rho = \frac{Q}{\frac{4}{3} \pi r^3} \Rightarrow Q = \frac{4}{3} \pi \rho r^3
$$

Gauss's law states that

$$
\oint E \, dA = \frac{Q}{\epsilon_0}
$$

The surface area of this sphere we are talking about is $A = 4 \pi r^2$, so the area can come out of the integral.
Simplifying a little,

$$
E = \frac{\rho V}{A \epsilon_0} = \frac{\rho }{\epsilon_0} \frac{\frac{4}{3} \pi r^3}{4 \pi r^2} = \frac{\rho r}{3 \epsilon_0}
$$

Alright, this seems pretty legit. But who knows? ¯\(°_o)/¯

## The Differential Form

Aright, so one way to make sure this result is right, let's check this using the differential form of Gauss's Law.
Because its not usually taught in high school (lol I wish it was though), I'm going to give a brief explanation.

The differential form of Gauss's law equates the divergence of the electrical field to the charge density.
The divergence of a vector function is essentially a measure of the quantity of flux that is emitted by the function.
Gauss's law in differential form is

$$
\nabla \cdot E = \frac{\rho}{\epsilon_0}
$$

In Cartesian coordinates, the divergence of an electrical field $E = E_x \hat{x} + E_{y} \hat{y} + E_{z} \hat{z}$ is

$$
\nabla \cdot E = \frac{\partial E_x}{\partial x} + \frac{\partial E_y}{\partial y} + \frac{\partial E_z}{\partial z}
$$

We can easily see that the electrical field can be written as

$$
E = \langle E_x, E_y, E_z \rangle = \frac{\rho}{\epsilon_0} \langle ax, by, cz \rangle
$$

for all $a+b+c = 1$.
This is a whole class of solutions to the problem.

## Ahhhhh what happened $\dots$

Holy cow! ┬──┬ ノ( ゜-゜ノ) We got two different solutions to the same problem.
And we used the same law.
It turns out what happened was a lack of boundary conditions!
Remember that Gauss's law is just a tool to find the electric field surrounding a given charge configuration.
Its important to not plug and chug things blindly.
Specifically, in order for the entirety of electronamgnetism to even work, we need these boundary conditions! (pesky boundary conditions, always getting in the way of the fun...)
Anyways, I've got homework to finish, so that's all for today! ♪~ ᕕ(ᐛ)ᕗ
