---
layout: post
mathjax: true
title: "Damped, Driven Oscillator"
categories: misc
comments: true
---

Alright, so we've all seen what a simple harmonic oscillator is and how to solve its equation (I hope). So let's move into more spicy territory, shall we?

If you like looking at blocks on a spring (maybe you're attracted to it, who knows?) you know that the amplitude of the oscillations decreases slowly over time. This is due to a lot of different things. It could be friction, it could be drag (if you say wind resistance I will (ง'̀-'́)ง ok?), it could be your friend Throckmorton thats blowing on the block (bad Throckmorton, bad!)

Regardless of the cause, experimental studies show that the force is proportional to the velocity of the block. We let the constant of proportionality be $b$, so

$F = -bv$

We could stop here and start to analyze the system, but for the sake of spiciness, we move on to something more.
Remember your old friend Throckmorton?
Well yeah, for the sake of being annoying, he's screwing with your experiment and moving the place the spring is rooted in.
But he is still your friend, so instead of moving it around in a random way, he moves the support exactly sinusoidally, and avoids having you look up integrals (very fun, but an acquired taste).
Here, Throckmorton also helps out your grades in your physics class by making you learn some new physics, so be semi-appreciative of him, but only sometimes! ༼ つ ͡° ͜ʖ ͡°༽つ

Anyway, let the amplitude of the oscillations of the force he applies be $F_0$. To make the mathematics easier, we write the force he exerts as a complex exponential:

$$
F(t) = F_0 e^{i \omega t}
$$

But the astute mathematician in you will realize that there is an imaginary part, but we'll take care of that later, so don't worry about it for now.
And there is still the spring, so the final force is $F=-kx$.
Using F=ma, we can write the equation of motion as

$$
ma + bv + kx = F_0 e^{i \omega t}
$$

To make things a little easier on us, we use dot notation (Newton, if you remember from calculus class, invented this). Recall that $v = \dot{x}$ and $a = \ddot{x}$, so

$$
m \ddot{x} + b \dot{x} + kx = F_0 e^{i \omega t}
$$

Ok, so we got a differential equation, but have no idea how to solve it. Back to Throckmorton!

You ask your friend for help and this is the hint he gives you: (in a rather annoying voice) "After a short time, if I look at the block with my *perfect eyes*, I notice that it oscillates at the same frequency as my hand"

So after you get over his annoying voice, you decide to pick apart his hint. What he means by *after a short time* is that the system takes its own time to get into shape for the oscillation that Throckmorton is imparting on it. After all, the block does have mass. And by definition, mass is the tendency of an object to resist change. This period where the block doesn't oscillate with Throcky's hand is called the transient.

If the block oscillates at the same frequency as your friend's hand, we can write $x(t)$ as

$$
x(t) = A e ^ {i \omega t}
$$

Again, we'll comeback to the fact that these are complex numbers later. Moreover, the amplitude $A$, as we will show later, is also a complex number.

Substituting this into the equation of motion we found earlier and cancelling factors of $e^{i \omega t}$, we get

$$
A \left (- m \omega^2 + i b \omega + k \right) = F_0 \Rightarrow A = \frac{F_0}{- m \omega^2 + k + ib}
$$

This is a complex number (ಠ╭╮ಠ)
But this isn't the end of the world. But the spice level just went up to *hot!*. Anyways, remember from math class (I certainly don't, I was probably asleep or on (╯°□°)╯︵ ʞooqǝɔɐɟ ) that a complex number can be written as $A = |A| e ^ {i \phi}$, where $|A|$ is the phase and $\phi$ is the phase.
We can multiply both the numerator and denominator of $A$ by the denominator's conjugate and separate componenets to find

$$
A = \frac{F_0 \left (k - m \omega^2 \right)}{(k - m \omega^2)^2 + (b \omega)^2} - i \frac{F_0 b \omega}{(k - m \omega^2)^2 + (b \omega)^2}
$$

So we got ourselves a complex number eh?
Taking the magnitude, which is just the Pythagorean sum of the imaginary and real parts, and the phase, whose tangent is the quotient when dividing the imaginary part by the real part,

$$
|A| = \frac{F_0}{\sqrt{(k - m \omega^2)^2 + (b \omega)^2 }}
$$

$$
\tan \phi = \frac{b \omega}{m \omega^2 - k}
$$

And we're done.
It can be seen that the maximum amplitude is achieved when $\omega = \sqrt{\frac{k}{m}}$.
Recognize this from the boring lessson you managed to sleep through?
Yeah, that's right! Its the frequency of a block on a spring!

༼ ºل͟º ༼ ºل͟º ༼ ºل͟º ༽ ºل͟º ༽ ºل͟º ༽

༼ ºل͟º ༼ ºل͟º ༼ ºل͟º ༽ ºل͟º ༽ ºل͟º ༽

༼ ºل͟º ༼ ºل͟º ༼ ºل͟º ༽ ºل͟º ༽ ºل͟º ༽

(Ending on a cliffhanger lol)
