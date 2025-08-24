---
title: "단일 입자의 운동"
excerpt: 책 기준 2장 내용
tags: physics plasma single particle motion
header:
  teaser: https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcRZplqQsfMnOSyYRjjzr6zXYM-zkt-rm1oeXLK_GKncRFjhT2_n
---

# 2. Single Particle Motions

플라즈마는 수많은 입자들로 구성되어 있으며, 이들 각각은 전기장과 자기장에 의해 영향을 받는다. Maxwell 방정식과 Newton의 법칙에 따르면, 이 입자들은 복잡한 궤적을 따라 움직인다. 그러나 놀랍게도, 평균적으로는 이 궤적이 단순한 형태를 가지며, 그 궤적을 구성하는 요소들—예를 들어 회전 운동, 드리프트 운동 등—은 매우 일반적이다. 이 장에서는 단일 입자가 정적(static) $\mathbf{E}$ 및 $\mathbf{B}$장에서 어떻게 움직이는지를 살펴본다.

## 2.1 Uniform $\mathbf{B}$ Field: The Cyclotron Motion

전하 $q$를 가진 입자가 속도 $\mathbf{v}$로 움직일 때, 입자가 자기장 $\mathbf{B}$ 내에서 받는 힘은 **Lorentz 힘**이다:

$$
\mathbf{F} = q\mathbf{v} \times \mathbf{B}
\tag{2.1}
$$

이때 전기장은 없다고 가정하자. $\mathbf{B} = B\hat{z}$라면, $\mathbf{v} = v_x \hat{x} + v_y \hat{y}$일 경우, $\mathbf{F}$는 $z$축을 중심으로 하는 원운동을 유도한다. 운동 방정식은 다음과 같다:

$$
m \frac{d\mathbf{v}}{dt} = q\mathbf{v} \times \mathbf{B}
\tag{2.2}
$$

이 방정식은 속도 변화가 자기장과 수직인 방향에서만 일어난다는 것을 보여준다. 입자는 $\mathbf{B}$에 수직한 평면에서 반시계방향 또는 시계방향으로 원운동을 하며, 이 회전 운동을 **gyration**, 그 주파수를 **cyclotron frequency**라 부른다:

$$
\Omega = \frac{|q|B}{m}
\tag{2.3}
$$

이때 부호는 방향만을 나타내며, 실제 운동 방향은 $q$의 부호에 따라 달라진다. $q > 0$이면 반시계방향, $q < 0$이면 시계방향이다.

회전 반지름은 다음과 같이 주어진다:

$$
\rho = \frac{v_\perp}{\Omega}
\tag{2.4}
$$

여기서 $v_\perp$는 $\mathbf{B}$에 수직한 성분의 속도이다. 이 반지름은 **Larmor 반지름** 또는 **gyroradius**라고도 하며, 때때로 $r_L$ 또는 $\rho_c$로 표기된다.

운동은 다음과 같이 표현된다:

$$
x(t) = \rho \cos(\Omega t + \phi_0), \quad y(t) = \rho \sin(\Omega t + \phi_0)
\tag{2.5}
$$

여기서 $\phi_0$는 초기 위상이다. $\mathbf{B}$ 방향(즉, $z$축)으로의 속도 성분 $v_z$는 변화하지 않으며, 결과적으로 입자의 궤적은 나선형(spiral path)이 된다.

