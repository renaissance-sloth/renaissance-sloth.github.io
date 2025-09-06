---
title: "파동 함수"
excerpt: 
tags: physics quantum
header:
  teaser: https://drive.google.com/thumbnail?id=1Qm_zarRZ2x-0ElOGprphzt1zN4FiPnS6&sz=w1000
---
# 파동 함수

## 슈뢰딩거 방정식

고전 역학에서 뉴턴의 운동 방정식 $\vec{F}$ $= m \vec{a}$는 힘과 가속도의 관계를 나타내며, 이를 통해 물체의 움직임을 결정할 수 있습니다. 양자 역학에서는 이에 대응하는 방정식이 바로 **슈뢰딩거 방정식**입니다.

입자의 상태는 **파동 함수** $\Psi$로 완전히 기술되며, 스핀을 고려하지 않는 비상대론적 경우에 대한 시간 의존 슈뢰딩거 방정식은 다음과 같습니다.

$ i \hbar \frac{\partial \Psi}{\partial t}$ $= - \frac{\hbar^{2}}{2m} \nabla^{2}\Psi + V\Psi $

여기서,
- $\hbar$ $= \frac{h}{2\pi}$ $\approx 1.05\times10^{-34} Js$
- $\nabla^{2}$ $= \left(
\frac{\partial^{2}}{\partial x^{2}}+
\frac{\partial^{2}}{\partial y^{2}}+
\frac{\partial^{2}}{\partial z^{2}}
\right)$: **라플라시안 연산자**

이 방정식을 풀면 특정 계의 양자 상태를 기술하는 파동 함수를 얻을 수 있습니다.

### 양자화 규칙

고전 역학에서 관측 가능한 물리량(에너지, 운동량 등)은 양자 역학에서 연산자로 대체됩니다.

- 에너지: $E \rightarrow i\hbar\frac{\partial}{\partial t}$
- 운동량: $\vec{p} \rightarrow -i\hbar\vec{\nabla}$, $ p^{2} \rightarrow -\hbar^{2} \nabla^{2}$
- 위치: $\vec{r} \rightarrow \vec{r}$

이를 고전적 관계식 $E$ $= \frac{p^2}{2m} + V$에 적용하면 슈뢰딩거 방정식을 얻을 수 있습니다.

## 통계적 해석

막스 보른은 파동 함수 $\Psi$가 확률 진폭(probability amplitude)이며, 그 제곱 $\left&#124; \Psi \right&#124;^{2}$ 이 입자가 특정 위치에 있을 확률 밀도를 나타낸다고 제안했습니다.

입자가 시간 $t$에서 구간 $[a, b]$에 있을 확률은 다음과 같이 계산됩니다.
$ \frac{
\int_{a}^{b} {dx \left| \Psi (x,t) \right|^{2}}
}{
\int_{-\infty}^{\infty} {dx \left| \Psi (x,t) \right|^{2}}
} $

이 해석은 양자 역학의 확률적 본질을 설명하는 핵심 개념입니다.

### 철학적 해석

양자 역학의 해석에는 여러 견해가 있습니다.

- **실재론(아인슈타인):** 입자는 측정 전에 특정한 위치에 존재한다.
- **코펜하겐 해석(보어):** 입자는 측정 전에는 특정한 위치에 존재하지 않는다.
- **불가지론:** 형이상학적 논쟁은 의미가 없으며, 계산에 집중해야 한다.

이와 관련된 유명한 문구로 **"Shut up and calculate!"**가 있습니다.

벨 부등식 실험은 코펜하겐 해석이 실재론적 해석보다 양자역학을 더 잘 설명함을 보여주었습니다.

### 파동 함수의 붕괴

`측정을 바로 반복하면 항상 같은 값이 나옵니다.`

이는 측정이 이루어진 후 파동 함수가 해당 연산자의 고유 상태로 붕괴됨을 의미합니다. 즉, 특정한 상태가 결정된 이후에는 같은 실험을 반복해도 동일한 결과를 얻습니다.

## 확률 개념

### 이산 변수의 확률

