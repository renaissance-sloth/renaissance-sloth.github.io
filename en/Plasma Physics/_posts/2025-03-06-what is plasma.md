---
title: "Introducing Plasma Physics"
excerpt: Only 1% of the universe is matter we know, and 99% of that is in a plasma state.
tags: physics plasma intro
header:
  teaser: https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcRZplqQsfMnOSyYRjjzr6zXYM-zkt-rm1oeXLK_GKncRFjhT2_n
---

# Introduction to Plasma Physics
## Plasma in Nature
Only 1% of the universe is matter we know, and 99% of that is in a plasma state.

Plasma is also called the "fourth state of matter." The states of matter are usually thought of as solid-liquid-gas, but when gas is heated further, it becomes plasma.

Plasma is made up of ions and electrons, so electric fields are everywhere, and particles "collide" if they can feel each other's electric fields.

Fluid dynamics, which describes the flow of water and air, is already complex, but the electromagnetic force of plasma makes the motion even more diverse.

In the end, physicists studying plasma must solve the four Maxwell's equations in electromagnetism and the equations of motion in mechanics.

Since air cools plasma, plasma usually exists only in a vacuum. In space, it is mostly in a plasma state. The interiors and atmospheres of stars, gas nebulae, and entire galaxies are plasma, which is why we can see them.

On Earth, there is less plasma because of the atmosphere. On Earth, plasma can be found in lightning flashes, colorful auroras, fluorescent lights, and the pixels of plasma TVs.

The "Saha equation" allows us to calculate the amount of ionization of gases in thermal equilibrium.

### Saha equation
$ \frac{n_{i}}{n_{n}} \approx 2.4\times10^{21}\frac{T^{3/2}}{n_{i}}e^{-U_{i}/KT} $

Here, $n_{i}$ is the density of ionized atoms (number per $m^{3}$), $n_{n}$ is the density of neutral atoms (number per $m^{3}$), $T$ is the temperature (K), $K$ is the Boltzmann constant (approximately $1.380\times10^{−23} J/K$), and $U_{i}$ is the ionization energy ($J$).

Let's calculate for the atmosphere, $n_{n}=3\times10^{25}m^{-3}$, $T=300K$, $U_{i}=14.5eV$, $\frac{n_{i}}{n_{n}＋n_{i}} \approx \frac{n_{i}}{n_{n}}$, and the expected value by the equation is $\frac{n_{i}}{n_{n}} \approx 10^{-122}$.

When the temperature rises enough that $KT$ is similar to the ionization energy $U_{i}$, it becomes plasma. This is why plasma exists on high-temperature celestial bodies, but not on Earth.

Let's look at the physical meaning contained in the Saha equation.

Atoms can be ionized in collisions with enough energy to lose electrons. At low temperatures, there are fewer particles with enough energy, so there are fewer strong collisions. The exponent of the equation means that the atoms decay exponentially with temperature, which is fast enough. Once an atom is ionized, it remains so until it meets an electron.

The recombination rate depends on the electron density, which is equal to $n_{i}$. Therefore, the ion fraction must decrease as $n_{i}$ decreases. This is why $n_{i}$ is in the denominator on the right. Plasmas in the interstellar medium can exist even at low temperatures because $n_{i}$ is small.

## How do you define plasma?

Not all ionized gases are plasmas. All gases are always ionized to some extent. Therefore, a useful definition of plasma is "plasma is a `quasineutral` gas of charged and neutral particles that exhibits `collective behavior`."

Now, let's define `quasineutrality` and `collective behavior`. Quasineutrality will be explained later, so we will skip it, and collective behavior is as follows.

Consider the forces acting on ordinary air molecules. Molecules are neutral and light, so electromagnetic forces and gravity are ignored. Molecules move freely until they collide, and collisions control their motion.

Since plasma is charged, the charges move, creating differences in the densities of positive and negative charges, and creating currents and electromagnetic fields. These affect the motion of other charged particles over long distances.

![Illustration showing long-range electrostatic forces in plasma](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRDiGHE6MO46AAiD-zCB8tpcqc7iZ_FS2GICw&s)

