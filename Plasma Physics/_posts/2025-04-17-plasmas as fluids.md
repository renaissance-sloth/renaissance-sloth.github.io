---
title: "유체로서의 플라즈마"
excerpt: 책 기준 3장 내용
tags: physics plasma fluid
header:
  teaser: https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcRZplqQsfMnOSyYRjjzr6zXYM-zkt-rm1oeXLK_GKncRFjhT2_n
---

# **3 Plasmas as Fluids**

## **3.1 Introduction**

플라즈마에서는 앞 장보다 훨씬 더 복잡한 상황이 전개된다. 전기장 $\mathbf{E}$와 자기장 $\mathbf{B}$는 외부에서 주어지는 것이 아니라, 입자들의 위치와 운동에 의해 결정된다. 따라서 우리는 자기일관적인(self-consistent) 문제를 해결해야 하며, 이는 곧 입자들이 궤도를 따라 움직이면서 자기장을 생성하고, 생성된 장이 다시 입자들을 정확히 그 궤도로 움직이게 하는 장–입자 쌍의 조합을 찾아야 함을 의미한다. 그리고 이 모든 과정은 시간에 따라 변하는 동역학적 상황 속에서 이루어져야 한다.

이는 매우 어렵게 들릴 수 있지만, 실제로는 그렇게 어렵지 않다.

플라즈마 밀도가 일반적으로 $10^{18}\,\text{m}^{-3}$ 정도라는 것을 이미 살펴보았다. 만약 이러한 각각의 입자들이 복잡한 궤적을 따라 움직이며, 그 움직임을 모두 추적해야만 플라즈마의 거동을 예측할 수 있다면, 이는 사실상 불가능한 과제가 될 것이다. 다행히도 실제 실험에서 관측되는 플라즈마 현상의 80% 이상은 놀랍게도 매우 단순한 모델로도 설명이 가능하다.

이러한 모델은 유체 역학에서 사용하는 모델로, 개별 입자의 정체성은 무시되고 오직 유체 요소(fluid element)의 집합적 운동만 고려된다. 물론, 플라즈마의 경우 유체가 전하를 띠고 있다는 점에서 일반 유체와는 다르다. 일반적인 유체에서는 빈번한 충돌이 유체 요소 내의 입자들을 함께 움직이게 만들지만, 충돌이 적은 플라즈마에서도 이러한 유체 모델이 유효하다는 점은 매우 흥미롭다. 우리는 그 이유를 곧 살펴보게 될 것이다.

이 책의 대부분은 이러한 플라즈마 유체 이론에서 도출할 수 있는 결과들에 중점을 두고 있다. 보다 정교한 접근법인 **kinetic theory**는 수학적으로 훨씬 복잡하며, 이 입문서에서는 다루기에 적절치 않다. **kinetic theory**에 대한 소개는 7장에서 다룬다.

일부 플라즈마 문제의 경우, **fluid theory**나 **kinetic theory**만으로는 설명이 불가능하다. 이 경우에는 개별 입자의 궤적을 직접 추적하는 귀찮은 과정을 거쳐야 한다. 현대의 컴퓨터는 이러한 계산을 수행할 수 있으며, 3차원 공간에서 약 $10^6$개의 입자의 위치와 속도 성분을 저장할 수 있는 메모리를 가진다. 이러한 시뮬레이션은 실험과 이론 사이의 격차를 메우는 데 중요한 역할을 한다.

---

## **3.2 Relation of Plasma Physics to Ordinary Electromagnetics**

### **3.2.1 Maxwell’s Equations**

**진공 내에서의 Maxwell 방정식:**

$$
\nabla \cdot \mathbf{E} = \frac{\sigma}{\varepsilon_0} \tag{3.1}
$$

$$
\nabla \cdot \mathbf{B} = 0 \tag{3.2}
$$

$$
\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t} \tag{3.3}
$$

$$
\nabla \times \mathbf{B} = \mu_0 \mathbf{j} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t} \tag{3.4}
$$

**매질 내에서의 Maxwell 방정식:**

$$
\nabla \cdot \mathbf{D} = \sigma \tag{3.5}
$$

$$
\nabla \cdot \mathbf{B} = 0 \tag{3.6}
$$

$$
\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t} \tag{3.7}
$$