- 전체 개수: $N$ $= \sum_{j=0}^{\infty} N(j)$
- 특정 값 $j$가 나올 확률: $ P(j)$ $= \frac{N(j)}{N} $
- $j$ 또는 $k$가 나올 확률: $ P(j) + P(k) $
- 확률의 총합: $ \sum_{j=0}^{\infty} P(j)$ $= 1 $
- 중간값($j_m$): $ \sum_{j=0}^{j_{m}-1} P(j)$ $= \sum_{j=j_{m}+1}^{\infty} P(j) $
- 평균값: $ \langle j \rangle$ $= \sum_{j=0}^{\infty} j P(j) $
- 함수 $f$의 기대값: $ \langle f(j) \rangle$ $= \sum_{j=0}^{\infty} f(j) P(j) $
- 분산(표준편차):
  $ \sigma\equiv\sqrt{\left<(j-\left<j\right>)^{2}\right>}$ $= \sqrt{\left<j^{2}\right>-\left<j\right>^{2}} $

### 연속 변수의 확률

- 전체 확률: $\int_{-\infty}^{\infty}\rho(x)dx=1$
- $a$와 $b$ 사이의 확률: $P_{ab}$ $=\int_{a}^{b}\rho(x)dx$
- $\langle x \rangle$ $=\int_{-\infty}^{\infty}x\rho(x)dx$
- $\langle f(x) \rangle$ $=\int_{-\infty}^{\infty}f(x)\rho(x)dx$
- $\sigma^{2}$ $=\int_{-\infty}^{\infty}\left(x-\langle x \rangle\right)^{2} \rho(x)dx$ $= \left\langle\left(x-\langle x \rangle\right)^{2}\right\rangle$ $=\langle x^{2} \rangle- \langle x \rangle^{2}$

이러한 확률 개념은 양자 역학의 본질적인 확률적 성질을 정량적으로 설명하는 데 사용됩니다.

## 정규화

이전에 언급한 바와 같이 입자가 시간 $t$에서 구간 $[a, b]$에 있을 확률은 다음과 같이 계산됩니다.
$ \frac{
\int_{a}^{b} {dx \left| \Psi (x,t) \right|^{2}}
}{
\int_{-\infty}^{\infty} {dx \left| \Psi (x,t) \right|^{2}}
} $

