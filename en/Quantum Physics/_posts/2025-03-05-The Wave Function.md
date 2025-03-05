---
title: "The Wave Function"
excerpt: "The Wave Function"
tags: syllabus physics quantum
header:
  teaser: https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcQqoGDngbpKU_7jpFv4thAwH03rpQ8HZk7VXCkdFrS0IHbkrjgE
---

# The Wave Function

## The Schrödinger Equation

In Newtonian mechanics, there is a very famous governing equation called $\vec{F} = m \vec{a}$. This can be interpreted as saying that when a physical force (electromagnetic force, frictional force, etc.) is applied, the object accelerates. If you solve the differential equation above, you can obtain the position and velocity of the object. Similarly, in quantum mechanics, the Schrödinger equation plays the same role.

The dynamical state of a particle is completely specified by a wave function $\Psi$.
For a non-relativistic, spinless particle, 
the evolution of $\Psi(r,t)$ is governed by the **Schrödinger equation** $ i \hbar \frac{\partial \Psi}{\partial t} = - \frac{\hbar^{2}}{2m} \nabla^{2}\Psi + V\Psi $

where $\nabla^{2}f=
\left( 
  \frac{\partial^{2}}{\partial x^{2}}+
  \frac{\partial^{2}}{\partial y^{2}}+
  \frac{\partial^{2}}{\partial z^{2}} 
\right)f$ called **Laplacian** and $\hbar = \frac{h}{2\pi} = 1.054572\times10^{-34} Js$

### Quantization Rule

In quantum mechanics, anything that can be measured classically becomes an operator.

The Schrödinger equation can be obtained by applying the operator rules

$E \rightarrow i\hbar\frac{\partial}{\partial t}$

$\vec{p}\rightarrow -i\hbar\vec{\nabla}$, $ p^{2} \rightarrow -\hbar^{2} \nabla^{2} $

$ \vec{r}=\vec{r} $

to the classical relation for a conservative system $ E=\frac{p^{2}}{2m}+V $ so that $ i\hbar\frac{\partial}{\partial t}\Psi=\left( -\frac{\hbar^{2}}{2m}\nabla^{2}+V \right)\Psi $

## The Statistical Interpretation

Born said $\Psi$ is **Probability amplitude**.

to get the probability of finding particles between a & b at time t is $ \frac{
  \int_{a}^{b} {dx \left| \Psi (x,t) \right|^{2}}
 }{
  \int_{-\infty}^{\infty} {dx \left| \Psi (x,t) \right|^{2}}
 } $

### Philosophy

The realist claim, represented by Einstein, is as follows: There is an objective reality. Causality and locality are preserved. The statistical nature of quantum theory means that it is incomplete (there are hidden variables).

The orthodox (Copenhagen interpretation) claim, represented by Bohr, is as follows: The statistical nature of measurement is a fundamental property of nature (there is no "strict" causality).

The agnostic claim is as follows: There is no need to worry about such metaphysical questions.

There is a famous idiom for this:
> Shut up and calculate!

To the next question, "Where is the particle just before the measurement shows that it is at point C?", each person's answer is as follows:

Realist: At point C.

Orthodox: Nowhere.

Agnostic: That is a meaningless question.

A relatively recent Bell inequality experiment shows that the Orthodox side is correct.

### Collapse of Wave Function
`Repeating a measurement right away always gives the same value.`

Wave function collapses to an eigenfunction of the measurement operator.

## Probability
### Discrete Variables

Total number: $ N=\sum_{j=0}^{\infty} {N(j)} $

Probability of $j$: $ P(j)=\frac{N(j)}{N} $

Probability of $j$ or $k$: $P(j)+P(k)$

Sum rule: $ \sum_{j=0}^{\infty}P(j)=1 $

Median ($j_m$): $ \sum_{j=0}^{j_{m}-1}P(j)=\sum_{j=j_{m}+1}^{\infty}P(j) $

Average: $\left<j\right>=\sum_{j=0}^{\infty}jP(j)$

Average/expectation value of a function $f$ of $j$: $ \left<f(j)\right>=\sum_{j=0}^{\infty}f(j)P(j) $

Variance(Standard deviation): $ \sigma\equiv\sqrt{\left<(j-\left<j\right>)^{2}\right>} = \sqrt{\left<j^{2}\right>-\left<j\right>^{2}} $

/TODO()

## Normalization

## Momentum

## The Uncertainty Principle