$$
\nabla \times \mathbf{H} = \mathbf{j} + \frac{\partial \mathbf{D}}{\partial t} \tag{3.8}
$$

$$
\mathbf{D} = \varepsilon \mathbf{E},\quad \mathbf{B} = \mu \mathbf{H} \tag{3.9–3.10}
$$

여기서 $\sigma$와 $\mathbf{j}$는 “자유” 전하 밀도 및 전류 밀도를 의미한다. 유전체의 분극(polarization) 및 자화(magnetization)로부터 발생하는 “결합된” 전하 및 전류 밀도는 $\mathbf{D}$와 $\mathbf{H}$ 정의에 포함되어 있다. 플라즈마에서는 이온과 전자가 이러한 “결합된” 전하 및 전류의 역할을 한다. 그러나 이러한 전하들은 복잡하게 움직이므로, 그 효과를 두 개의 상수 $\varepsilon$ 및 $\mu$로 대체하는 것은 실질적으로 불가능하다.

따라서 플라즈마 물리학에서는 일반적으로 진공 방정식 (3.1)–(3.4)를 사용하며, 여기서 $\sigma$와 $\mathbf{j}$는 외부 및 내부의 모든 전하 및 전류를 포함한다.

우리는 진공 방정식에서 $\mathbf{D}$와 $\mathbf{H}$ 대신 $\mathbf{E}$와 $\mathbf{B}$를 사용한다. 이는 전하가 받는 힘 $q\mathbf{E}$, 전류가 받는 힘 $\mathbf{j} \times \mathbf{B}$가 $\mathbf{E}$ 및 $\mathbf{B}$에 의존하기 때문이다. 따라서 $\varepsilon_0$와 $\mu_0$만을 사용하여 설명이 가능하다면 $\mathbf{D}$와 $\mathbf{H}$를 도입할 필요가 없다.

## **3.2.2 Classical Treatment of Magnetic Materials**

플라즈마 내에서 각 회전 입자는 자기 모멘트(magnetic moment)를 가지므로, 직관적으로는 플라즈마를 투자율 $\mu_m$을 가지는 자성 물질로 간주하는 것이 자연스러워 보일 수 있다. (여기서 $\mu$는 단열 불변량 $\mu$와 구별하기 위해 $\mu_m$으로 표기함)

그러나 실제로는 그렇게 하지 않으며, 왜 그런지를 설명하기 위해 일반적인 자성 물질의 취급 방식을 복습해 보자.

예를 들어, 철과 같은 강자성체는 자기 모멘트 $\mu_i$를 가지는 도메인(domain)들로 구성되어 있으며, 이들은 단위 부피당 다음과 같은 전체 자화(magnetization)를 유도한다:

$$
\mathbf{M} = \sum_i \mu_i \tag{3.11}
$$

이는 다음과 같은 결합 전류 밀도(bound current density)를 유도한다:

$$
\mathbf{j}_b = \nabla \times \mathbf{M} \tag{3.12}
$$

진공 Maxwell 방정식 (3.4)에 이 결합 전류 및 외부 전류 $\mathbf{j}_f$를 포함시키면:

$$
\nabla \times \mathbf{B} = \mu_0 (\mathbf{j}_f + \mathbf{j}_b) + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t} \tag{3.13}
$$

우리는 이를 다음과 같은 간단한 형태로 표현하고 싶다:

$$
\nabla \times \mathbf{H} = \mathbf{j}_f + \frac{\partial \mathbf{D}}{\partial t} \tag{3.14}
$$

이를 위해 $\mathbf{j}_b$를 $\mathbf{H}$의 정의에 포함시키고, 다음과 같이 정의한다:

$$
\mathbf{B} = \mu_0 (\mathbf{H} + \mathbf{M}) \tag{3.15}
$$

$\mathbf{M}$이 $\mathbf{B}$ 혹은 $\mathbf{H}$에 비례한다고 가정하면,

$$
\mathbf{M} = \chi_m \mathbf{H} \tag{3.16}
$$

여기서 $\chi_m$은 자기 감수율(magnetic susceptibility)이며, 이에 따라:

$$
\mathbf{B} = \mu_0 (1 + \chi_m) \mathbf{H} = \mu_m \mathbf{H} \tag{3.17}
$$

