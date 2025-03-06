---
title: "파동 함수"
excerpt: "파동 함수"
tags: physics quantum
header:
  teaser: https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcQqoGDngbpKU_7jpFv4thAwH03rpQ8HZk7VXCkdFrS0IHbkrjgE
---
# 파동 함수

## 슈뢰딩거 방정식

뉴턴 역학에는 $\vec{F} = m \vec{a}$라는 매우 유명한 지배 방정식이 있습니다. 이는 물리적 힘(전자기력, 마찰력 등)이 가해지면 물체가 가속된다는 의미로 해석할 수 있습니다. 위의 미분 방정식을 풀면 물체의 위치와 속도를 얻을 수 있습니다. 마찬가지로 양자 역학에서는 슈뢰딩거 방정식이 같은 역할을 합니다.

입자의 동적 상태는 파동 ​​함수 $\Psi$에 의해 완전히 지정됩니다.
비상대론적이고, 스핀이 없는 입자의 경우,
$\Psi(r,t)$의 진화는 **슈뢰딩거 방정식**에 의해 지배됩니다. $ i \hbar \frac{\partial \Psi}{\partial t} = - \frac{\hbar^{2}}{2m} \nabla^{2}\Psi + V\Psi $

여기서 $\nabla^{2}f=
\left(
\frac{\partial^{2}}{\partial x^{2}}+
\frac{\partial^{2}}{\partial y^{2}}+
\frac{\partial^{2}}{\partial z^{2}}
\right)f$는 **라플라시안**이라고 하며 $\hbar$는 $\frac{h}{2\pi}$로 $1.054572\times10^{-34} Js$입니다.

### 양자화 규칙

양자 역학에서 고전적으로 측정할 수 있는 모든 것은 연산자가 됩니다.

슈뢰딩거 방정식은 연산자 규칙을 적용해 얻을 수 있습니다.

$E \rightarrow i\hbar\frac{\partial}{\partial t}$

$\vec{p}\rightarrow -i\hbar\vec{\nabla}$, $ p^{2} \rightarrow -\hbar^{2} \nabla^{2} $

$ \vec{r}\rightarrow\vec{r} $

고전적인 보존 시스템에 대한 관계식 $ E=\frac{p^{2}}{2m}+V $에 적용하여 $ i\hbar\frac{\partial}{\partial t}\Psi=\left( -\frac{\hbar^{2}}{2m}\nabla^{2}+V \right)\Psi $를 얻을 수 있습니다.

## 통계적 해석

막스 보른(Born)은 $\Psi$가 **확률 진폭**이라고 말했습니다.

시간 t에서 a와 b 사이에 있는 입자를 찾을 확률을 구하려면 $ \frac{
\int_{a}^{b} {dx \left| \Psi (x,t) \right|^{2}}
}{
\int_{-\infty}^{\infty} {dx \left| \Psi (x,t) \right|^{2}}
} $을 계산하면 됩니다.

### 철학

아인슈타인이 대표한 실재론적 주장은 다음과 같습니다. 객관적 현실이 있습니다. 인과성과 국소성은 보존됩니다. 양자 이론의 통계적 특성은 불완전하다는 것을 의미합니다(숨겨진 변수가 있음).

보어가 대표한 정통(코펜하겐 해석) 주장은 다음과 같습니다. 측정의 통계적 특성은 자연의 근본적인 속성입니다(엄격한 인과성은 없습니다).

불가지론적 주장은 다음과 같습니다. 그러한 형이상학적 질문에 대해 걱정할 필요가 없습니다.

이에 대한 유명한 관용구가 있습니다.
> Shut up and calculate!

다음 질문인 "측정 결과 C 지점에 있다는 것을 보여주기 직전 입자는 어디에 있습니까?"에 대한 각 사람의 답은 다음과 같습니다.

현실주의자: C 지점에 있습니다.

정통주의자: 어디에도 없습니다.

불가지론자: 의미 없는 질문입니다.

비교적 최근의 벨 부등식 실험은 정통주의자 측이 옳다는 것을 보여줍니다.

### 파동 함수의 붕괴
`측정을 바로 반복하면 항상 같은 값이 나옵니다.`

파동 함수는 측정 연산자의 고유 함수로 붕괴됩니다.

## 확률
### 이산 변수

총 개수: $ N=\sum_{j=0}^{\infty} {N(j)} $

$j$의 확률: $ P(j)=\frac{N(j)}{N} $

$j$ 또는 $k$의 확률: $P(j)+P(k)$

합계 규칙: $ \sum_{j=0}^{\infty}P(j)=1 $

중간값 ($j_m$): $ \sum_{j=0}^{j_{m}-1}P(j)=\sum_{j=j_{m}+1}^{\infty}P(j) $

평균: $\left<j\right>=\sum_{j=0}^{\infty}jP(j)$

함수 $f$의 평균/기대값 $j$: $ \left<f(j)\right>=\sum_{j=0}^{\infty}f(j)P(j) $

분산(표준편차): $ \sigma\equiv\sqrt{\left<(j-\left<j\right>)^{2}\right>} = \sqrt{\left<j^{2}\right>-\left<j\right>^{2}} $

/TODO()

## 정규화

## 모멘텀

## 불확정성 원리