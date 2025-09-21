---
title: "Perturbation Theory"
excerpt: "'양자물리 및 연습 II' 과목의 6단원 강의입니다."
tags: syllabus physics quantum
header:
  teaser: https://drive.google.com/thumbnail?id=1Qm_zarRZ2x-0ElOGprphzt1zN4FiPnS6&sz=w1000
---

---

# 제6장 섭동 이론 (Perturbation Theory)

## 단열 근사 및 산란 (섭동 이론)

이 자료는 시간에 무관한 섭동 이론(Time-Independent Perturbation Theory)의 기본 방법론, 특히 비축퇴(Nondegenerate) 및 축퇴(Degenerate) 시스템에 이 이론을 적용하는 방법에 대해 설명하고 있습니다.

### 1. 섭동 이론 (Perturbation Theory)의 개요

정확하게 풀 수 없는 해밀토니안 $H$를 다룰 때, 섭동 이론이 적용됩니다. $H$는 **정확히 풀 수 있는 부분 $H_0$**와 **작은 섭동 $H'$**으로 분리됩니다.

$$ H = H_0 + \lambda H' $$

여기서 $\lambda$는 섭동 매개변수로 도입되며, 계산이 끝난 후 $\lambda = 1$로 설정됩니다. 섭동 이론을 적용하기 위해서는 $H'$가 $H_0$에 비해 작아야 합니다. 예를 들어, 수소 원자의 경우 $H_0$에 대한 파동 함수와 에너지 스펙트럼은 이미 정확하게 알려져 있습니다.

파동 함수($\Psi$)와 에너지($E$)는 $\lambda$에 대한 멱급수(power series)로 확장됩니다:

$$ \Psi = \Psi^{(0)} + \lambda \Psi^{(1)} + \lambda^2 \Psi^{(2)} + \dots $$
$$ E = E^{(0)} + \lambda E^{(1)} + \lambda^2 E^{(2)} + \dots $$

### 2. 비축퇴 섭동 이론 (Nondegenerate Perturbation Theory)

$H_0$의 에너지 스펙트럼이 비축퇴(non-degenerate)일 때 적용됩니다.

#### 2.1. 1차 에너지 보정 ($E_n^{(1)}$)