Consider a region of charged plasma separated by a distance r, as shown in the figure above. A and B experience forces that are inversely proportional to the square of the distance. However, for a given solid angle ($\Delta r/r$) the volume of B that affects A is proportional to the cube of r. Therefore, plasmas exert forces over long distances. `Collective action` refers to motion that depends not only on local collisions but also on distant plasma conditions.

## What is temperature?

Let's review the physical concept of "temperature" again.

A gas in thermal equilibrium has particles of all velocities, and these velocities are very likely to follow the Maxwell distribution.

### 1-dimensional Maxwell distribution
Let's simply assume that particles only move along straight lines (in 1 dimension). A strong magnetic field can actually make electrons move only along magnetic field lines.

The 1-dimensional Maxwell distribution is $f(u)=A \exp\left( -\frac{1}{2}mu^{2}/KT \right)$. Here, $f du$ is the number of particles per unit volume whose velocities are between $u$ and $u+du$, $\frac{1}{2}mu^{2}$ is the kinetic energy, and $K$ is the Boltzmann constant. Since $k$ will be used as the wave propagation constant, we will use a capital letter for the Boltzmann constant.

Since the density $n$ (the number of particles per unit volume, $m^{-3}$) is equal to the number of particles at all velocities, it is given by $n=\int_{-\infty}^{\infty} {f(u)du}$, and can be calculated as $A=n\left(\frac{m}{2\pi KT}\right)^{1/2}$.

---
<details>
<summary>How to calculate $A$</summary>

$n$
$=\int_{-\infty}^{\infty} {f(u)du}$
$=\int_{-\infty}^{\infty} {A \exp\left( -\frac{1}{2}mu^{2}/KT \right)} du$
$=A\int_{-\infty}^{\infty} {\exp\left( -\frac{m}{2KT} u^{2}\right)} du$
$=A\sqrt{2\pi \int_{0}^{\infty} r{ \exp\left( -\frac{m}{2KT} r^{2}\right)} dr}$
$=A\sqrt{2\pi \int_{0}^{\infty} \frac{d}{dr} \left(-\frac{KT}{m} \exp\left( -\frac{m}{2KT} r^{2}\right)\right) dr}$
$=A\sqrt{2\pi \left[-\frac{KT}{m} \exp\left( -\frac{m}{2KT} r^{2}\right)\right]_{0}^{\infty}}$
$=A\sqrt{2\pi \left(0 - -\frac{KT}{m}\right)}$
$=A\sqrt{\frac{2\pi KT}{m}}$

$\therefore A$ $=n\sqrt{\frac{m}{2\pi KT}}$ $=n\sqrt{\frac{m}{2\pi KT}}$ $=n\left(\frac{m}{2\pi KT}\right)^{1/2}$
</details>
---

The width of the distribution can be characterized by a constant $T$, which is called the temperature.

To understand the exact meaning of $T$, let's calculate the average kinetic energy of the particles.

$E_{av}=\frac{\int_{-\infty}^{\infty} {\frac{1}{2}mu^{2} f(u)}du}{\int_{-\infty}^{\infty} {f(u)}du}$

For convenience, let's define it as follows.

$v_{th}=(2KT/m)^{1/2}$, $y=u/v_{th}$

If we express the one-dimensional Maxwell distribution using the defined symbol,
$f(u)=A \exp(-u^{2}/v_{th}^{2})$
and the average kinetic energy is
$E_{av}$ $=\frac{\frac{1}{2}m A v_{th}^{3}\int_{-\infty}^{\infty} {\left[\exp(-y^{2})\right]y^{2}}dy}{A v_{th}\int_{-\infty}^{\infty} {\exp(-y^{2})}dy}$ .

<details>
<summary>Let's simply calculate the average kinetic energy.</summary>
<p></p>
<p>First, we can calculate the $\int_{-\infty}^{\infty} {y^{2}\left[\exp(-y^{2})\right]}dy$ part of the molecule.</p>

<p>If we integrate by parts</p>

<p>$\int_{-\infty}^{\infty} {y^{2}\left[\exp(-y^{2})\right]}dy$
$= \int_{-\infty}^{\infty} {y \cdot \left[\exp(-y^{2})\right]y}dy$</p>

<p>And, $\left[y \cdot -\frac{1}{2}\left[\exp(-y^{2})\right]\right]_{-\infty}^{\infty}=0$, so </p>