![Fig. 2.1](https://)  
*그림 2.1: 균일한 자기장에서의 나선 운동*

이 단순한 운동은 플라즈마 물리학의 기본 단위라고 할 수 있다. 대부분의 복잡한 현상은 이러한 나선 운동과 외부 힘에 의한 느린 변화로 구성되어 있다. 전자($q = -e$)와 이온($q = +e$)은 서로 반대 방향으로 회전하게 되며, 이는 많은 현상의 원인이 된다.

---

다음 절부터는 전기장이 포함된 경우와 공간적으로 변하는 자기장에 대한 단일 입자의 움직임을 다룹니다.

## 2.2 Uniform $\mathbf{E}$ and $\mathbf{B}$ Fields: The $\mathbf{E} \times \mathbf{B}$ Drift

이제 공간적으로 일정한 전기장 $\mathbf{E}$가 존재하는 경우를 고려하자. 자기장 $\mathbf{B}$는 여전히 $\hat{z}$ 방향으로 일정하며, 전기장은 $\hat{x}$ 방향으로 일정하다고 하자:

$$
\mathbf{B} = B \hat{z}, \quad \mathbf{E} = E \hat{x}
\tag{2.6}
$$

이때 운동 방정식은 다음과 같다:

$$
m \frac{d\mathbf{v}}{dt} = q\left( \mathbf{E} + \mathbf{v} \times \mathbf{B} \right)
\tag{2.7}
$$

이 문제를 푸는 효율적인 방법은 속도를 다음 두 성분으로 나누는 것이다:

$$
\mathbf{v} = \mathbf{v}_\text{gyro} + \mathbf{v}_d
\tag{2.8}
$$

여기서 $\mathbf{v}_\text{gyro}$는 기존의 나선 운동 성분이고, $\mathbf{v}_d$는 느리게 변하는 평균 속도(drift)이다. 시간이 충분히 경과하면 초기의 나선 운동은 상쇄되고, 입자는 평균적으로 일정한 속도로 이동한다. 이 평균 속도를 **$\mathbf{E} \times \mathbf{B}$ drift**라 하며, 다음과 같이 표현된다:

$$
\mathbf{v}_E = \frac{\mathbf{E} \times \mathbf{B}}{B^2}
\tag{2.9}
$$

이 drift는 다음과 같은 중요한 특징들을 가진다:

1. **전하의 종류에 무관**: $q$에 비례하지 않으므로, 전자와 이온 모두 같은 방향과 속도로 drift한다.
2. **가속이 없는 이동**: 속도가 일정하며, 에너지가 변하지 않는다.
3. **선형 중첩 가능**: 여러 전기장 성분에 대해 drift 속도는 각각의 $\mathbf{E}_i \times \mathbf{B}$를 더한 것과 같다.

이 drift는 plasma 내에서 전체적인 이동을 유발할 수 있으며, 특히 도체 벽을 따라 plasma가 빠르게 움직이도록 만들 수 있다. $\mathbf{v}_E$의 방향은 항상 $\mathbf{E}$와 $\mathbf{B}$에 모두 수직이며, 이는 손으로 벡터곱을 계산해보면 쉽게 알 수 있다.

---

이 절의 drift는 가장 단순한 예시이며, 이후에 다룰 **gradient-B drift**, **curvature drift**, **polarization drift**, **magnetic mirror drift** 등은 이보다 훨씬 더 복잡한 상황을 다룬다. 그럼에도 불구하고, $\mathbf{E} \times \mathbf{B}$ drift는 가장 널리 사용되는 개념이다.

## 2.3 Nonuniform Magnetic Fields: The Magnetic Mirror

이제 $\mathbf{B}$가 일정하지 않은 경우를 살펴보자. 특히 **자기장 강도가 위치에 따라 변하는 경우**, 입자의 운동에 어떤 변화가 생기는지 살펴본다. 이 경우 입자는 자기장의 나선형을 따라 움직이며, 자기장이 점점 강해지는 방향에서는 **반사(reflection)**된다. 이러한 효과를 **magnetic mirror 효과**라 하며, 플라즈마 포획 장치에서 매우 중요하다.

![Fig. 2.2](https://)  
*그림 2.2: magnetic mirror 구성. 양쪽 끝에서 자기장이 강해지면 입자가 반사됨*

입자가 자기장의 나선형을 따라 움직이는 동안, 다음 물리량은 일정하게 유지된다:

1. **총 에너지 보존**:
   $$
   \frac{1}{2} m (v_\parallel^2 + v_\perp^2) = \text{constant}
   \tag{2.10}
   $$
2. **자기 모멘트 보존** (adiabatic invariant):
   $$
   \mu = \frac{mv_\perp^2}{2B} = \text{constant}
   \tag{2.11}
   $$

이 두 조건을 결합하면 다음과 같은 결과를 얻을 수 있다: 입자가 $B$가 점점 커지는 영역으로 이동하면 $v_\perp$는 증가하고 $v_\parallel$는 감소한다. 특정 지점에서 $v_\parallel = 0$이 되면 입자는 반사되어 다시 돌아간다. 이 지점을 **mirror point**라 하며, 다음 조건을 만족해야 한다:

$$
\frac{v_\perp^2}{v_\parallel^2} > \frac{B_{\text{max}}}{B_{\text{min}}} - 1
\tag{2.12}
$$

이 식은 mirror 포획 조건을 나타내며, 입자의 나선이 얼마나 가파르게 감겨야 하는지를 나타낸다.

이러한 magnetic mirror는 Van Allen radiation belt, 태양 코로나, Tokamak 장치의 말단 등에서 자연적 또는 인공적으로 발생한다. 포획된 입자들은 이러한 mirror 영역 안에서 진동 운동을 하며, 상당한 시간 동안 가두어질 수 있다.

## 2.4 Gradient-B and Curvature Drifts

$\mathbf{B}$가 공간적으로 변할 때, 특히 그 크기나 방향이 변할 경우, 입자는 **나선 운동**을 하는 동시에 느린 평균 운동(drift)을 하게 된다. 이 절에서는 두 가지 중요한 drift를 다룬다:

- **Gradient-B drift**: 자기장 크기의 기울기에 의한 drift  
- **Curvature drift**: 자기장 선의 곡률에 의한 drift

이러한 drift는 입자의 평균 운동량 보존, 자기 모멘트 보존, Lorentz 힘에 의해 유도된다.

### Gradient-B Drift

먼저 자기장이 점차 강해지는 방향으로 공간적으로 일정한 기울기를 가진다고 가정하자. 즉, $\mathbf{B} = B(y)\, \hat{z}$처럼 $y$ 방향으로 변한다고 하자. 이 경우, 입자는 한 바퀴 회전하는 동안 $y$ 방향으로 이동하면서, 자기장의 세기가 바뀌는 구간을 경험하게 된다. 그 결과, 궤도 반지름과 회전 속도가 달라지며, 궤적이 대칭이 아니게 되어 순수 회전 외에 느린 **평균 drift**가 발생한다.

이 drift는 다음과 같이 표현된다:

$$
\mathbf{v}_{\nabla B} = \frac{1}{2} \frac{mv_\perp^2}{qB^3} (\mathbf{B} \times \nabla B)
\tag{2.13}
$$

이 drift의 특징은 다음과 같다:

- $v_\perp$에 비례하므로 나선 반경이 클수록 크다.  
- 전자의 경우 ($q = -e$), 이온과 반대 방향으로 drift한다.  
- 전하의 부호에 따라 방향이 결정된다.  

### Curvature Drift

자기장 선이 직선이 아닌 곡선일 경우, 입자는 그 곡선 중심 방향으로 **구심 가속도**를 경험하게 된다. 이때 구심 가속도에 대응하는 **가짜 힘(fictitious force)**이 자기장 선에서 벗어난 방향으로 작용한다. 이 힘이 Lorentz 힘과 결합하여 새로운 drift를 유발한다.

Curvature drift는 다음과 같이 표현된다:

$$
\mathbf{v}_c = \frac{mv_\parallel^2}{qB^2} \frac{\mathbf{R}_c \times \mathbf{B}}{R_c^2}
\tag{2.14}
$$

여기서 $\mathbf{R}_c$는 자기장 선의 곡률 반지름을 나타내며, 방향은 곡률 중심을 향한다. 이 drift는 다음과 같은 특징을 가진다:

- $v_\parallel$의 제곱에 비례하므로, 자기장 선을 따라 빠르게 움직이는 입자일수록 크다.  
- 전자와 이온은 반대 방향으로 drift한다.  
- $\mathbf{R}_c \times \mathbf{B}$ 방향으로 이동한다.  

### 총 Drift 속도

위의 두 drift는 모두 **전기장 없이도 발생하는 비에너지적 drift**이다. 이 두 효과가 동시에 존재할 경우, 평균 drift 속도는 두 drift의 합이다:

$$
\mathbf{v}_d = \mathbf{v}_{\nabla B} + \mathbf{v}_c
\tag{2.15}
$$

이 drift들은 plasma의 **집단적인 전류 흐름**을 유발하며, 자기장 자체를 변화시키는 결과를 낳을 수 있다. 특히 토카막(Tokamak)이나 방사선대에서 입자의 confinement(가두기) 효율과 안정성에 큰 영향을 미친다.

## 2.5 Polarization Drift

이번에는 전기장이 시간에 따라 변하는 경우를 고려하자. $\mathbf{E}(t)$가 시간적으로 변동하지만 공간적으로는 일정하다고 가정하면, 입자는 단순히 $\mathbf{E} \times \mathbf{B}$ drift만 하는 것이 아니라, 전기장의 시간 변화로 인해 **추가적인 가속**을 받게 된다. 이로 인해 새로운 형태의 drift가 발생하는데, 이를 **polarization drift**라 한다.

운동 방정식은 다음과 같다:

$$
m \frac{d\mathbf{v}}{dt} = q\left( \mathbf{E}(t) + \mathbf{v} \times \mathbf{B} \right)
\tag{2.16}
$$

이 방정식에서 $\mathbf{v}$는 다시 다음과 같이 나눌 수 있다:

$$
\mathbf{v} = \mathbf{v}_\text{gyro} + \mathbf{v}_E + \mathbf{v}_p
\tag{2.17}
$$

여기서:

- $\mathbf{v}_\text{gyro}$는 나선 운동 (gyration)
- $\mathbf{v}_E = \frac{\mathbf{E} \times \mathbf{B}}{B^2}$는 평상시의 drift
- $\mathbf{v}_p$는 우리가 관심 갖는 polarization drift

이제 평균 운동을 다루는 관점에서 $\mathbf{v}_\text{gyro}$는 무시하고, 남은 $\mathbf{v}$에 대해 풀어보면, $\mathbf{v}_p$는 다음과 같이 유도된다:

$$
\mathbf{v}_p = \frac{m}{qB^2} \frac{d\mathbf{E}_\perp}{dt}
\tag{2.18}
$$

여기서 $\mathbf{E}_\perp$는 자기장 $\mathbf{B}$에 수직한 성분만 고려한다.

### 특성

- $q$가 분모에 있으므로 **전자의 drift는 이온보다 훨씬 크다**.
- 그러나 $q$가 전류를 계산할 때도 사용되므로, **polarization drift에 의한 전류 밀도**는 다음과 같다:

  $$
  \mathbf{J}_p = n q \mathbf{v}_p = \frac{n m}{B^2} \frac{d\mathbf{E}_\perp}{dt}
  \tag{2.19}
  $$

  이 전류는 $q$에 의존하지 않으며, **species-independent** 하다.

- 이 전류는 Maxwell 방정식의 **변위 전류(displacement current)**와 매우 유사한 형태를 가진다. displacement current는 진공에서 $d\mathbf{E}/dt$에 비례하고, polarization current는 유체 내에서 입자의 관성에 의해 유도된다.

### 물리적 의미

전기장이 시간적으로 증가하면, 입자들이 가속되며 전기장 방향으로 이동한다. 이는 밀도의 국소적 증가를 야기하며, 결과적으로 전하 분리가 발생한다. 그러나 plasma는 이를 허용하지 않으며, Debye 차폐에 의해 전위 변화가 억제된다. 이때 polarization drift는 이러한 전위 변화를 중화시키는 방향으로 작용한다. 즉, plasma는 **중성 상태(quasineutrality)**를 유지하기 위해 polarization current를 통해 응답한다.

이 효과는 특히 **고주파 전자파의 전파**, **압축 파(compressive waves)**, 그리고 **자기 포획 장치의 안정성 분석**에서 중요한 역할을 한다.

<!-- /TODO() -->