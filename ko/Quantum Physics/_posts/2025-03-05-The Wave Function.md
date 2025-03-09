---
title: "파동 함수"
excerpt: 
tags: physics quantum
header:
  teaser: https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcQqoGDngbpKU_7jpFv4thAwH03rpQ8HZk7VXCkdFrS0IHbkrjgE
---
# 파동 함수

## 슈뢰딩거 방정식

고전 역학에서 뉴턴의 운동 방정식 $\vec{F} = m \vec{a}$는 힘과 가속도의 관계를 나타내며, 이를 통해 물체의 움직임을 결정할 수 있습니다. 양자 역학에서는 이에 대응하는 방정식이 바로 **슈뢰딩거 방정식**입니다.

입자의 상태는 **파동 함수** $\Psi$로 완전히 기술되며, 스핀을 고려하지 않는 비상대론적 경우에 대한 시간 의존 슈뢰딩거 방정식은 다음과 같습니다.

$ i \hbar \frac{\partial \Psi}{\partial t} = - \frac{\hbar^{2}}{2m} \nabla^{2}\Psi + V\Psi $

여기서,
- $\hbar = \frac{h}{2\pi} \approx 1.054572\times10^{-34} Js$
- $\nabla^{2} = \left(
\frac{\partial^{2}}{\partial x^{2}}+
\frac{\partial^{2}}{\partial y^{2}}+
\frac{\partial^{2}}{\partial z^{2}}
\right)$: **라플라시안 연산자**

이 방정식을 풀면 특정 계의 양자 상태를 기술하는 파동 함수를 얻을 수 있습니다.

## 양자화 규칙

고전 역학에서 관측 가능한 물리량(에너지, 운동량 등)은 양자 역학에서 연산자로 대체됩니다.

- 에너지: $E \rightarrow i\hbar\frac{\partial}{\partial t}$
- 운동량: $\vec{p} \rightarrow -i\hbar\vec{\nabla}$, $ p^{2} \rightarrow -\hbar^{2} \nabla^{2}$
- 위치: $\vec{r} \rightarrow \vec{r}$

이를 고전적 관계식 $E = \frac{p^2}{2m} + V$에 적용하면 슈뢰딩거 방정식을 얻을 수 있습니다.

## 통계적 해석

막스 보른은 파동 함수 $\Psi$가 확률 진폭(probability amplitude)이며, 그 제곱 $\left&#124; \Psi \right&#124;^{2}$ 이 입자가 특정 위치에 있을 확률 밀도를 나타낸다고 제안했습니다.

입자가 시간 $t$에서 구간 $[a, b]$에 있을 확률은 다음과 같이 계산됩니다.
$ \frac{
\int_{a}^{b} {dx \left| \Psi (x,t) \right|^{2}}
}{
\int_{-\infty}^{\infty} {dx \left| \Psi (x,t) \right|^{2}}
} $

이 해석은 양자 역학의 확률적 본질을 설명하는 핵심 개념입니다.

## 철학적 해석

양자 역학의 해석에는 여러 견해가 있습니다.

- **실재론(아인슈타인):** 입자는 측정 전에 특정한 위치에 존재한다.
- **코펜하겐 해석(보어):** 입자는 측정 전에는 특정한 위치에 존재하지 않는다.
- **불가지론:** 형이상학적 논쟁은 의미가 없으며, 계산에 집중해야 한다.

이와 관련된 유명한 문구로 **"Shut up and calculate!"**가 있습니다.

벨 부등식 실험은 코펜하겐 해석이 실재론적 해석보다 양자역학을 더 잘 설명함을 보여주었습니다.

## 파동 함수의 붕괴

`측정을 바로 반복하면 항상 같은 값이 나옵니다.`

이는 측정이 이루어진 후 파동 함수가 해당 연산자의 고유 상태로 붕괴됨을 의미합니다. 즉, 특정한 상태가 결정된 이후에는 같은 실험을 반복해도 동일한 결과를 얻습니다.

## 확률 개념

### 이산 변수의 확률

- 전체 개수: $N = \sum_{j=0}^{\infty} N(j)$
- 특정 값 $j$가 나올 확률: $ P(j) = \frac{N(j)}{N} $
- $j$ 또는 $k$가 나올 확률: $ P(j) + P(k) $
- 확률의 총합: $ \sum_{j=0}^{\infty} P(j) = 1 $
- 중간값($j_m$): $ \sum_{j=0}^{j_{m}-1} P(j) = \sum_{j=j_{m}+1}^{\infty} P(j) $
- 평균값: $ \langle j \rangle = \sum_{j=0}^{\infty} j P(j) $
- 함수 $f$의 기대값: $ \langle f(j) \rangle = \sum_{j=0}^{\infty} f(j) P(j) $
- 분산(표준편차):
  $ \sigma\equiv\sqrt{\left<(j-\left<j\right>)^{2}\right>} = \sqrt{\left<j^{2}\right>-\left<j\right>^{2}} $

이러한 확률 개념은 양자 역학의 본질적인 확률적 성질을 정량적으로 설명하는 데 사용됩니다.