이와 같은 $\mathbf{B}$와 $\mathbf{H}$ 간의 간단한 선형 관계는 (3.16)처럼 $\mathbf{M}$이 선형일 때만 가능하다.

하지만 플라즈마에서는 각 입자가 자기 모멘트 $\mu_\alpha$를 가지며, $\mathbf{M}$은 1 m³ 내의 이들 $\mu_\alpha$의 합으로 표현된다. 이 경우 $\mathbf{M}$과 $\mathbf{H}$ 사이의 관계는 더 이상 선형이 아니므로, $\mathbf{B} = \mu_m \mathbf{H}$ 형태로 기술할 수 없으며, 따라서 플라즈마를 자성 매질로 간주하는 것은 실용적이지 않다.

---

## **3.2.3 Classical Treatment of Dielectrics**

단위 부피당 분극(P)은 개별 쌍극자의 전기 모멘트 $p_i$들의 합이다. 이는 다음과 같은 결합 전하 밀도를 생성한다:

$$
\sigma_b = -\nabla \cdot \mathbf{P} \tag{3.18}
$$

진공 Maxwell 방정식 (3.1)은 자유 전하 $\sigma$와 결합 전하 $\sigma_b$를 모두 포함해야 하며:

$$
\nabla \cdot \mathbf{E} = \frac{1}{\varepsilon_0} (\sigma + \sigma_b) \tag{3.19}
$$

우리는 이를 다음과 같은 간단한 형태로 쓰기를 원한다:

$$
\nabla \cdot \mathbf{D} = \sigma \tag{3.20}
$$

이를 위해 다음과 같이 정의한다:

$$
\mathbf{D} = \varepsilon_0 \mathbf{E} + \mathbf{P} \tag{3.21}
$$

$\mathbf{P}$가 $\mathbf{E}$에 선형 비례하면:

$$
\mathbf{P} = \chi_e \varepsilon_0 \mathbf{E} \tag{3.22}
$$

따라서 유전율 $\varepsilon$은 다음과 같이 주어진다:

$$
\varepsilon = \varepsilon_0 (1 + \chi_e) \tag{3.23}
$$

이러한 관계 (3.22)는 플라즈마에서도 유효할 가능성이 있으며, 따라서 우리는 플라즈마의 $\varepsilon$에 대한 표현을 유도해볼 수 있다.

---

## **3.2.4 The Dielectric Constant of a Plasma**

2.5절에서 살펴본 바와 같이, 시간에 따라 변화하는 전기장 $\mathbf{E}$는 분극 전류 $\mathbf{j}_p$를 유도하며, 이는 다시 연속 방정식을 통해 다음과 같은 분극 전하를 유도한다:

$$
\sigma_p = -\int \nabla \cdot \mathbf{j}_p \, dt \tag{3.24}
$$

이것은 식 (3.18)의 대응 관계로 볼 수 있다. 그러나 앞서 논의한 바와 같이, 시간 변화가 없는 전기장에서는 플라즈마 내에서 분극 효과가 발생하지 않는다.

$\sigma_p$보다는 $\mathbf{j}_p$에 대한 명확한 표현이 존재하므로, 우리는 Maxwell 방정식 중 다음을 사용하여 접근한다:

$$
\nabla \times \mathbf{B} = \mu_0 \mathbf{j} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t} \tag{3.25}
$$

이를 다음과 같은 형태로 쓰고자 한다:

$$
\nabla \times \mathbf{B} = \mu_0 \varepsilon \frac{\partial \mathbf{E}}{\partial t} \tag{3.26}
$$

이를 위해 다음과 같이 정의하면 된다:

$$
\mathbf{j} = \varepsilon_0 (\varepsilon - 1) \frac{\partial \mathbf{E}}{\partial t} \tag{3.27}
$$

식 (2.67)에서의 $\mathbf{j}_p$를 사용하면:

$$
\varepsilon = 1 - \frac{\omega_p^2}{\omega^2} \tag{3.28}
$$

이는 횡방향 운동에 대한 저주파 플라즈마 유전율이다. 이 식은 $\omega \ll \omega_c$이고, $\mathbf{E} \perp \mathbf{B}$인 경우에만 유효하다. 일반적인 경우에 대한 $\varepsilon$의 표현은 훨씬 복잡하며, 한 페이지에 담기 어렵다.

