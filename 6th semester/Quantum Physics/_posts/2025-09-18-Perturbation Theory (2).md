---
title: "Perturbation Theory (2)"
excerpt: "'양자물리 및 연습 II' 과목의 6단원 강의 (2)입니다."
tags: syllabus physics quantum
header:
  teaser: https://drive.google.com/thumbnail?id=1Qm_zarRZ2x-0ElOGprphzt1zN4FiPnS6&sz=w1000
---

---

## 수소 원자의 미세 구조 (상대론적 및 스핀-궤도 결합 보정)

본 자료는 시간에 무관한 섭동 이론(Time-Independent Perturbation Theory)을 이용하여 수소 원자의 에너지 스펙트럼에 대한 **미세 구조 보정(Fine Structure Correction)**을 계산하는 방법을 다루고 있습니다. 이 보정은 **상대론적 효과**와 **스핀-궤도 결합(Spin-Orbit Coupling)**이라는 두 가지 주요 원인에 의해 발생합니다.

### 1. 상대론적 운동 에너지 보정

전자는 빠르게 움직이므로, 전자의 운동 에너지를 계산할 때 고전적인 공식 $T = p^2/(2m)$ 대신 **상대론적 공식**을 사용해야 합니다.

상대론적 운동 에너지 $T$의 정확한 공식은 다음과 같습니다 (정지 질량 에너지를 뺀 값):
$$ T = \sqrt{p^2 c^2 + m^2 c^4} - m c^2 $$

이 식을 $p \ll mc$ (전자의 운동량 $p$가 $mc$에 비해 매우 작을 때) 조건에서 멱급수(power series)로 전개할 수 있습니다.

$mc$에 비해 $P$가 작으므로 이 양($P/mc$)은 작은 계수입니다. 이 전개를 통해 얻는 결과는 다음과 같습니다:

$$ T \approx \frac{p^2}{2m} - \frac{p^4}{8m^3 c^2} + \dots $$

