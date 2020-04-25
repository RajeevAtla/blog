---
layout: post
mathjax: true
title: "More Plasma, More Captain Phasma"
categories: PlasmaPhysics
---
These are my notes for Chapter Two of *Introduction to Plasma Physics and Controlled Fusion* by Francis F. Chen. Its really a great book and its available online, so I would recommend that you check it out!

MLA Citation - Chen, Francis F. *Introduction to Plasma Physics and Controlled Fusion*. 3rd ed., Springer International Publishing Switzerland, 2016, *Springer Link*, [link.springer.com/content/pdf/10.1007%2F978-3-319-22309-4.pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-22309-4.pdf.)

## 2.1 Introduction
A particular difficulty when working with plasma is the intermediate density.

What we mean by this is: consider a normal fluid.
Because its dense enough, the collision forces are much higher than the electromagnetic forces, so the electromagnetic forces can be safely neglected in analysis of the fluid.
Therefore, we can simply use fluid dynamics to describe the fluid, no what the fluid is made up of, charged or uncharged.

On the other hand, on the other extreme of low-density devices, consider an alternating-gradient synchotron. 
Here, only the trajectories of a couple particles need to be calculated, meaning that we can use a more direct approach i.e. a Lagrangian approach (in the sense of Lagrange's view on continuum mechanics, *not* his formulation of classical mechanics).
Specifically, we can track each and every single particle with ease because there are only a few particles.

Now we consider how plasma behaves.
Due to its density being right in the middle of the objects discussed above, it is then intuitive that plasmas behave sometimes like fluids and sometimes like a collection of individual particles.

In order to best understand how plasmas behave, we first consider how a particle behaves in the prescence of electrical and magnetic fields i.e. we are going to start by studying single-particle motions.

##2.2 $E=0$
Consider a charged particle in a region with magnetic field $\boldsymbol{B} = B \boldsymbol{\hat{z}}$.
From definition of the cross product, all motion will happen in the $xy$ plane.
The equations of motion are therefore $\dot{v}_x = \frac{qB}{m} v_y$ and $\dot{v}_y = -\frac{qB}{m}$.
These are coupled differential equations, so we could use normal modes, but that takes lots of time, so instead we use a quick little trick ( ͡°( ͡° ͜ʖ( ͡° ͜ʖ ͡°)ʖ ͡°) ͡°): we take the time derivative of each equation.

That yields $\ddot{v}_x = \frac{qB}{m} \dot{v}_y$.
But $\dot{v}_y = - \frac{qB}{m} v_x$. Therefore,


$$
\ddot{v}_{x} = - \left (\frac{qB}{m} \right)^2 v_x
$$


Similarly,


$$
\ddot{v}_{x} = - \left (\frac{qB}{m} \right)^2 v_x
$$


In the phase space $(v_x, v_y)$, this looks like an ellipse whose dimensions are dependent on initial conditions.
However, we do know that these equations descibe a simple harmonic oscillator.
This oscillator's frequency is known as the **cyclotron frequency**


$$
\omega_c = \frac{|q|B}{m}
$$


We can see that the solution to these equations can be put in the form


$$
v_{i} = v_{\perp} e^{i(\omega_c t + \phi_i)}
$$


Here:
- $v_{\perp}$ is the velocity perpendicular to $\boldsymbol{B}$
- $\phi_i$ is the phase

We can choose the phase so that


$$
v_x = \dot{x} = v_{\perp} e^{i \omega_c t} \Rightarrow x-x_0 = - i \frac{v_{\perp}}{\omega_c} e^{i \omega_c t}
$$


We can use the fact that $v_y = \frac{m}{qB} \dot{v}_x $.
Therefore,


$$
v_y = \frac{m}{qB} \dot{v}_x = \pm \frac{1}{\omega_c} \dot{v}_x = \pm i v_{\perp} e^{i \omega_c t}
$$

Integrating,


$$
y-y_0 = \pm \frac{v_{\perp}}{\omega_c} e^{i \omega_c t}
$$

Taking the real part of each,


$$
x - x_0 = \frac{v_{\perp}}{\omega_c} \sin{\omega_c t}
$$


and


$$
y - y_0 = \pm \frac{v_{\perp}}{\omega_c} \cos{\omega_c t}
$$


We see that the motion of the particle is in a circle.
We call the radius of this circle the **Larmor radius**.


$$
r_{L} = \frac{v_{\perp}}{\omega_c} = \frac{m v_{\perp}}{|q| B}
$$


We call the point $(x_0 , y_0)$ the **guiding center**.
This is the center of the orbit and is fixed, for now (¬‿¬).

### 2.2.2 Finite $E$