만일 $\int_{-\infty}^{\infty} {dx \left| \Psi (x,t) \right|^{2}}$ $=N$으로 유한하다면, $\rho(x,t)$ $=\frac{
\left&#124; \Psi (x,t) \right&#124;^{2}
}{
\int_{-\infty}^{\infty} {dx \left&#124; \Psi (x,t) \right&#124;^{2}}
}$이다. 이를 $\Psi$가 `square-integrable`, `normalizable` 하다고 한다.

$\Phi(x,t)$ $=\frac{1}{\sqrt{N}}\Psi(x,t)$로 두면, $\rho(x,t)$ $= \left&#124; \Phi(x,t) \right&#124;^{2}$이고, $\int_{-\infty}^{\infty} {dx \left&#124; \Phi (x,t) \right&#124;^{2}}=1$이다. 이때, $\Phi$를 `normalized` 되었다고 한다.

### 슈뢰딩거 방정식의 정규화
---
우선 전체 확률을 시간에 대해 미분할 것이다.

$ \frac{d}{dt} \int_{-\infty}^{\infty} {dx \left&#124; \Psi (x,t) \right&#124;^{2}} $ 
$= \int_{-\infty}^{\infty} {dx \frac{\partial}{\partial t} \left&#124; \Psi (x,t) \right&#124;^{2}} $

여기서
$\frac{\partial}{\partial t} \left&#124; \Psi (x,t) \right&#124;^{2}$ $=\frac{\partial}{\partial t}\left( \Psi^{\*} \Psi \right)$ 
$=\frac{\partial \Psi^{\*}}{\partial t}\Psi+\Psi^{\*}\frac{\partial \Psi}{\partial t}$
이다.

---
슈뢰딩거 방정식을 다시 가져오자. 1차원에서 볼 것이기에 라플라시안 연산자는 공간에 대한 이차 미분으로 바뀌었다.

$ i \hbar \frac{\partial \Psi}{\partial t}$ $= - \frac{\hbar^{2}}{2m} \frac{\partial^{2}\Psi}{\partial x^{2}}  + V\Psi $

양변에 $ \Psi^{\*} $를 곱하면 

$ i \hbar\Psi^{\*} \frac{\partial \Psi}{\partial t}$ $= - \frac{\hbar^{2}}{2m} \Psi^{\*}\frac{\partial^{2}\Psi}{\partial x^{2}}  + V\Psi^{\*}\Psi $
을 얻었다.

따라서
$ \Psi^{\*} \frac{\partial \Psi}{\partial t}$ $= - \frac{\hbar}{2mi} \Psi^{\*}\frac{\partial^{2}\Psi}{\partial x^{2}}  + \frac{1}{i\hbar}V\Psi^{\*}\Psi $
이다.

---

다시 슈뢰딩거 방정식에서 conjugate를 취하면

$ -i \hbar \frac{\partial \Psi^{\*}}{\partial t}$ $= - \frac{\hbar^{2}}{2m} \frac{\partial^{2}\Psi^{\*}}{\partial x^{2}}  + V\Psi^{\*} $이다. 

이때, $V$는 실함수이기 때문에 바뀌지 않았다.

양변에 $\Psi$를 곱하면

$ -i \hbar \frac{\partial \Psi^{\*}}{\partial t}\Psi$ $= - \frac{\hbar^{2}}{2m} \frac{\partial^{2}\Psi^{\*}}{\partial x^{2}} \Psi + V\Psi^{\*}\Psi $
을 얻었다.

따라서
$ \frac{\partial \Psi^{\*}}{\partial t}\Psi$ $= \frac{\hbar}{2mi} \frac{\partial^{2}\Psi^{\*}}{\partial x^{2}} \Psi - \frac{1}{i\hbar}V\Psi^{\*}\Psi $
이다.

---

$\frac{\partial \Psi^{\*}}{\partial t}\Psi+\Psi^{\*}\frac{\partial \Psi}{\partial t}$

$= \frac{\hbar}{2mi} \frac{\partial^{2}\Psi^{\*}}{\partial x^{2}} \Psi - \frac{\hbar}{2mi} \Psi^{\*}\frac{\partial^{2}\Psi}{\partial x^{2}} $
$ - \frac{1}{i\hbar}V\Psi^{\*}\Psi + \frac{1}{i\hbar}V\Psi^{\*}\Psi $

$= - \frac{\hbar}{2mi} (\Psi^{\*}\frac{\partial^{2}\Psi}{\partial x^{2}} - \frac{\partial^{2}\Psi^{\*}}{\partial x^{2}} \Psi)$
$= - \frac{\hbar}{2mi} \frac{\partial}{\partial x} (\Psi^{\*}\frac{\partial\Psi}{\partial x} - \frac{\partial\Psi^{\*}}{\partial x} \Psi)$
로 얻을 수 있고,

$ \frac{d}{dt} \int_{-\infty}^{\infty} {dx \left&#124; \Psi (x,t) \right&#124;^{2}} $ 
$= \int_{-\infty}^{\infty} {dx \frac{\partial}{\partial t} \left&#124; \Psi (x,t) \right&#124;^{2}} $
$= - \frac{\hbar}{2mi}\int_{-\infty}^{\infty} {dx  \frac{\partial}{\partial x} (\Psi^{\*}\frac{\partial\Psi}{\partial x} - \frac{\partial\Psi^{\*}}{\partial x} \Psi)} $
$= - \frac{\hbar}{2mi} (\Psi^{\*}\frac{\partial\Psi}{\partial x} - \frac{\partial\Psi^{\*}}{\partial x} \Psi) \left.\right&#124;_{-\infty}^{\infty} $
$=0$
으로, 

전체 확률은 시간에 무관하게 상수이고, 정규화가 되었다면 전체 확률은 1로 보존된다.

---

### 연속방정식

$\frac{\partial}{\partial t} \left&#124; \Psi (x,t) \right&#124;^{2}$
$= - \frac{\hbar}{2mi} \frac{\partial}{\partial x} (\Psi^{\*}\frac{\partial\Psi}{\partial x} - \frac{\partial\Psi^{\*}}{\partial x} \Psi)$
을 3차원에서 살펴보자. $\frac{\partial}{\partial x}\to\nabla$ 로만 바꾸면 된다.

결과는
$\frac{\partial}{\partial t} \left&#124; \Psi (x,t) \right&#124;^{2}$
$= - \frac{\hbar}{2mi} \nabla \cdot (\Psi^{\*}\nabla\Psi - (\nabla\Psi^{\*}) \Psi)$
로 나타난다.

이때, $\left&#124; \Psi (x,t) \right&#124;^{2}$ $= \rho$, $\frac{\hbar}{2mi} (\Psi^{\*}\nabla\Psi - (\nabla\Psi^{\*}) \Psi)$ $= \vec{j}$로 정의하자.

$\frac{\partial\rho}{\partial t} + \nabla\cdot\vec{j}=0$
를 얻을 수 있고, 이는 연속방정식이다.

확률 밀도가 보존된다는 의미이다.

## 운동량

위치의 기댓값은 다음과 같이 표현한다.

$\langle x\rangle$
$=\int_{-\infty}^{\infty}  x\left&#124; \Psi (x,t) \right&#124;^{2}dx$
$= \int_{-\infty}^{\infty}  \Psi^{\*}(x,t)x\Psi(x,t)dx$

위치의 기댓값을 시간에 대해 미분해보자.

$\frac{d}{dt} \langle x\rangle$
$= \int_{-\infty}^{\infty} x \frac{\partial}{\partial t} \left&#124; \Psi (x,t) \right&#124;^{2}dx$
$= - \frac{\hbar}{2mi} \int_{-\infty}^{\infty} x \frac{\partial}{\partial x} (\Psi^{\*}\frac{\partial\Psi}{\partial x} - \frac{\partial\Psi^{\*}}{\partial x} \Psi)dx$

$= \- \frac{\hbar}{2mi} ( [x (\Psi^{\*}\frac{\partial\Psi}{\partial x} \- \frac{\partial\Psi^{\*}}{\partial x} \Psi)]\_{\-\infty}^{\infty} $ 
$\- \int\_{\-\infty}^{\infty} (\Psi^{\*}\frac{\partial\Psi}{\partial x} \- \frac{\partial\Psi^{\*}}{\partial x} \Psi)dx )$
$= \frac{\hbar}{2mi}\int\_{\-\infty}^{\infty} (\Psi^{\*}\frac{\partial\Psi}{\partial x} \- \frac{\partial\Psi^{\*}}{\partial x} \Psi)dx$
$= \cdots$
$= \int\_{\-\infty}^{\infty} \Psi^{\*}\frac{\hbar}{mi}\frac{\partial}{\partial x} \Psi dx$
$= \int\_{\-\infty}^{\infty} \Psi^{\*}\frac{p}{m}\Psi dx$
$\equiv \langle v_{x} \rangle $
$= \int\_{\-\infty}^{\infty} \Psi^{\*}v_{x}\Psi dx$

따라서 
$p=\frac{\hbar}{i}\frac{\partial}{\partial x}$, 
$v=\frac{p}{m}$
으로 정의하는 것이 합당하다.

### 에렌페스트 정리(Ehrenfest theorem)
뉴턴의 고전 역학에서 운동량을 시간에 대해 미분하면 무엇인지 알고 있는가?

$$ \frac{dp}{dt} = -\frac{\partial V}{\partial x} $$

운동량을 시간에 대해 미분하면 힘을 얻을 수 있다.

이와 같이 운동량 기댓값의 시간에 대한 미분을 구해보자.

결과로 $ \frac{d\langle p\rangle}{dt} = \langle -\frac{\partial V}{\partial x}\rangle $를 얻을 수 있다.

## 불확정성 원리
### 드 브로이의 공식
입자가 파장 $\lambda$의 이동하는 파동이라 할때, 운동량의 크기는
$p=\frac{h}{\lambda}=\hbar k$, $k=\frac{2\pi}{\lambda} $
로 나타난다.

$\lambda$를 점차 많이 더할 경우 위치는 선명하게 결정되지만, 운동량은 흐트러지게 된다. 

이를 식으로 나타내면 
$ \sigma_{x}\sigma_{p} \geq \frac{\hbar}{2} $
로 나타나고, 동시에 $x$와 $p$를 이보다 더 정확하게 측정하는 것은 물리적으로 불가능하다.

### 일반화된 불확정성 원리
$\sigma_{A}\sigma_{B} \geq &#124; \frac{1}{2i} \langle [A,B] \rangle &#124;$이다. 이때, $[A,B]=AB-BA$, $\sigma_{f}$는 $f$의 표준편차이다.