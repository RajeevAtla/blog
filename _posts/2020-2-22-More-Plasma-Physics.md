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

## 2.2 $E=0$
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

We now add in an electric field with $E_y = 0$, so $\boldsymbol{E} = E_x \boldsymbol{\hat{x}} + E_z \boldsymbol{\hat{z}}$.
We start with the $\boldsymbol{\hat{z}}$-direction.
The equation of motion in this direction is


$$
\frac{dv_z}{dt} = \frac{qE_z}{m} \Rightarrow v_z = \frac{qE_z}{m} t + v_{0_{z}} \Rightarrow z-z_0 = \frac{qE_z}{2m} t^2 + v_{0_{z}} t
$$


This means that in the $\boldsymbol{\hat{z}}$-direction, there is simply an acceleration along $\boldsymbol{B}$.

#### Transverse Components
We now consider the transverse components: the $\boldsymbol{\hat{x}}$- and $\boldsymbol{\hat{y}}$-directions.


$$
\dot{v}_x = \frac{q}{m} E_x + \omega_c v_y
$$


$$
\dot{v}_y = - \omega_c v_x
$$


Differentiating, after assuming a constant $\boldsymbol{E}$, we have, after a little manipulation and simplification,


$$
\ddot{v}_x = - \omega_c^2 v_x
$$


$$
\ddot{v_y} = - \omega_c^2 \left (\frac{E_x}{B} + v_y \right)
$$


We see that both the motion in both directions exhibits simple harmonic motion, so we can solve this to find


$$
v_x = v_{\perp} e^{i \omega_c t}
$$


$$
v_y = i v_{\perp} e^{i \omega_c t} - \frac{E_x}{B}
$$


We can define the guiding center drift to be $v_{gc} = \frac{E_x}{B}$, so we recover the Larmor motion we found before, albeit superimposed with a guiding center drift in the $- \boldsymbol{\hat{y}}$-direction.

#### General Drift
We consider the general drift, for arbitrary $\boldsymbol{E}$ and $\boldsymbol{B}$.
We consider the homogenous part of the Lorentz force equation, so we can omit the $m \boldsymbol{\dot{v}}$ term, because it simply is the Larmor rotation.


$$
\boldsymbol{E} + \boldsymbol{v} \times \boldsymbol{B} = 0 \Rightarrow \boldsymbol{E} \times \boldsymbol{B} = \boldsymbol{B} \times \left (\boldsymbol{v} \times \boldsymbol{B} \right) = \boldsymbol{v} B^2 - \boldsymbol{B} \left ( \boldsymbol{v} \cdot \boldsymbol{B} \right)
$$


Taking the transverse components, we can see that the electric field drift is


$$\boldsymbol{v}_E = \frac{\boldsymbol{E} \times \boldsymbol{B} }{B^2}$$


The magnitude is


$$
v_E = \frac{E}{B}
$$

### 2.2.3 Gravitational Field
Sometimes, we need to consider non-electric forces when analyzing a particle.
We make the substitution $q \boldsymbol{E} \to \boldsymbol{F}$, so the guiding center drift is then given by


$$
\boldsymbol{v}_f = \frac{\boldsymbol{F} \times \boldsymbol{B} }{qB^2}
$$


If $\boldsymbol{F}$ is the force of gravity, then


$$
\boldsymbol{v}_g = \frac{m \boldsymbol{v} \times \boldsymbol{B} }{qB^2}
$$


There is a subtle difference here from the normal $\boldsymbol{v}_E$, namely that the sign of the charge does indeed matter.
This means that ions and electrons will drift in opposite directions, giving a net current density in the plasma of


$$
\boldsymbol{j} = n(M +m) \frac{\boldsymbol{g} \times \boldsymbol{B} }{B^2}
$$


## 2.3 Nonuniform $\boldsymbol{B}$ Field

We now consider inhomogeneous fields for $\boldsymbol{E}$ and $\boldsymbol{B}$.

### 2.3.1 $ \nabla \boldsymbol{B} \perp \boldsymbol{B}$: Grad-B Drift

Consider when the lines of force are straight, but their density increases in the $\boldsymbol{\hat{y}}$-direction.

The gradient in $\boldsymbol{B}$ causes the Larmor radius to vary, becoming larger at the bottom of the orbit than the top.
This should lead to a drift, with opposing directions for ions and electrons, perpendicular to both $\boldsymbol{B}$ and $\del \boldsymbol{B}$.

We now consider the average motions in each direction.
Clearly, $\langle F_x \rangle = 0$, because the particle spends equally as much time moving up and down.
From the work we've done above, we see that


$$
F_y = -q v_x B_z(y) \approx -qv_{\perp} B_0 \cos{(\omega_c t)} \pm q v_{\perp} r_L \cos^2 {\omega_c t} \frac{\partial B}{\partial y} 
$$


We have used a Taylor expansion of $B_z \approx B_0 + y \frac{\partial B_z}{\partial y}$.
To be valid, this approximation requires $r/L \ll 1$, where $L \sim \frac{\partial B_z}{\partial y}$.

We see that the first term averages to $0$ and the $\cos^2$ averages to $\frac{1}{2}$, so


$$
\langle F_y \rangle = \pm \frac{q v_{\perp} r_L }{2} \frac{\partial B}{\partial y}
$$


The guiding center's drift velocity is then

$$
\boldsymbol{v}_{gc} = \pm \frac{v_{\perp} r_L }{2 B} \frac{\partial B}{\partial y} \boldsymbol{\hat{x}}
$$


Since the choice of coordinates is arbitrary, we can generalize to find the grad-B drift.


$$
v_{\nabla \boldsymbol{B}} = \pm \frac{v_\perp r_L}{2} \frac{\boldsymbol{B} \times \nabla \boldsymbol{B} }{B^2}
$$


Up to the $1/2$ factor, we could have derived this with dimensional analysis.
Note that this is in opposing directions for ions and electrons and causes a current transverse to $\boldsymbol{B}$.

### 2.3.2 Curved B: Curvature Drift
Now we consider the case when the lines of force are curved with a constant radius of curvature $R_c$, with $B$ a constant.
Recall from electrodynamics that such a magnetic field doesn't obey Maxwell's equations, so in practice, we will always also have a grad-B drift superimposed to the curvature drift.

The average centrifugal force is


$$
\boldsymbol{F}_{cf} = \frac{m v_{\parallel}^2 \boldsymbol{R}_c }{R_c}
$$


We have used $v_{\parallel}^2$ to denote the average square of the velocity along $\boldsymbol{B}$.

The curvature drift $\boldsymbol{v}_R$ is then


$$
\boldsymbol{v}_{R} = \frac{m v_{\parallel}^2 }{qB^2} \frac{\boldsymbol{R}_c \times \boldsymbol{B} }{R_c^2}
$$

#### Accompanying Grad-B drift

