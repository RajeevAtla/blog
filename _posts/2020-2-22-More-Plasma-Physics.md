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
This should lead to a drift, with opposing directions for ions and electrons, perpendicular to both $\boldsymbol{B}$ and $ \nabla \boldsymbol{B}$.

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
We must take into account the decrease of $B$ with raidus.
In a vacuum, we have $\nabla \times \boldsymbol{B} = 0$, by Gauss's law of magnetism.
In cylindrical coordinates, $\nabla \times \boldsymbol{B}$ has only a $\boldsymbol{\hat{z}} $-component, since $\boldsymbol{B}$ has only a $\boldsymbol{\hat{\theta}}$-component and $\nabla B$ has only an $\boldsymbol{\hat{r}}$-component.
We then have the differnential equation


$$
\frac{1}{r} \frac{\partial}{\partial r} \left (r B_{\theta} \right) = 0 \Rightarrow B_{\theta} \propto \frac{1}{r}
$$


Therefore,

$$
B \propto \frac{1}{R_c} \Rightarrow \frac{\nabla B}{B} = - \frac{\boldsymbol{R}_c }{R_c^2}
$$

Evaluating the cross product to find the drift, we see that

$$
v_{\nabla B} = \frac{m v_{\perp}^2 }{2q} \frac{\boldsymbol{R}_c \times \boldsymbol{B} }{R_c^2 B^2}
$$


Adding up the contributions from each drift,


$$
\boldsymbol{v}_R + \boldsymbol{v}_{\nabla B} = \frac{m \boldsymbol{R}_c \times \boldsymbol{B} }{q R_c^2 B^2} \left (\frac{1}{2} v_{\perp}^2 + v_{\parallel}^2 \right)
$$


Because the drifts add, this means that its impossible to confine a plasma into a torus, as it will always drift out, no matter how the temperature and magnetic field vary.

Applying a Maxwellian distribution on $\langle v_{\parallel}^2 \rangle$ and $\langle \frac{1}{2} v_{\perp}^2 \rangle$, we see that each becomes $\frac{KT}{m}$, so


$$
\langle \boldsymbol{v}_{R + \nabla B} \rangle = \frac{r_L}{R_c} v_{th} \boldsymbol{\hat{y}}
$$


### $\nabla \boldsymbol{B} \parallel \boldsymbol{B} $: Magnetic Mirrors

Now we consider a magnetic field which is pointed in the $z$-direction and whose magnitude varies in the $z$-direction.
Let the field be symmetric about the axis, so $B_{\theta} = 0$ and $\frac{\partial }{\partial \theta} = 0$.
Since the magnetic field lines converge and diverge, there is definitely a component in the radial direction: $B_r$.
We now show that this component generates a force that can trap a particle in a magnetic field.

From $\nabla \cdot \boldsymbol{B} = 0$, $\frac{1}{r} \frac{\partial}{\partial r} \left (r B_r \right) + \frac{\partial B_z}{\partial z} = 0$.
Assuming that $\frac{\partial B_z}{\partial z}$ exists at $r=0$ and $\frac{\partial^2 B_z}{\partial r \, \partial z} \approx 0$, we have


$$
r B_r = - \int \limits_{0}^{r} r' \frac{\partial B_z}{\partial z} \, dr' \approx \frac{1}{2} r^2 \frac{\partial B_z}{\partial z} \bigg \vert_{r = 0} \Rightarrow B_r = - \frac{r}{2} \frac{\partial B_z}{\partial z} \bigg \vert_{r = 0}
$$

Evaulating the Lorentz force and ignoring all inhomogenous terms, we see that the only force of interest is


$$
F_z = \frac{1}{2} q v_{\theta} r \frac{\partial B_z}{\partial z}
$$


Taking the average over one complete gyration,


$$
\langle F_z \rangle = - \frac{1}{2} \frac{m v_{\perp}^2 }{B} \frac{\partial B_z}{\partial z}
$$


We define the magnetic moment of a gyrating particle to be $\mu \equiv \frac{mv_{\perp}^2 }{2B}$, so


