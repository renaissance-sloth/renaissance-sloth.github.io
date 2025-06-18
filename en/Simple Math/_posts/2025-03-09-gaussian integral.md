---
title: "Gaussian integral"
excerpt: The Gaussian integral is $\int_{-\infty}^{\infty}{e^{-x^{2}}}dx$. The answer is $\sqrt{\pi}$.

tags: math
header:
  teaser:
---

# Gaussian integral
The Gaussian integral is $\int_{-\infty}^{\infty}{e^{-x^{2}}}dx$. The answer is $\sqrt{\pi}$.

# Derivation of values
## Polar coordinates
We can derive it by integrating through polar coordinates.

Let's call the value we want to derive $I$.

$\int_{-\infty}^{\infty}{e^{-x^{2}}}dx=I$

First, let's consider the following double integral.

$I^{2}$
$= \left(\int_{-\infty}^{\infty}{e^{-x^{2}}}dx\right)\left(\int_{-\infty}^{\infty}{e^{-y^{2}}}dy\right)$
$= \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} {e^{-x^{2}}e^{-y^{2}}} dxdy $

Simply put,

$\int_{-\infty}^{\infty}\int_{-\infty}^{\infty} {e^{-(x^{2}+y^{2})}} dxdy$

In polar coordinates $dxdy\rightarrow rdrd\theta$, It can be replaced with $x^{2}+y^{2}\rightarrow r^{2}$, and the integration interval is $r$ is $[0,\infty)$, $\theta$ is $[0,2\pi]$.

Therefore,

$\int_{0}^{2\pi}\int_{0}^{\infty} {re^{-r^{2}}} drd\theta$
$=\int_{0}^{2\pi}d\theta \int_{0}^{\infty} {re^{-r^{2}}} dr$.

In this case, $re^{-r^{2}}$
$=\frac{d}{dr}\left(-\frac{1}{2}e^{-r^{2}}\right)$

Therefore,
$\int_{0}^{2\pi}d\theta \int_{0}^{\infty} {re^{-r^{2}}} dr$
$=2\pi \left[-\frac{1}{2}e^{-r^{2}}\right]_{0}^{\infty}$
$=2\pi(0--\frac{1}{2})$
$=\pi$
.

As a result,
$ I^{2}$
$= \pi$ is obtained.

Therefore, $I$
$=\int_{-\infty}^{\infty}{e^{-x^{2}}}dx$
$= ​​\sqrt{\pi}$