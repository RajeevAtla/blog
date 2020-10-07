---
layout: post
mathjax: true
title: "Earnshaw's Theorem"
categories: misc
---

So it's come to my attention that my blog doesn't really have that many EM problems on it, so I decided to prove Earnshaw's theorem.
But what really is Earnshaw's Theorem and why should you care? That's what we talk about in this blog post.

## Earnshaw's Theorem: The Statement

Earnshaw's Theorem states that a system of charges cannot cause a charge to be in stable equilibrium.

## Earnshaw's Theorem: The Proof

You can look at any decent electrodynamics book for a formal proof, but that's not why we're here. (･.◤)
The purpose of this blog is to make less people hate physics, and I can tell from experience that a formal proof does the opposite (•_•) ( •_•)>⌐■-■ (⌐■_■).

So here we go:
Suppose we have a system of charges $q_i$ located at positions $r_i$.
For argument's sake, let's say we can fix these charges, so we don't need to consider the fact that their positions might change later on.

Let's place a charge $Q$ at position $R = \langle 0, \dots 0 \rangle$.
Now let's consider the forces upon this charge.

$$
\sum F = \sum \frac{q_i Q}{4 \pi \epsilon_0 r_i^2} = Q \sum \frac{q_i}{4 \pi \epsilon_0 r_i^2} = QE
$$

Not unsurprisingly, we can see that the net force is equal to the product of the test charge and the electric field produced by the system of charges.
We use this fact to finish the problem.

Suppose we choose $Q$ to be in equilbrium, so that the force at the origin is $0$.｡゜(｀Д´)゜｡
To see that this equilibrium is unstable, perturb $Q$ slightly to $\vec{\epsilon} = \langle \epsilon, 0, \dots 0 \rangle$, where $\epsilon \ll r_i$.

We next use a multivariate Taylor expansion to approximate the net force at this point:
$$
\sum F = Q \sum \frac{q_i}{4 \pi \epsilon_0 (\vec{r}_i - \vec{\epsilon}\,)^2} \approx \frac{Q}{4 \pi \epsilon_0} \sum \frac{q_i}{r_i^2} \left (1 + 2   \frac{\epsilon}{r_i} + O \left( \left ( \frac{\epsilon}{r_i} \right)^3 \right) \right)
$$

Observe that no matter the magnitude or sign of $q_i$ or $r_i$, we end up with a force that is positive in nature.
The approximation is valid here because for $\epsilon \ll r_i$, Lagrange's error bound guarantees that
$$
O \left( \left ( \frac{\epsilon}{r_i} \right)^3 \right) < 2 \frac{\epsilon}{r_i}
$$

This effectively finishes the proof because in order for the equilibrium to be stable, the force must be a restoring one in nature, meaning that is must be negative locally at $\vec{\epsilon}$.
However, we have proved that this is not possible.

And that was just one example of how powerful Taylor expansions are in math. (ʘᗩʘ')
Although they are the bane of some calculus students' existence, ಠ_ಥ they are trully useful, and really helped a lot while proving Earnshaw's Theorem.
Peace out! (｡◕‿◕｡)