$$
\langle F_z \rangle = - \mu \frac{\partial B_z}{\partial z}
$$


We can generalize this to the general force on a diamagnetic particle, which we write as


$$
\boldsymbol{F}_{\parallel} = - \mu \nabla_{\parallel} B
$$


Note that the magnetic moment is also $\mu = IA$, for a current loop.

We now show that $\mu$ remains invariant across changing $\boldsymbol{B}$.
We first consider the component of the equation along $\boldsymbol{B}$ and multiply both sides by $\frac{ds}{dt} = v_{\parallel}$.


$$
m \frac{d v_{\parallel}}{dt} = - \mu \frac{\partial B}{\partial s} \Rightarrow m v_{\parallel} \frac{d v_{\parallel} }{dt} = \frac{d}{dt} \left (\frac{1}{2} mv_{\parallel}^2 \right) = - \mu \frac{dB}{dt}
$$


Energy must be conserved, so


$$
\frac{d}{dt} \left (\frac{1}{2} m v_{\parallel}^2 + \frac{1}{2} m v_{\perp}^2 \right) = \frac{d}{dt} \left (\frac{1}{2} m v_{\parallel}^2 + \mu B \right) = 0
$$


With the condition we found above, we can substitute to find that $\frac{d \mu}{dt} = 0$, as desired.

#### Magnetic Mirror
$\mu$-invariance is the basis of one of the primary schemes of plasma confinement - the magnetic mirror.
As a particle moves from a weak $B$ to a strong $B$, $v_{\perp}$ must increase in order to keep $\mu$ a constant.
However, since energy must be conserved, $v_{\parallel}$ must then decrease, as the magnetic force does no work.

This type of confinement isn't perfect, as a particle with $v_{\perp}$ will have $\mu = 0$ and will be free to escape.
We now further discuss the conditions required for a particle to escape.
A particle with $v_{\parallel} = v_{\parallel_{0}}$ and $v_{\perp} = v_{\perp_{0}}$ at the midplane between the two fields will have $v_{\perp} = v_{\perp} '$ and $v_{\parallel} = 0$ at the turning point.
Let the two respective fields be $B_0$ and $B'$.
Using $\mu$-invariance,


