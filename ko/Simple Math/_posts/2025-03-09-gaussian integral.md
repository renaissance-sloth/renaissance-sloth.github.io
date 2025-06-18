---
title: "가우스 적분"
excerpt: 가우스 적분(Gaussian integral)은 $\int_{-\infty}^{\infty}{e^{-x^{2}}}dx$이다. 답은 $\sqrt{\pi}$이다.
tags: math
header:
  teaser: 
---

# 가우스 적분
가우스 적분(Gaussian integral)은 $\int_{-\infty}^{\infty}{e^{-x^{2}}}dx$이다. 답은 $\sqrt{\pi}$이다.

# 값 유도
## 극좌표계
극좌표계를 통한 적분으로 구할 수 있다.

구하고자 하는 값을 $I$라 해보자.

$\int_{-\infty}^{\infty}{e^{-x^{2}}}dx=I$

우선 아래와 같은 중적분을 생각해 보자.

$ I^{2}$ 
$= \left(\int_{-\infty}^{\infty}{e^{-x^{2}}}dx\right)\left(\int_{-\infty}^{\infty}{e^{-y^{2}}}dy\right)$ 
$= \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} {e^{-x^{2}}e^{-y^{2}}} dxdy $

간단히 하면,

$\int_{-\infty}^{\infty}\int_{-\infty}^{\infty} {e^{-(x^{2}+y^{2})}} dxdy$

극좌표로 $dxdy\rightarrow rdrd\theta$, $x^{2}+y^{2}\rightarrow r^{2}$로 바꿀 수 있고, 적분구간은 $r$이 $[0,\infty)$, $\theta$가 $[0,2\pi]$가 된다.

따라서 

$\int_{0}^{2\pi}\int_{0}^{\infty} {re^{-r^{2}}} drd\theta$
$=\int_{0}^{2\pi}d\theta \int_{0}^{\infty} {re^{-r^{2}}} dr$이다. 

이때, $re^{-r^{2}}$
$=\frac{d}{dr}\left(-\frac{1}{2}e^{-r^{2}}\right)$이다.

따라서, 
$\int_{0}^{2\pi}d\theta \int_{0}^{\infty} {re^{-r^{2}}} dr$
$=2\pi \left[-\frac{1}{2}e^{-r^{2}}\right]_{0}^{\infty}$
$=2\pi(0--\frac{1}{2})$
$=\pi$
이다.

결과적으로 
$ I^{2}$ 
$= \pi$임을 얻어내었다.

그렇기에 $I$
$=\int_{-\infty}^{\infty}{e^{-x^{2}}}dx$
$= \sqrt{\pi}$이다.