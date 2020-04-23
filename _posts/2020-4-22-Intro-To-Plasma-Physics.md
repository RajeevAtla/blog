---
layout: post
mathjax: true
title: "My First Experience With Plasma Physics"
categories: Plasma Physics,  misc
---
These are my notes for Chapter 1 of *Introduction to Plasma Physics and Controlled Fusion* by Francis F. Chen.

MLA Citation - Chen, Francis F. *Introduction to Plasma Physics and Controlled Fusion*. 3rd ed., Springer International Publishing Switzerland, 2016, *Springer Link*, [link.springer.com/content/pdf/10.1007%2F978-3-319-22309-4.pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-22309-4.pdf.)

## 1.1 Occurence of Plasmas in Nature
### The Nature of the Universe
According to NASA's [WMAP](https://wmap.gsfc.nasa.gov/universe/uni_matter.html), the universe is composed primarily of dark energy (71.4 %).
Following that is dark matter (24 %).
Both last and least is regular matter (4.6 %).

### About Plasma
Plasma is an ionized gas.
This means that at least one of the electrons in an atom that constitutes the plasma has been stripped free.

Plasma is also called the "fourth state of matter.
When solids are heated, they turn into liquid.
When liquids are heated, they turn into a gas.
When gases are heated enough to ionize them, a plasma is created.

A plasma is made up of both ions and electrons, so there are a rather large number of electric fields everywhere inside the plasma.
Moreover, these charged particles are always moving, so there are also magnetic fields being created.
The particles can now interact with each other through their magnetic and electric fields, significantly increasing their range of possible motions.
Moreover, external magnetic fields are often applied to a plasma in order to control it.

Usually, plasma only exists in a vacuum (e.g. outer space)
In order to create it in a laboratory, we need to pump air out of a vacuum chamber to be used to create the plasma in.
Earth is obviously not a vacuum, so plasmas don't occur naturally.
It is rare to see plasma outside of lightning bolts, arouras, fluorescent tubes, and plasma TVs.

### Saha Equation

This can be seen through the Saha ionization equation, developed by Indian astrophysicist Meghnad Saha in 1920.
The equation predicts the amount of ionization in a gas at thermal equilibrium.
Let $n_i$ be the numerical density of the ionized atoms and let $n_n$ be the numerical density of the neutral atoms.
Let $T$ be the temperature of the gas (we use Kelvin here).
Let $k$ be the Boltzmann constant.
Let $U_i$ be the ionization energy of the gas - i.e. the amount of thermal energy needed to be given to an atom to remove its outermost electron.
The Saha equation mathematically states the relationship as


$$
\frac{n_i}{n_n} \approx \left (2.4 \times 10^{21} \right) \frac{T^{\frac{3}{2}}}{n_i} e^{- \frac{U_i}{kT}}
$$


Recalling that nitrogen makes up the highest amount in the Earth's atmosphere, we can approximate the atmosphere as made entirely of nitrogen, which has an ionization energy of $14.5$ eV.
For air at room temperature, $n_n$ is approximately $3 \times 10^{25} \, \text{m}^{-3}$.
Room temperature is around $300$ Kelvin, so by the Saha equation, we can estimate that the fractional ionization in the air we breath is extremely low:


$$
\frac{n_i}{n_n} \sim 10^{-122}
$$


We graph the visual representation using Asymptote:
![Diagram 4]({{ site.url }}/assets/images/diagram4.png "Diagram 4")

As you can see, as temperature is raised, the amount of ionization increases rapidly, eventually making $n_i = n_n$.
That's why plasmas can't occur naturally on Earth, as life couldn't easily coexist with the plasma.

### Physical Interpretation

We don't want to overuse the Saha equation, as it is a very rough approximation.
However, we do want to emphasize the physical principles behind it.
From statistical mechanics, the atoms in a gas have a spread of thermal energies.
Intuitively, an atom with more energy will have a higher chance of knocking out an electron when colliding with another atom.
Moreover, the atoms will obviously collide with more force.

## 1.2 Definition of Plasma

Not all ionized gases can be called plasmas, as there is always some degree of ionization in a gas, no matter what temperature.
Therefore, its nice to have a definition to rely on:

*A plasma is a quasineutral gas of charged and neutral particles which exhibits collective behavior.* (Chen 1.2)

We now discuss collective behavior.
In a plasma, there are charged particles: positive ions and negative electrons.
These charges produce electric fields and their movement produces magnetic fields.