*   첫 번째 항 $\frac{p^2}{2m}$는 **비상대론적 운동 에너지**입니다.
*   두 번째 항 $\mathbf{H'_R = - \frac{p^4}{8m^3 c^2}}$는 해밀토니안에 대한 **상대론적 보정(Relativistic Correction)** 항으로 간주되며, 이를 섭동 $H'_R$로 사용하여 섭동 이론을 적용합니다,,.

이 섭동 항은 매우 작으며, $H_0$의 비섭동 에너지 스펙트럼($E_n$)에 비해 대략 **$10^{-4}$** 정도의 보정을 제공할 것으로 예상됩니다,. 실제로 $n=1$ 상태에 대해 추정하면, 보정량은 비섭동 에너지에 비해 $10^{-4}$ 정도 차이가 납니다,.

#### 1차 에너지 보정 $E^{(1)}_R$ 계산:

1차 에너지 보정 $E^{(1)}_R$은 비섭동 파동 함수($\Psi^{(0)}_n$)에 대한 섭동 해밀토니안($H'_R$)의 **기대값(expectation value)**으로 주어집니다,:

$$ E_n^{(1)} = \langle \Psi_n^{(0)} | H'_R | \Psi_n^{(0)} \rangle = - \frac{1}{8m^3 c^2} \langle p^4 \rangle $$

이 기대값 계산에는 $p^4$ 연산자가 포함됩니다. 이 계산을 위해 **페인만-헬만 정리(Feynman-Hellmann theorem)**나 **비리얼 정리(Virial theorem)**와 같은 특수한 방법을 사용해야 합니다,.

$E_n^{(1)}$의 최종 결과는 다음과 같이 주어진 에너지 ($E_n$)와 양자수 ($n, l$)의 함수로 표현될 수 있습니다,:

$$ E_n^{(1)} = -\frac{(E_n)^2}{2m c^2} \left[ \frac{4n}{l+1/2} - 3 \right] $$

### 2. 스핀-궤도 결합 (Spin-Orbit Coupling)

두 번째 주요 보정은 **스핀-궤도 결합**입니다. 전자가 핵 주변을 궤도 운동할 때, 양성자(핵)의 관점에서 전자는 자기장을 경험하며, 이 자기장은 전자의 고유 스핀 자기 모멘트($\mu_s$)와 상호작용합니다,.

스핀-궤도 결합 해밀토니안($H'_{SO}$)은 다음과 같이 주어집니다,:

$$ H'_{SO} = \frac{1}{2m^2 c^2} \left( \frac{e^2}{4\pi \epsilon_0} \right) \frac{1}{r^3} \mathbf{S} \cdot \mathbf{L} $$

여기서 $\mathbf{S} \cdot \mathbf{L}$은 스핀 연산자 $\mathbf{S}$와 궤도 각운동량 연산자 $\mathbf{L}$의 내적을 나타냅니다.

#### 1차 에너지 보정 $E^{(1)}_{SO}$ 계산:

$E^{(1)}_{SO}$는 $H'_{SO}$의 기대값으로 주어집니다.

*   **보존되는 양자수:** 섭동 $H'_{SO}$를 포함해도 $L^2$, $S^2$, 그리고 **전체 각운동량** $\mathbf{J} = \mathbf{L} + \mathbf{S}$와 그 $z$ 성분 $J_z$는 $H'_{SO}$와 교환되므로 **좋은 양자수(Good Quantum Numbers)**로 유지됩니다,,,.
*   **$\mathbf{L} \cdot \mathbf{S}$의 값:** $\mathbf{L} \cdot \mathbf{S}$ 연산자는 $\mathbf{J}^2 = (\mathbf{L} + \mathbf{S})^2$로부터 유도될 수 있습니다,.
    $$ \mathbf{L} \cdot \mathbf{S} = \frac{1}{2} (\mathbf{J}^2 - \mathbf{L}^2 - \mathbf{S}^2) $$
    $\Psi^{(0)}_{n, l, j, m_j}$ 상태에서 이 연산자의 고유값은 다음과 같습니다,:
    $$ \langle \mathbf{L} \cdot \mathbf{S} \rangle = \frac{\hbar^2}{2} [j(j+1) - l(l+1) - s(s+1)] $$
    여기서 전자 스핀 $s$는 항상 $1/2$이므로 $s(s+1) = 3/4$입니다,.
*   **$\langle 1/r^3 \rangle$의 기대값:** 이 계산 역시 특별한 기술(예: 페인만-헬만 정리)을 사용하여 얻어지며, 결과는 다음과 같습니다,:
    $$ \left\langle \frac{1}{r^3} \right\rangle = \frac{1}{n^3 a_0^3 l(l+1/2)(l+1)} $$
    여기서 $a_0$는 보어 반경입니다.

이러한 결과를 종합하면, 스핀-궤도 결합의 1차 에너지 보정 $E^{(1)}_{SO}$는 다음과 같습니다:
$$ E^{(1)}_{SO} = \langle H'_{SO} \rangle = \frac{(E_n)^2}{m c^2} \frac{n[j(j+1) - l(l+1) - 3/4]}{l(l+1/2)(l+1)} $$

### 3. 미세 구조의 총 에너지 보정

상대론적 보정 $E^{(1)}_R$과 스핀-궤도 결합 보정 $E^{(1)}_{SO}$를 합산하여 **미세 구조의 1차 에너지 보정($E^{(1)}_{FS}$)**을 얻습니다.

$$ E^{(1)}_{FS} = E^{(1)}_R + E^{(1)}_{SO} $$

두 항을 더하고 $E_n$의 표현식을 이용하여 정리하면, 수소 원자의 에너지 준위에 대한 총 미세 구조 보정은 다음과 같이 $\mathbf{n}$과 $\mathbf{j}$에만 의존하는 형태로 나타납니다,:

$$ E_{n j} = E_n + E^{(1)}_{FS} = E_n \left[ 1 + \frac{\alpha^2}{n^2} \left( \frac{n}{j+1/2} - \frac{3}{4} \right) \right] $$

여기서 $\alpha$는 **미세 구조 상수(Fine Structure Constant)**이며, $\alpha \approx 1/137$로 작은 값입니다,.

*   이 공식은 섭동 보정 후 에너지 준위가 더 이상 궤도 양자수 $l$에 의존하지 않고 주 양자수 $n$과 **총 각운동량 양자수 $j$**에만 의존함을 보여줍니다,.
*   이 계산 결과는 **수소 원자의 에너지 준위 분리(Energy Level Splitting)**를 정밀하게 설명하며, 이는 분광학 실험 결과와 놀라울 정도로 정확하게 일치합니다,,,.

예를 들어, $n=2$ 상태를 고려하면, 미세 구조 보정을 통해 에너지 준위가 분리되어 $j$ 값에 따라 달라지는 스펙트럼을 관찰할 수 있습니다,.