<p>$=-\int_{-\infty}^{\infty} {-\frac{1}{2}\exp \left(-y^{2}\right)} dy$
$=\frac{1}{2}\int_{-\infty}^{\infty} {\exp \left(-y^{2}\right)} dy$.</p>

<p>Now, by substituting into the average kinetic energy equation and simplifying the integral,</p>

<p>$E_{av}$ 
$=\frac{\frac{1}{2}m A v_{th}^{3}\int_{-\infty}^{\infty} {\left[\exp(-y^{2})\right]y^{2}}dy}{A v_{th}\int_{-\infty}^{\infty} {\exp(-y^{2})}dy}$
$=\frac{\frac{1}{2}m A v_{th}^{3}\frac{1}{2}\int_{-\infty}^{\infty} {\exp \left(-y^{2}\right)} dy}{A v_{th}\int_{-\infty}^{\infty} {\exp(-y^{2})}dy}$
$=\frac{\frac{1}{2}m A v_{th}^{3}\frac{1}{2}}{A v_{th}}$
$=\frac{1}{4}m v_{th}^{2}$</p>

<p>Since $v_{th}=(2KT/m)^{1/2}$ is defined, </p>

<p>We can calculate $\frac{1}{2}m v_{th}^{2}=KT$.</p>
</details>

As a result, we can obtain $E_{av}=\frac{1}{2}KT$.

### 3D Maxwell Distribution
If we only have the results in 1 dimension, it is not difficult to extend to 3 dimensions.

Maxwell distribution now becomes
$f(u,v,w)$$=A_{3}\exp\left[ -\frac{1}{2}m\left( u^{2}+v^{2}+w^{2} \right)/KT \right]$

At this time, $A_{3}=n\left(\frac{m}{2\pi KT}\right)^{3/2}$.

The average kinetic energy is
$E_{av}$
$=\frac{\iiint_{-\infty}^{\infty} {A_{3}\frac{1}{2}m \left( u^{2}+v^{2}+w^{2} \right) e^{-\frac{1}{2}m\left( u^{2}+v^{2}+w^{2} \right)/KT}} du dv dw}{\iiint_{-\infty}^{\infty} {A_{3}e^{-\frac{1}{2}m\left( u^{2}+v^{2}+w^{2} \right)/KT}} du dv dw}$



Since Maxwell distribution is isotropic, the equation is symmetrical in $u,v,w$.

Therefore, we only need to calculate the first term and multiply it by 3.

As a result, we can obtain $E_{av}=\frac{3}{2}KT$.

As a generalized result, we can obtain the average kinetic energy of $\frac{1}{2}KT$ for each degree of freedom.

### Representation of Temperature
Since temperature $T$ and average kinetic energy $E_{av}$ are deeply related, temperature is expressed in energy units in plasma physics.

To express temperature, energy corresponding to $KT$ is used.

When $KT$ $=1 eV$ $= 1.6\times 10^{-19} J$, $T$ $= \frac{1.6\times10^{-19}}{1.38\times10^{-23} }$ $\approx 11600 ^{\circ}K$.

For nuclear fusion to occur, a temperature of about $10 keV$ is required. The density must be lower than $10^{14}$.

Sometimes ions and electrons often have Maxwellian distributions of different temperatures ($T_{i}, T_{e}$).

This happens because the collision rate between ions or between electrons themselves is greater than the collision rate between ions and electrons.

Each may be in thermal equilibrium, but the plasma will not last long enough for the two temperatures to become equal.

In the presence of a magnetic field **B**, even the same ions can have different temperatures. This is because the forces parallel to **B** and the forces perpendicular to it (Lorenz forces) are different. Each can follow a Maxwell distribution with a temperature ($ T_{\bot}, T_{&#124;&#124;} $).

High temperature does not necessarily mean a lot of heat. In the case of fluorescent lamps, the internal electron temperature is about $20,000^{\circ}K$, but the electron density is much lower than the atmospheric pressure, so the heat capacity is not large. Therefore, the total amount of heat transferred is small despite the high temperature.

The plasma used in the laboratory is usually hot, about $1,000,000^{\circ}K (100 eV)$, but the density is only about $10^{18}-10^{19}$ per $m^{3}$, so there is no need to worry about the wall containing the plasma getting hot.

/TODO()