1차 에너지 보정은 다음과 같이 주어집니다. 이는 **교란 해밀토니안($H'$)의 기대값**과 같습니다:

$$ E_n^{(1)} = \langle \Psi_n^{(0)} | H' | \Psi_n^{(0)} \rangle $$

#### 2.2. 2차 에너지 보정 ($E_n^{(2)}$)

2차 에너지 보정은 1차 파동 함수 보정($\Psi_n^{(1)}$)을 활용하여 결정되며, 다음 공식으로 주어집니다:

$$ E_n^{(2)} = \sum_{m \neq n} \frac{|\langle \Psi_m^{(0)} | H' | \Psi_n^{(0)} \rangle|^2}{E_n^{(0)} - E_m^{(0)}} $$

여기서 합산은 $n$ 상태를 제외한 모든 $m$ 상태에 대해 이루어지므로 분모가 0이 되는 발산(divergence)은 발생하지 않습니다.

#### 2.3. 1차 파동 함수 보정 ($\Psi_n^{(1)}$)

1차 보정된 파동 함수 $\Psi_n^{(1)}$는 비섭동 기저 상태($\Psi_m^{(0)}$)의 선형 결합으로 전개될 수 있습니다. 여기서 $m=n$인 항은 제외됩니다. 이 계수 $C_m^{(n)}$는 다음과 같습니다:

$$ C_m^{(n)} = \frac{\langle \Psi_m^{(0)} | H' | \Psi_n^{(0)} \rangle}{E_n^{(0)} - E_m^{(0)}} \quad (m \neq n) $$

### 3. 축퇴 섭동 이론 (Degenerate Perturbation Theory)

$H_0$의 에너지 스펙트럼이 축퇴(degenerate)인 경우, 비축퇴 이론을 사용할 때 분모 $E_n^{(0)} - E_m^{(0)}$가 0이 되어 발산할 수 있습니다. 따라서 축퇴 섭동 이론을 적용해야 합니다.

#### 3.1. "좋은" 비섭동 상태 (Good Unperturbed States)

축퇴 시스템의 경우, 섭동 $H'$이 가해질 때 스펙트럼이 분리(splitting, 또는 축퇴 해소)되는 경우가 많습니다. 축퇴 섭동 이론의 핵심은 섭동이 가해지기 전에 이미 **$H'$를 대각화하는 선형 결합**인 "좋은" 비섭동 상태 $\Psi^{(0)}$를 찾는 것입니다.

가장 간단한 2중 축퇴(Two-Fold Degeneracy) 상태 ($\Psi_A^{(0)}, \Psi_B^{(0)}$가 동일한 $E_0$를 가짐)를 고려하면, 해는 선형 결합 $\Psi^{(0)} = \alpha \Psi_A^{(0)} + \beta \Psi_B^{(0)}$ 형태로 가정됩니다.

#### 3.2. 1차 에너지 보정의 결정

1차 에너지 보정 $E^{(1)}$을 결정하기 위해, $W$ 행렬 요소를 정의합니다:

$$ W_{ij} = \langle \Psi_i^{(0)} | H' | \Psi_j^{(0)} \rangle \quad (i, j = A, B) $$

$E^{(1)}$과 계수 $\alpha, \beta$는 다음 행렬 방정식, 즉 **고유값 방정식(Eigenvalue Equation)**을 만족해야 합니다:

$$ \begin{pmatrix} W_{AA} - E^{(1)} & W_{AB} \\ W_{BA} & W_{BB} - E^{(1)} \end{pmatrix} \begin{pmatrix} \alpha \\ \beta \end{pmatrix} = 0 $$

비자명 해($\alpha, \beta \neq 0$)를 얻기 위해서는 행렬식이 0이어야 합니다 (**세기 방정식(Secular Equation)**). 이 방정식을 풀면 $E^{(1)}$에 대한 2차 방정식을 얻고, 두 개의 근 $E_{+}^{(1)}$와 $E_{-}^{(1)}$을 통해 **에너지 스펙트럼의 분리**를 확인할 수 있습니다.

2중 축퇴의 1차 에너지 보정 $E_{\pm}^{(1)}$의 일반 해는 다음과 같습니다:

$$ E_{\pm}^{(1)} = \frac{1}{2} \left[ (W_{AA} + W_{BB}) \pm \sqrt{(W_{AA} - W_{BB})^2 + 4 |W_{AB}|^2} \right] $$

#### 3.3. 대칭성과 축퇴의 해소 (Lifting of Degeneracy)

만약 어떤 **에르미트 연산자 $A$**가 **$H_0$와 $H'$ 모두와 교환**된다면 ($[A, H_0] = 0$ 및 $[A, H'] = 0$), 섭동이 포함된 후에도 대칭성이 유지됩니다.

이 경우, $\Psi_A^{(0)}$와 $\Psi_B^{(0)}$가 $A$의 고유 함수(eigenfunctions)라면, 섭동 행렬 $W$의 비대각 요소 $W_{AB}$는 0이 됩니다. 따라서 섭동은 기존의 축퇴 상태를 그대로 유지한 채 에너지를 이동시킬 뿐, 해당 대칭성으로 인한 축퇴는 해소되지 않습니다.

### 4. 응용 예시 및 다음 주제

*   **수소 원자의 미세 구조(Fine Structure):** 수소 원자의 미세 구조(상대론적 보정 및 스핀-궤도 결합)는 섭동 $H'$이 매우 작기 때문에 섭동 이론을 적용하여 에너지 스펙트럼의 분리를 예측할 수 있으며, 이는 분광학 실험 결과와 정확히 일치합니다.
*   **다음 강의 주제:** 수소 원자의 미세 구조와 제만 효과(Zeeman effect)와 같은 추가적인 섭동 현상.