플라즈마 밀도가 낮을수록 ($\rho \to 0$), $\varepsilon$은 진공값인 1로 수렴한다. 또한 $B \to \infty$일 때에도 $\varepsilon \to 1$이 되는데, 이는 분극 drift $\mathbf{v}_p$가 0이 되어 입자가 횡방향 전기장에 반응하지 않기 때문이다. 실험실 플라즈마에서는 일반적으로 식 (3.28)의 두 번째 항이 1보다 훨씬 크므로, 플라즈마 입자들이 생성하는 전기장은 외부 전기장을 크게 왜곡시킨다. 유전율이 큰 플라즈마는 교류 전기장을 차폐하며, 이는 $\lambda_D$가 작은 경우 정전기장을 차폐하는 현상과 유사하다.

## **3.3 The Fluid Equation of Motion**

Maxwell 방정식은 주어진 플라즈마 상태에 대해 $\mathbf{E}$와 $\mathbf{B}$를 알려준다. 자기일관적인 문제를 풀기 위해서는 $\mathbf{E}$와 $\mathbf{B}$에 대한 플라즈마의 반응을 기술하는 방정식이 추가로 필요하다. 유체 근사에서는 플라즈마를 여러 종류의 입자 종(species)들로 구성된 상호침투 유체로 간주한다. 가장 간단한 경우로 하나의 이온 종만 있다고 가정하면, 양전하를 가진 이온 유체와 음전하를 가진 전자 유체 각각에 대해 두 개의 운동 방정식이 필요하다. 부분 이온화된 기체의 경우, 중성 원자에 대한 유체 방정식도 추가되어야 한다. 중성 유체는 충돌을 통해 이온 및 전자와 상호작용하며, 전자와 이온 유체는 충돌이 없어도 서로 생성하는 $\mathbf{E}$ 및 $\mathbf{B}$장을 통해 상호작용한다.

---

### **3.3.1 The Convective Derivative**

단일 입자에 대한 운동 방정식은 다음과 같다:

$$
m\frac{d\mathbf{v}}{dt} = q(\mathbf{E} + \mathbf{v} \times \mathbf{B}) \tag{3.29}
$$

우선 충돌과 열운동이 없다고 가정하자. 이 경우 유체 요소 내의 모든 입자는 함께 이동하며, 입자의 평균 속도 $\mathbf{u}$는 개별 속도 $\mathbf{v}$와 같다. 양변에 밀도 $n$을 곱하면:

$$
mn\frac{d\mathbf{u}}{dt} = qn(\mathbf{E} + \mathbf{u} \times \mathbf{B}) \tag{3.30}
$$

그러나 이 형태는 실제로 사용하기에 불편하다. (3.29)의 시간 도함수는 입자 위치에서 평가되는데, 우리는 고정된 위치에서 유체 방정식을 다루고 싶기 때문이다.

예를 들어 커피에 떠 있는 크림 한 방울을 유체 요소로 생각해보자. 커피를 휘저으면 이 방울은 가늘어지다가 사라지고 만다. 반면 컵 안의 특정 위치에 고정된 유체 요소는, 입자들이 끊임없이 들어오고 나가더라도 정체성을 유지한다.

1차원 $x$ 공간에서 유체의 어떤 성질 $G(x, t)$에 대해 유체와 함께 움직이는 기준계에서의 변화율은 다음과 같다:

$$
\frac{dG}{dt} = \frac{\partial G}{\partial t} + u \frac{\partial G}{\partial x} \tag{3.31}
$$

3차원으로 일반화하면:

$$
\frac{dG}{dt} = \frac{\partial G}{\partial t} + (\mathbf{u} \cdot \nabla) G \tag{3.32}
$$

이것이 **convective derivative**이며, $D G / D t$로도 표기된다. $(\mathbf{u} \cdot \nabla)$는 스칼라 미분 연산자이다. 부호로 인해 혼란을 줄 수 있으므로 간단한 예시들을 들어 설명한다.

#### 예시 1: 온수기에서의 온도 변화

온수기 안의 유체 요소가 위로 움직이면서 가열될 수 있다. 동시에 paddle wheel이 바닥의 찬 물을 끌어올리면 온도가 감소한다. 이 경우:

$$
\frac{dT}{dt} = \frac{\partial T}{\partial t} + u_x \frac{\partial T}{\partial x} \tag{3.33}
$$

