---
layout: post
mathjax: true
title: "Rotating Special Relativity"
categories: misc
comments: true
---

When in the course of doing physics problems (man, I should *really* stop listening to Hamilton), you find yourself at the intersection of what seems to be two different fields.
For example, consider the following problem, at the intersection of special relativity and oribital mechanics.

## Problem

Superman loves playing with his yo-yo.
Model the yo-yo as a particle of mass $m$.
Superman spins it in a circular orbit of radius $r$ and at a angular velocity $\omega$.
Superman, being Superman, can spin the yo-yo at relativistic speeds.
He wants you to find the magnitude of the force he has to exert to spin his yo-yo.

## Solution

We assume that Superman's hand is at the origin in the xy-plane and that the yo-yo spins in the xy-plane only.
The main idea here is to use the standard method of dealing with rotating motion, but using the *proper velocity* instead of simply using the *velocity*.
The proper velocity $\overrightarrow{u}$ is, letting $\tau$ be the proper time and $\overrightarrow{x}$ the 4-position.

$$
\overrightarrow{u} = \frac{d \overrightarrow{x}}{d \tau} =
\begin{pmatrix}
c \frac{dt}{d \tau} \\
\frac{dx}{d \tau} \\
\frac{dy}{d \tau} \\
\frac{dz}{d \tau} \\
\end{pmatrix}
=
\gamma
\begin{pmatrix}
c \\
\overrightarrow{v} \\
\end{pmatrix}
$$

Here $\overrightarrow{v}$ is a 3-vector.
The components of $\overrightarrow{v}$ are easily found, as we can just use basic kinematics and geometry.

$$
\overrightarrow{v}
=
\begin{pmatrix}
\frac{dx}{dt} \\
\frac{dy}{dt} \\
\frac{dz}{dt} \\
\end{pmatrix}
=
\begin{pmatrix}
\frac{d}{dt} \left ( r \sin{\omega t} \right) \\
\frac{d}{dt} \left ( -r \cos{\omega t} \right) \\
\frac{d}{dt} \left ( z_0 \right) \\
\end{pmatrix}
$$

Here, $z_0$ is a constant representative of the height of Superman's hand, so the last component of the vector is zero.
The first two components are fairly easy to evaluate.

$$
\overrightarrow{v}
=
\begin{pmatrix}
\omega r \cos{\omega t} \\
\omega r \sin{\omega t} \\
0 \\
\end{pmatrix}
$$

Therefore, the magnitude of $\overrightarrow{v}$

$$
\left | \overrightarrow{v} \right | = \omega r
$$

This makes sense.
Now we can write the proper velocity.

$$
\overrightarrow{u}
=
\gamma
\begin{pmatrix}
0 \\
\omega r \cos{\omega t} \\
\omega r \sin{\omega t} \\
0 \\
\end{pmatrix}
= \frac{\omega r}{\sqrt{1 - \frac{\omega^2 r^2}{c^2}}}
\begin{pmatrix}
0 \\
\cos{\omega t} \\
\sin{\omega t} \\
0 \\
\end{pmatrix}
$$

Now, we recall that force is the time derivative of the the momentum, so it makes sense for us to find that first.
However, we need the 4-momentum, not the normal momentum.
But that's simple to find, since we have the proper velocity and can simply multiply by mass.

$$
\overrightarrow{P} = \frac{m \omega r}{\sqrt{1 - \frac{\omega^2 r^2}{c^2}}}
\begin{pmatrix}
0 \\
\cos{\omega t} \\
\sin{\omega t} \\
0 \\
\end{pmatrix}
$$

As we recalled earlier, force is the derivative of momentum.
We can simply do this to find

$$
\overrightarrow{f} = \frac{d\overrightarrow{P}}{dt} = \frac{m \omega^2 r}{\sqrt{1 - \frac{\omega^2 r^2}{c^2}}}
\begin{pmatrix}
0 \\
\cos{\omega t} \\
\sin{\omega t} \\
0 \\
\end{pmatrix}
$$

Taking the magnitude,

$$
\boxed{\left| \overrightarrow{f} \right| = \frac{m \omega^2 r}{\sqrt{1 - \frac{\omega^2 r^2}{c^2}}}}
$$
