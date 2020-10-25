---
layout: post
mathjax: true
title: "Another, Another One"
categories: misc
---

Let's keep our pattern of posting Princeton's Graduate Qualifier exams.
Today, we'll do [J09M.1](https://phy.princeton.edu/sites/physics/files/graduate-program/prelims/PrelimJ09.pdf), which is entitled "Coupled Pendula" because its literally solving the system where two pendula are coupled together with a spring at their midpoints.

## Solution

Since this problem has two degrees of freedom: $\theta_1$ and $\theta_2$, we are compelled to use Lagrangian mechanics because a Newtonian analysis would be very time and space intensive.
We start by finding the potential energy.
Let $U_1$ and $U_2$ be the potential energy for each pendulum and let $U_{12}$ be the potential energy of the spring.
It's easy to see that

$$
U_i = mg \ell \left (1 - \cos{\theta_i} \right) \approx \frac{1}{2} mg \ell \theta_i^2
$$

To find the energy of the spring, we must first find the length of the spring when it is stretched.
Let $d$ be the distance between the vertices of each pendulum.
Using some right-angle trigonometry, we can easily see that the length of the spring is

$$
\sqrt{\left (d + \frac{\ell}{2} \left (\sin{\theta_2} - \sin{\theta_1} \right) \right)^2 + \left (\frac{\ell}{2} \left (\cos{\theta_2} - \cos{\theta_1} \right) \right)}
$$

Using the first order expansions for sine and cosine, since $\theta_i$ are assumed to be small, the length is approximately

$$
d + \frac{\ell}{2} \left(\theta_2 - \theta_1 \right)
$$

We don't really care about $d$, since we want to find the *excess* length of the spring, i.e. we can subtract away the $d$ to find

$$
\frac{\ell}{2} \left (\theta_2 - \theta_1 \right)
$$

We can now see that

$$
U_{12} = \frac{1}{2} k \left (\frac{\ell}{2} \left (\theta_1 - \theta_2 \right) \right)^2 = \frac{1}{8} k \ell^2 \left (\theta_1 - \theta_2 \right)^2
$$

Finally, the total potential energy is

$$
U = \left (\frac{1}{2} mg \ell + \frac{1}{8} k \ell^2 \right) \left (\theta_1^2 + \theta_2^2 \right) - \frac{1}{4} k \ell^2 \theta_1 \theta_2
$$

Next, we need to find the kinetic energy.
A well known fact for a pendulum is that $K_i = \frac{1}{2} m \ell^2 \dot{\theta}_i^2$.
Therefore,

$$
K = \frac{1}{2} m \ell^2 \left (\dot{\theta}_1^2 + \dot{\theta}_2^2 \right)
$$

Finally, the Lagrangian is
$$
\mathcal{L} = \frac{1}{2} m \ell^2 \left (\dot{\theta}_1^2 + \dot{\theta}_2^2 \right) - \left (\frac{1}{2} mg \ell + \frac{1}{8} k \ell^2 \right) \left (\theta_1^2 + \theta_2^2 \right) + \frac{1}{4} k \ell^2 \theta_1 \theta_2
$$

Whooo! That's long!
Next, we use the Euler-Lagrange equations.
Since there aren't any nonconservative forces acting on the system, there are no constraint forces, so the Euler-Lagrange equations are simply

$$
\frac{\partial \mathcal{L}}{\partial{\theta_i}} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{\theta_i}}
$$

Evaulating for $i = 1, 2$, we have the following matrix equation

$$
\begin{pmatrix}
\ddot{\theta_1}
\ddot{\theta_2}
\end{pmatrix}
=
\begin{pmatrix}
- \left ( \frac{g}{\ell} + \frac{k}{4m} \right) & \frac{k}{4m} \\
\frac{k}{4m} & - \left ( \frac{g}{\ell} + \frac{k}{4m} \right) \\
\end{pmatrix}
\begin{pmatrix}
\theta_1 \\
\theta_2 \\
\end{pmatrix}
$$

Congratulations! We've successfully turned this problem into an eigenvalue problem.
This means that we can finish this problem off using some help from linear algebra.
We can find the eigenfrequencies of the middle matrix using a determinant, and can find

$$
\omega_1 = - \frac{g}{\ell} - \frac{k}{2m}
$$

$$
\omega_2 = - \frac{g}{\ell}
$$

Intuitively, we can see that $\omega_1$ corresponds to the pendula oscillating in directions opposite to each other.
Similarly, $\omega_2$ corresponds to the pendula oscillating with each other, cancelling out the effect of the spring because its length doesn't change.
We can therefore write the corresponding eigenvectors of the matrix as

$$
\nu_1 =
\begin{pmatrix}
1
-1
\end{pmatrix}
$$

$$
\nu_2 =
\begin{pmatrix}
1
1
\end{pmatrix}
$$

Finally, we can put together an expression for $\theta_i$ using the constants $A$ and $B$.

$$
\begin{pmatrix}
\theta_1 (t) \\
\theta_2 (t) \\
\end{pmatrix}
= A
\begin{pmatrix}
1 \\
-1 \\
\end{pmatrix}
e^{-i \left (\frac{g}{\ell} + \frac{k}{2m} \right)t}
+ B
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
e^{-i \frac{g}{\ell} t}
$$

Finally, we are given the initial conditions $\theta_1 (t) = 0$, $\theta_2 (t) = \theta_0 $, and $\dot{\theta}_1 = \dot{\theta}_2 = 0$.
Substituting and solving for $A$ and $B$, we find that

$$
A = -B = \frac{1}{2} \theta_0
$$

Substituting back into the original equation,

$$
\begin{pmatrix}
\theta_1 (t) \\
\theta_2 (t) \\
\end{pmatrix}
= \frac{1}{2} \theta_0
\begin{pmatrix}
1 \\
-1 \\
\end{pmatrix}
e^{-i \left (\frac{g}{\ell} + \frac{k}{2m} \right)t}
- \frac{1}{2} \theta_0
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
e^{-i \frac{g}{\ell} t}
$$

And we are done!