#### 예시 2: 하구 근처의 염도 변화

하천 입구에서는 상류 방향으로 염도 구배가 존재하고, 밀물 시에는 염도 계면이 상류로 이동한다:

$$
\frac{dS}{dt} = \frac{\partial S}{\partial t} + u_x \frac{\partial S}{\partial x} \tag{3.34}
$$

#### 예시 3: 고속도로 입구에서의 교통 밀도 변화

차량 운전자는 도로에 가까워질수록 밀도가 높아짐을 느낀다. 이는 $\frac{dG}{dt}$ 항이다. 한편, 주변 도로에서 유입되는 차량도 밀도를 증가시키며, 이는 $\frac{\partial G}{\partial t}$ 항에 해당한다.

플라즈마의 경우 $G = \mathbf{u}$로 두고 식 (3.30)을 다음과 같이 쓴다:

$$
mn\left( \frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla) \mathbf{u} \right) = qn(\mathbf{E} + \mathbf{u} \times \mathbf{B}) \tag{3.35}
$$

---

### **3.3.2 The Stress Tensor**

열운동을 고려할 경우, 식 (3.35)의 우변에는 압력력이 추가되어야 한다. 이는 입자들이 유체 요소 안팎으로 무작위로 이동하면서 생기는 효과로, 단일 입자 운동 방정식에는 나타나지 않는다.

예를 들어 $(x_0, y, z)$에 중심을 둔 유체 요소 $\Delta x \Delta y \Delta z$를 생각하자. 입자들이 $x$ 방향으로 운동할 때, 한쪽 면 A에서 들어오고 다른 면 B에서 나가는 입자들의 운동량 차이를 계산하면 다음과 같다:

$$
\Delta P_x = - \frac{\partial}{\partial x} \left( \frac{1}{3} mn \langle v_r^2 \rangle \right) \Delta x \Delta y \Delta z \tag{3.38}
$$

이때 $\langle v_r^2 \rangle = \frac{kT}{m}$이므로, 압력은 다음과 같이 정의된다:

$$
p \equiv \frac{1}{3} mn \langle v_r^2 \rangle = nkT \tag{3.42}
$$

따라서 압력 구배력은 다음과 같다:

$$
\mathbf{F}_p = -\nabla p \tag{3.43}
$$

전체 유체 운동 방정식은 다음과 같다:

$$
mn\left( \frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla) \mathbf{u} \right) = qn(\mathbf{E} + \mathbf{u} \times \mathbf{B}) - \nabla p \tag{3.44}
$$

---

### **3.3.3 Collisions**

중성 가스가 존재하면, 하전 유체는 그와의 충돌을 통해 운동량을 교환한다. 평균 자유시간이 $\tau$라면, 이로 인한 힘은 대략 $-\frac{mn}{\tau}(\mathbf{u} - \mathbf{u}_0)$로 나타낼 수 있다.

이를 고려한 일반화된 방정식은 다음과 같다:

$$
mn\left( \frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla) \mathbf{u} \right) = qn(\mathbf{E} + \mathbf{u} \times \mathbf{B}) - \nabla \cdot \mathbf{P} - \frac{mn}{\tau}(\mathbf{u} - \mathbf{u}_0) \tag{3.47}
$$

---

### **3.3.4 Comparison with Ordinary Hydrodynamics**

일반 유체는 다음의 Navier–Stokes 방정식을 따른다:

$$
\rho \left( \frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla) \mathbf{u} \right) = -\nabla p + \mu \nabla^2 \mathbf{u} \tag{3.48}
$$

이것은 (3.47)과 거의 동일하며, $\mathbf{E}, \mathbf{B}$ 항이 없다는 점과 단일 종이라는 점만이 다르다. 두 식이 동일하다는 점은 **fluid theory**가 실제로 플라즈마를 기술할 수 있음을 나타낸다.

다만, 유체 이론은 맥스웰 분포를 가정한 평균값 $\langle v_r^2 \rangle$에만 의존하므로, 분포가 맥스웰 형태와 완전히 일치하지 않아도 유효하다.

### **3.3.5 Equation of Continuity**

물질 보존 법칙은, 어떤 부피 $V$ 내의 전체 입자 수 $N$이 오직 경계면 $S$를 통한 플럭스에 의해만 변할 수 있다는 사실을 말한다. 입자 플럭스 밀도는 $n\mathbf{u}$이므로, 발산 정리를 이용하면:

