---
layout: post
mathjax: true
title: "Another Princeton Problem"
categories: misc
---

Turns out Princeton makes some really, really good problems to do if you like doing physics.
So, just like when your binge-watching a good TV show, I need another one, another one, another one...

In fact... lets write some python code for it

```python
while True:
  s = "another one, "
  print("I need " + s)
```

Don't actually run it - its an infinite loop and might crash your system.

If you do run it, hit CTRL+C if you want it to stop.

## [Problem](https://phy.princeton.edu/sites/physics/files/graduate-program/prelims/PrelimJ08.pdf)
This is Princeton Graduate Prelims J08M.1, entitled "Pendulum on a Sled".

A plane pendulum consists of a bob of mass $m$ suspended by a massless rigid rod of length $\ell$ that is hinged to a sled
of mass $M$.
The sled slides without friction on a horizontal rail.
Gravity acts with the ususal downward acceleration $g$.

1. Taking $x$ and $\theta$ as generalized coordinates, write the Lagrangian for the system.
2. Derive the equations of motion for the system.
3. Find the frequency $\omega$ for *small* oscillations of the bob about the vertical.
4. At time $t=0$ the bob and the sled, which had been previously at rest, are set in motion by a sharp tap delivered to the bob. The tap imparts a horizontal impulse $\Delta P = F \Delta t$ to the bob. Find expressions for the values of $\dot \theta$ and $\dot x$ just after the impulse.

## Part 1
We let $x$ be the horizontal displacement of the sled and let $\theta$ be the angle made with the vertical by the pendulum.
Letting the sled's original location be the origin, the coordinates of the sled are $(x,0)$ and the coordinates of the bob are $(x + \ell \sin{\theta}, -\ell \cos \theta)$.
The total kinetic energy is then


$$
K = \frac{1}{2} (M+m) \dot{x}^2 + m \dot{x} \ell \dot{\theta} \cos{\theta} + \frac{1}{2} m \ell^2 \dot{\theta}^2
$$


Only the bob has any changing potential energy, so up to a constant, the potential energy is


$$
U = -mg \ell \cos{\theta}
$$


The Lagrangian is then


$$
\mathcal{L} = T-U = \frac{1}{2} (M+m) \dot{x}^2 + m \dot{x} \ell \dot{\theta} \cos{\theta} + \frac{1}{2} m \ell^2 \dot{\theta}^2 + mg \ell \cos{\theta}
$$

## Part 2

We use the Euler-Lagrange equations on both $\theta$ and $x$, starting with the former.

