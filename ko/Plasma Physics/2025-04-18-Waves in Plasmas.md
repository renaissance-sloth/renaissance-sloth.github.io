---
title: "플라즈마 내부에서의 파동"
excerpt: 책 기준 4장 내용
tags: physics plasma wave
header:
  teaser: https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcRZplqQsfMnOSyYRjjzr6zXYM-zkt-rm1oeXLK_GKncRFjhT2_n
---

# **4 Waves in Plasmas**

## **4.1 Representation of Waves**

파동은 임의의 양이 시간과 공간의 조합에 따라 주기적으로 진동하는 현상이다. 예를 들어 다음과 같은 파동이 있다고 하자:

$$
\phi = \phi_0 \cos(kx - \omega t) \tag{4.1}
$$

여기서:

- $k$는 파수,
- $\omega$는 각진동수,
- $\phi$는 전위나 밀도와 같은 어떤 물리량이다.

상기 표현은 다음의 복소 표현으로도 기술된다:

$$
\phi = \Re \left[ \phi_0 e^{i(kx - \omega t)} \right] \tag{4.2}
$$

파동은 다차원적으로 기술되며, 예를 들어 3차원 파동은 다음과 같다:

$$
\phi = \phi_0 \cos(\mathbf{k} \cdot \mathbf{r} - \omega t) \tag{4.3}
$$

---

## **4.2 Group Velocity**

파동이 주파수 $\omega$에 따라 분산되는 매질에서는 **군속도(group velocity)**가 중요하다. 위상 속도는:

$$
v_p = \frac{\omega}{k} \tag{4.4}
$$

군속도는 다음과 같이 정의된다:

$$
v_g = \frac{d\omega}{dk} \tag{4.5}
$$

이것은 파동군(wave packet)의 속도에 해당하며, 에너지 전달 속도와 관련된다.

---

## **4.3 Plasma Oscillations**

플라즈마는 전자의 집단적 움직임으로 인해 고유 진동을 한다. 이 진동의 기본 형태는 다음과 같은 간단한 운동 방정식으로 기술된다:

$$
m_e \frac{d^2 x}{dt^2} = -e E = -e \left( \frac{e n_0 x}{\varepsilon_0} \right) \tag{4.6}
$$

이는 단진자와 같은 방정식이며, 해는 다음과 같다:

$$
x(t) = x_0 \cos(\omega_p t + \phi) \tag{4.7}
$$

여기서 $\omega_p$는 **플라즈마 진동수(plasma frequency)**로 정의된다:

$$
\omega_p = \sqrt{ \frac{n_0 e^2}{m_e \varepsilon_0} } \tag{4.8}
$$

이는 전자의 집단적인 전기 복원력에 의한 진동으로, $\omega_p$보다 낮은 주파수의 전자기파는 플라즈마 내로 침투하지 못한다.

---

## **4.4 Electron Plasma Waves**

이러한 전자 진동은 전자 밀도의 파동으로 확장되며, 다음과 같은 선형화된 유체 방정식으로 기술할 수 있다:

- 연속 방정식:

$$
\frac{\partial n_1}{\partial t} + n_0 \nabla \cdot \mathbf{v}_1 = 0 \tag{4.9}
$$

- 운동 방정식:

$$
m_e \frac{\partial \mathbf{v}_1}{\partial t} = -e \mathbf{E}_1 - \frac{1}{n_0} \nabla p_1 \tag{4.10}
$$

압력 항을 포함할 경우, 파동의 분산 관계는 다음과 같다:

$$
\omega^2 = \omega_p^2 + 3 k^2 v_{Te}^2 \tag{4.11}
$$

여기서 $v_{Te}$는 전자 열속도이며, 이는 전자 압력의 영향을 포함한다.

---

## **4.5 Sound Waves**

이온은 전자보다 무거우므로, 음파(sound wave)는 주로 이온의 관점에서 기술된다. 전자들은 배경 전하 중성화를 유지하며, 전기장은 무시할 수 있다.

음파의 분산 관계는 다음과 같다:

$$
\omega = k c_s \tag{4.12}
$$

여기서 $c_s$는 이온 음속(ion sound speed)이며, 전자 압력에 의해 결정된다:

$$
c_s = \sqrt{ \frac{K T_e}{m_i} } \tag{4.13}
$$

---

## **4.6 Ion Waves**

보다 정확하게는, 이온 밀도의 작은 변동이 전자 압력과 전기장에 의해 복원되는 파동이다. 이온 유체 방정식을 풀면 음파와 유사한 결과를 얻지만, 감쇠나 이온–전자 간 차이에 따른 효과가 추가된다.

---

## **4.7 Validity of the Plasma Approximation**

파동 문제를 다룰 때도 quasineutrality는 유효한가? 전자 파동의 경우에는 그렇지 않다. 이들은 전자–이온 밀도 차이에 기인하므로 $\rho \ne 0$이다. 하지만 이온 파동이나 저주파 파동에서는 quasineutral 근사가 적용 가능하다.

---

## **4.8 Comparison of Ion and Electron Waves**

전자 파동은 높은 주파수와 짧은 파장을 가지며, $\omega \sim \omega_p$이다. 이온 파동은 낮은 주파수와 긴 파장을 가지며, $\omega \ll \omega_p$이다. 두 파동의 차이는 질량 차이와 전자-이온 동역학의 차이에서 비롯된다.

| 파동 종류         | 주파수 범위       | 파장         | 복원력      |
|------------------|------------------|--------------|-------------|
| Electron plasma wave | $\omega \sim \omega_p$ | 짧음        | 전기장       |
| Ion acoustic wave    | $\omega \ll \omega_p$ | 김          | 전자 압력    |