$$
\frac{d}{dt} \int_V n\, dV = -\int_S n\mathbf{u} \cdot d\mathbf{S} = -\int_V \nabla \cdot (n\mathbf{u})\, dV \tag{3.49}
$$

임의의 $V$에 대해 성립해야 하므로, 적분 내부항이 같아야 한다:

$$
\frac{\partial n}{\partial t} + \nabla \cdot (n\mathbf{u}) = 0 \tag{3.50}
$$

각 입자 종마다 하나씩의 연속 방정식이 존재한다. 입자의 생성 또는 소멸이 있을 경우, 그 항은 우변에 추가된다.

---

### **3.3.6 Equation of State**

방정식 집합을 닫기 위해 하나의 관계가 더 필요하다. 이는 압력 $p$과 밀도 $n$을 잇는 열역학적 상태 방정식으로, 다음과 같이 표현할 수 있다:

$$
p = C n^\gamma \tag{3.51}
$$

여기서 $C$는 상수이며, $\gamma = C_p / C_v$는 비열 비이다. 따라서 압력 구배는 다음과 같다:

$$
\nabla p = \gamma C n^{\gamma - 1} \nabla n \tag{3.52}
$$

등온 압축인 경우 $\gamma = 1$이고, 단열 압축인 경우 $\gamma > 1$이다. 자유도 수 $N$에 대해:

$$
\gamma = \frac{N + 2}{N} \tag{3.53}
$$

상태 방정식이 유효하려면 열전도 효과가 무시될 수 있을 정도로 작아야 한다. 이는 일반적으로 $\mathbf{B}$에 수직한 방향에서 더 잘 만족되며, 대부분의 기본적인 현상들은 식 (3.51)의 조잡한 가정만으로도 잘 설명된다.

---

### **3.3.7 The Complete Set of Fluid Equations**

단순화를 위해, 플라즈마가 이온과 전자 두 종으로만 이루어졌다고 하자. 전하 및 전류 밀도는 다음과 같다:

$$
\rho = q_i n_i + q_e n_e,\quad \mathbf{J} = q_i n_i \mathbf{v}_i + q_e n_e \mathbf{v}_e \tag{3.54}
$$

단일 입자 운동은 고려하지 않으므로, 유체 속도를 $\mathbf{u}$ 대신 $\mathbf{v}$로 표기한다. 충돌과 점성 효과는 무시한다. 다음의 방정식들이 전체 방정식 집합을 이룬다:

- Maxwell 방정식:

$$
\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0} \tag{3.55}
$$

$$
\nabla \cdot \mathbf{B} = 0 \tag{3.56}
$$

$$
\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t} \tag{3.57}
$$

$$
\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t} \tag{3.58}
$$

- 운동 방정식 (각 종별로 하나씩):

$$
m_i n_i \left( \frac{\partial \mathbf{v}_i}{\partial t} + \mathbf{v}_i \cdot \nabla \mathbf{v}_i \right) = q_i n_i (\mathbf{E} + \mathbf{v}_i \times \mathbf{B}) - \nabla p_i \tag{3.59}
$$

$$
m_e n_e \left( \frac{\partial \mathbf{v}_e}{\partial t} + \mathbf{v}_e \cdot \nabla \mathbf{v}_e \right) = q_e n_e (\mathbf{E} + \mathbf{v}_e \times \mathbf{B}) - \nabla p_e \tag{3.60}
$$

- 연속 방정식 (각 종별로 하나씩):

$$
\frac{\partial n_i}{\partial t} + \nabla \cdot (n_i \mathbf{v}_i) = 0,\quad \frac{\partial n_e}{\partial t} + \nabla \cdot (n_e \mathbf{v}_e) = 0 \tag{3.61}
$$

미지수는 16개: $n_i$, $n_e$, $p_i$, $p_e$, $\mathbf{v}_i$, $\mathbf{v}_e$, $\mathbf{E}$, $\mathbf{B}$. 각 벡터는 3성분이므로, 총 16개의 스칼라 미지수가 존재한다.