$$
\frac{v_{\perp_{0}}^2 }{B_0} = \frac{v_{\perp_{0}}}{B'}
$$


Combining this with energy conservation, we see that


$$
\frac{B_0}{B'} = \frac{v_{\perp_{0}}^2 }{v_0^2} \equiv \sin^2 \theta
$$


Here, $\theta$ is the pitch angle of the orbit in the weak-field region.
Particles with smaller $\theta$ will mirror in regions of higher $B$.
However, if $\theta$ is too small, then $B' > B_m$ and the particle doesn't mirror at all.

We see that the mirror ratio is


$$
\sin^2 \theta_m = \frac{B_0}{B_m} \equiv \frac{1}{R_m}
$$


This means that the non-mirror region is a cone, called a loss cone.
If a particle is in the loss cone, then it is not affected.

Note that the loss cone is independent of $q$ and $m$.
If no collisions occur, then both ions and electrons are sufficiently confined.
However, if they do occur, then particles can change their pitch angles and be scattered into the loss cone.
Electrons are usually lost more frequently because they are smaller and therefore have a higher collision frequency.

The magnetic mirror was first proposed by Enrico Fermi as a mechanism to accelerate cosmic rays.

## 2.4: Nonuniform $E$ Field
Now let the magnetic field be uniform and the electric field be nonuniform.
For simplicity, let $\boldsymbol{E}$ point in the $\boldsymbol{\hat{x}}$-direction and vary such that


$$
\boldsymbol{E} = E_0 \cos{kx} \, \boldsymbol{\hat{x}}
$$


This means that the equations of motion are 


$$
\dot{v}_x = \frac{qB}{m} v_y + \frac{q}{m} E_x (x)
$$


$$
\dot{v}_y = - \frac{qB}{m} v_x
$$


Putting the two equations together,


$$
\ddot{v}_x = - \omega_c^2 v_x \pm \frac{\omega_c \dot{E}_x }{B}
$$


$$
\ddot{v}_y = - \omega_c^2 v_y - \frac{\omega_c^2 E }{B}
$$


If the electric field is weak, then we can treat the orbit as undisturbed and try to "extrapolate" from there (you'll see how later).
We know that $x \equiv x_0 + r_L \sin{\omega t}$, so we can substitute this into the equation of motion above.
Moreover, since we need to find a speed $v_E$, we take the average motion, so all terms involving a sine or cosine are gone.
Therefore, $\langle v_x \rangle = 0$.
Taking the Larmor radius as small, or $kr_L \ll 1$, we can Taylor approximate (specifically, a Maclaurin series) around 0 to find that


$$
\langle v_y \rangle = - \frac{E_0}{B} \cos{kx_0} \left (1 - \frac{1}{4} k^2 r_L^2 \right)
$$


The usual $\boldsymbol{E} \times \boldsymbol{B}$ drift adds, and using linearity, we can say


$$
\boldsymbol{v}_E = \frac{\boldsymbol{E} \times \boldsymbol{B} }{B^2} \left (1 - \frac{1}{4} k^2 r_L^2 \right)
$$


Moreover, we can further correct this drift velocity by accounting for the (multi-dimensional) second derivative.
We do this by substituting $ik$ with $\nabla$.
Therefore,

$$
\boldsymbol{v}_E = \left (1 + \frac{1}{4} r_L^2 \nabla^2 \right) \frac{\boldsymbol{E} \times \boldsymbol{B}}{B^2}
$$


This is called the finite-Larmor-radius effect.

Since $r_L$ is much larger for electrons that for protons, the drift velocity is now dependent on species.
If a density clump occcurs within a plasma, the electric field can cause the different species to separate, resulting in the production of more electric fields.
If there is a feedback mechanism capable to self-enhancing itself through this effect, the plasma is not stable.
This instability is called a drift instability, which will be discussed later.
The grad-B drift is therefore a finite-Larmor-radius effect and also causes charges to separate.

However, the grad-B drift is proportional to $kr_L$, whereas this drift is proportional to $k^2 r_L^2$.
This means that this effect is only important at relatively large $k$.
For this reason, drift instabilities belong to another class of instabilites called microinstabilites.

## 2.5: Time-Varying $E$ Field
Let $\boldsymbol{E}$ point parallel to the x-axis.
We first consider the case when it varies sinusoidally in time.


$$
E(t)= E_0 e^{i \omega t}
$$


Since $\dot{E} = i \omega E$, we write the equation of motion as


$$
\ddot{v}_x = - \omega_c^2 \left (v_x \mp i \frac{\omega \~{E}}{\omega_c B} \right)
$$


Let $\~{v}_P \equiv \pm i\frac{\omega \~{E}_x}{\omega_c B}$ and $\~{v}_E = \frac{\~{E}_x}{B}$.
Therefore,


$$
\ddot{v}_x = - \omega_c^2 \left (v_x - \~{v}_p \right)
$$


$$
\ddot{v}_y = - \omega_c^2 \left (v_y - \~{v}_E \right)
$$


We can easily solve this to find that


$$
v_x = v_{\perp} e^{i \omega_c t} + \~{v}_p
$$


$$
v_y = \pm i v_{\perp} e^{i \omega_c t} + \~{v}_E
$$

We also see that the equations of motion aren't satisfied unless $\omega^2 \ll \omega_c^2$.
Making the approximation that $\boldsymbol{E}$ varies slowly, this condition holds, so this is the solution.

### Polarization Effects
We know that the guiding center motion due to a time-varying electric field.
Generalizing to arbitrary electric fields, we see that there is a new drift along the direction of $\boldsymbol{E}$, called the polarization drift.
We find it by replacing $i \omega$ with $\frac{\partial}{\partial t}$, so we can generalize the equation into


$$
\boldsymbol{v}_p = \pm \frac{1}{\omega_c B} \frac{d \boldsymbol{E}}{dt}
$$


Since this is in opposing directions depending on the species of the particle, this particular drift also has an associated polarization.