위 방정식들은 18개의 스칼라 방정식처럼 보이지만, 실제로는 (3.55)와 (3.57)이 (3.58)과 (3.56)의 발산을 통해 유도되므로 중복된다. 따라서 정확히 16개의 독립 방정식으로 16개의 미지수를 자기일관적으로 결정할 수 있다.

---

## **3.4 Fluid Drifts Perpendicular to B**

유체 요소는 많은 개별 입자로 구성되어 있으므로, 개별 입자의 guiding center drift가 있다면 유체에도 수직 drift가 존재할 것으로 예상할 수 있다. 그러나 압력 구배항 $\nabla p$는 유체 방정식에만 나타나므로, 입자들은 갖지 않지만 유체 요소는 갖는 drift가 있다.

각 입자 종에 대해:

$$
0 = q n (\mathbf{E} + \mathbf{v} \times \mathbf{B}) - \nabla p \tag{3.62}
$$

이 식에서 시간 변화 항은 무시할 수 있는 경우가 많고, $m n \frac{d\mathbf{v}}{dt}$ 항도 무시한다고 하자. $\mathbf{E}$와 $\mathbf{B}$는 일정하지만 $n$과 $p$에는 구배가 존재한다고 가정한다.

$\mathbf{B}$와 양변의 벡터곱을 취하면:

$$
\mathbf{v} = \frac{\mathbf{E} \times \mathbf{B}}{B^2} + \frac{\mathbf{B} \times \nabla p}{q n B^2} \tag{3.63}
$$

즉:

- **$E \times B$ drift**:

$$
\mathbf{v}_E = \frac{\mathbf{E} \times \mathbf{B}}{B^2} \tag{3.64}
$$

- **Diamagnetic drift**:

$$
\mathbf{v}_D = \frac{\mathbf{B} \times \nabla p}{q n B^2} \tag{3.65}
$$

등온 플라즈마에서 식 (3.52)를 적용하면:

$$
\mathbf{v}_D = \frac{K T}{q B} \frac{\mathbf{B} \times \nabla n}{n B} \tag{3.66}
$$

Q-머신의 실험적 조건에서는 자주 다음 형태로 사용된다:

$$
\mathbf{v}_{De} = -\frac{K T_e}{e B} \frac{1}{n} \frac{dn}{dr},\quad \mathbf{v}_{Di} = \frac{K T_i}{e B} \frac{1}{n} \frac{dn}{dr} \tag{3.67}
$$

크기는 다음과 같이 쉽게 계산된다:

$$
|\mathbf{v}_D| = \frac{K T}{q B \Lambda} \tag{3.68}
$$

여기서 $\Lambda = |n' / n|^{-1}$은 밀도 구배 스케일이다.

## **3.5 Fluid Drifts Parallel to B**

$\mathbf{B}$에 수직한 drift만이 존재하는 것은 아니다. 유체 요소가 $\mathbf{B}$를 따라 압력 구배를 가지는 경우에는 수직 drift 없이 단순히 자기장 방향으로 가속된다. 단일 입자와 달리, 유체는 압력 구배로 인해 $\mathbf{B}$ 방향으로 가속될 수 있으며 이는 drift가 아니다.

식 (3.44)의 좌변에 대해 $d/dt = \partial/\partial t + (\mathbf{u} \cdot \nabla)$ 형태를 전개하면, 이론적으로 $\mathbf{B}$ 방향 속도를 시간에 따라 구할 수 있다. 그러나 그 정확한 해는 일반적으로 복잡하다.

---

## **3.6 The Plasma Approximation**

지금까지의 전개에서 우리는 일반적인 Maxwell 방정식을 사용했으며, 전기장 $\mathbf{E}$를 구하기 위해 Gauss 법칙인 $\nabla \cdot \mathbf{E} = \rho/\varepsilon_0$를 사용했다.

그러나 실험실 플라즈마나 자연 플라즈마에서는 **quasineutrality**, 즉 $\rho \approx 0$인 근사가 매우 잘 성립한다. 즉, $n_e \approx Z n_i$이므로 $\nabla \cdot \mathbf{E} \approx 0$이다.

이것을 **plasma approximation**이라고 부르며, 대부분의 유체 해석에서 유용하다. 다만, 가장자리 효과나 전기 이중층(electric double layer), sheath 영역 등에서는 $\rho \ne 0$이고 정전기장이 존재하므로, 그때는 Poisson 방정식을 풀어야 한다.