---
title: "Identical particles - Lecture note"
excerpt: "'양자물리 및 연습 II' 과목의 5단원 강의 자료입니다."
tags: syllabus physics quantum
header:
  teaser: https://drive.google.com/thumbnail?id=1Qm_zarrZ2x-0ElOGprphzt1zN4FiPnS6&sz=w1000
---

### **Chap 5. 동일 입자**

1.  두 입자 시스템 (Two-Particle Systems)
2.  원자 (Atoms)
3.  고체 (Solids)
4.  양자 통계 역학 (Quantum Statistical Mechanics)

***

**동일한 물리적 속성을 가진 두 입자는 동등하다 (equivalent)**.
이들은 동일한 처리를 받을 때 동일하게 행동한다.

*   **고전 역학(CM):** 동등 입자는 **구별 가능(distinguishable)**하다. 왜냐하면 각 입자를 항상 추적할 수 있기 때문이다.
*   **양자 역학(QM):** 동등 입자는 **구별 불가능(indistinguishable)**하다. 왜냐하면 불확정성 원리 때문에 각 입자를 항상 추적할 수 없기 때문이다.

**구별 불가능한 입자를 동일 입자(identical)**라고 부른다.

***

### **5.1. 두 입자 시스템 (Two-Particle Systems)**

두 입자 상태: $\Psi(\mathbf{r}_1, \mathbf{r}_2, t)$

슈뢰딩거 방정식:
$i\hbar \frac{\partial \Psi}{\partial t} = H \Psi$

해밀턴ian:
$H = -\frac{\hbar^2}{2m_1}\nabla_1^2 - \frac{\hbar^2}{2m_2}\nabla_2^2 + V(\mathbf{r}_1, \mathbf{r}_2)$

$\|\Psi(\mathbf{r}_1, \mathbf{r}_2, t)\|^2 d^3r_1 d^3r_2 \propto$ 입자 1과 2를 각각 $\mathbf{r}_1$ 및 $\mathbf{r}_2$ 주변의 $d^3r_1$ 및 $d^3r_2$ 내에서 찾을 확률.

정규화 (Normalization):
$\int d^3r_1 \int d^3r_2 \|\Psi(\mathbf{r}_1, \mathbf{r}_2, t)\|^2 = 1$

$V = V(\mathbf{r}_1, \mathbf{r}_2) \implies \Psi(\mathbf{r}_1, \mathbf{r}_2, t) = \psi(\mathbf{r}_1, \mathbf{r}_2) \exp \left( -\frac{i}{\hbar} E t \right)$

$H \psi(\mathbf{r}_1, \mathbf{r}_2) = E \psi(\mathbf{r}_1, \mathbf{r}_2)$

문제 5.1을 읽고, 문제 5.3을 풀어라.

***

### **5.1.1. 보손과 페르미온 (Bosons & Fermions)**

상태 $a$와 $b$에 있는 구별 가능한 입자 1과 2:
$\psi(\mathbf{r}_1, \mathbf{r}_2) = \psi_a(\mathbf{r}_1) \psi_b(\mathbf{r}_2)$

1과 2가 구별 불가능한 (동일한) 경우:
$\psi_{\pm}(\mathbf{r}_1, \mathbf{r}_2) = A [\psi_a(\mathbf{r}_1) \psi_b(\mathbf{r}_2) \pm \psi_b(\mathbf{r}_1) \psi_a(\mathbf{r}_2)]$
여기서 **+는 보손(bosons)**에 해당하고, **-는 페르미온(fermions)**에 해당한다.

**스핀 통계 정리 (Spin statistics theorem):**
*   **정수 스핀 (Integer spin)** $\to$ **보손 (bosons)**: **대칭 (Symmetric)**
*   **반정수 스핀 (Half-integer spin)** $\to$ **페르미온 (fermions)**: **반대칭 (Anti-symm)**

$\psi_-(\mathbf{r}_1, \mathbf{r}_2) = A [\psi_a(\mathbf{r}_1) \psi_a(\mathbf{r}_2) - \psi_a(\mathbf{r}_1) \psi_a(\mathbf{r}_2)] = 0$

$\therefore$ 두 페르미온은 동일한 상태를 차지할 수 없다 (**파울리 배타 원리 (Pauli exclusion principle)**).

***

### **교환 연산자 (Exchange Operator)**

교환 연산자 (Exchange operator): $P f(\mathbf{r}_1, \mathbf{r}_2) = f(\mathbf{r}_2, \mathbf{r}_1)$

$P^2 f(\mathbf{r}_1, \mathbf{r}_2) = P f(\mathbf{r}_2, \mathbf{r}_1) = f(\mathbf{r}_1, \mathbf{r}_2)$

$\forall f \implies P^2 = 1$

$g$가 고유값 $\lambda$를 갖는 $P$의 고유함수라고 하자: $P g = \lambda g$

$\to P^2 g = \lambda P g = \lambda^2 g = g$

$\therefore \lambda = \pm 1$

두 동일 입자에 대해:
$P [H(\mathbf{r}_1, \mathbf{r}_2) \Psi(\mathbf{r}_1, \mathbf{r}_2)] = H(\mathbf{r}_2, \mathbf{r}_1) \Psi(\mathbf{r}_2, \mathbf{r}_1) = H(\mathbf{r}_1, \mathbf{r}_2) P \Psi(\mathbf{r}_1, \mathbf{r}_2)$

$\to PH = HP$ 또는 $[P, H] = 0$

$\forall \Psi$

$\therefore H$와 $P$는 동일한 고유상태를 공유할 **수 있으며 (can), 반드시 공유해야 한다 (MUST)**.
즉, $\psi(\mathbf{r}_1, \mathbf{r}_2) = \pm \psi(\mathbf{r}_2, \mathbf{r}_1)$는 **보손 (bosons)** 또는 **페르미온 (fermions)**에 대한 **대칭화 요구 조건 (Symmetrization requirement)**이다.

***

### **예제 5.1. 무한 사각 우물 (Infinite Square Well)**

폭이 $a$인 무한 사각 우물 안에 동일한 질량 $m$을 가진 두 개의 상호작용 없는 입자를 고려한다.

1-입자 상태는 다음과 같다:
$\psi_n(x) = \sqrt{\frac{2}{a}} \sin\left(\frac{n\pi}{a}x\right)$

$E_n = n^2 \frac{\hbar^2 \pi^2}{2ma^2} = n^2 K$

**구별 가능한 입자 (Distinguishable particles):**
$\psi_{n_1, n_2}(x_1, x_2) = \psi_{n_1}(x_1) \psi_{n_2}(x_2)$

$E_{n_1, n_2} = (n_1^2 + n_2^2) K$

예시, **바닥 상태 (Ground state):**
$\psi_{11}(x_1, x_2) = \frac{2}{a} \sin\left(\frac{\pi}{a}x_1\right) \sin\left(\frac{\pi}{a}x_2\right)$

$E_{11} = 2K$

**첫 번째 들뜬 상태 (1st excited state):**
$\psi_{12}(x_1, x_2) = \frac{2}{a} \sin\left(\frac{\pi}{a}x_1\right) \sin\left(\frac{2\pi}{a}x_2\right)$

$E_{12} = 5K$

$\psi_{21}(x_1, x_2) = \frac{2}{a} \sin\left(\frac{2\pi}{a}x_1\right) \sin\left(\frac{\pi}{a}x_2\right)$

$E_{21} = 5K$
**이중 축퇴된 (Doubly degenerate)**

($\psi_n(x) = \sqrt{\frac{2}{a}} \sin\left(\frac{n\pi}{a}x\right)$, $E_n = n^2 K$)

***

**보손 (Bosons):**
**바닥 상태 (Ground state):**
$\psi_0(x_1, x_2) = \frac{2}{a} \sin\left(\frac{\pi}{a}x_1\right) \sin\left(\frac{\pi}{a}x_2\right)$

$E_0 = 2K$

**첫 번째 들뜬 상태 (1st excited state):**
$\psi_1(x_1, x_2) = \frac{1}{\sqrt{2}} \left[ \frac{2}{a} \sin\left(\frac{\pi}{a}x_1\right) \sin\left(\frac{2\pi}{a}x_2\right) + \frac{2}{a} \sin\left(\frac{2\pi}{a}x_1\right) \sin\left(\frac{\pi}{a}x_2\right) \right]$

$E_1 = 5K$
**비축퇴된 (Nondegenerate)**

***

**페르미온 (Fermions):**
**바닥 상태 (Ground state):**
$\psi_0(x_1, x_2) = \frac{1}{\sqrt{2}} \left[ \frac{2}{a} \sin\left(\frac{\pi}{a}x_1\right) \sin\left(\frac{2\pi}{a}x_2\right) - \frac{2}{a} \sin\left(\frac{2\pi}{a}x_1\right) \sin\left(\frac{\pi}{a}x_2\right) \right]$

$E_0 = 5K$

***

### **5.1.2. 교환력 (Exchange Forces)**

상태 $a$에 있는 한 입자와 상태 $b$에 있는 다른 한 입자, 총 2개의 입자를 고려한다.

*   **구별 가능한 입자 (Particles distinguishable):** $\psi(x_1, x_2) = \psi_a(x_1) \psi_b(x_2)$ (입자 1은 $a$에, 2는 $b$에 있다.)
*   **보손 (Bosons):** $\psi_+(x_1, x_2) = \frac{1}{\sqrt{2}}[\psi_a(x_1)\psi_b(x_2) + \psi_b(x_1)\psi_a(x_2)]$
*   **페르미온 (Fermions):** $\psi_-(x_1, x_2) = \frac{1}{\sqrt{2}}[\psi_a(x_1)\psi_b(x_2) - \psi_b(x_1)\psi_a(x_2)]$
(모든 상태는 정규화되어 있다.)

입자 분리 표준 편차를 각 경우에 대해 계산할 것이다:
$\langle (x_1 - x_2)^2 \rangle = \langle x_1^2 \rangle + \langle x_2^2 \rangle - 2 \langle x_1 x_2 \rangle$

***

### **구별 가능한 입자 (Distinguishable Particles)**

$\psi_D(x_1, x_2) = \psi_a(x_1) \psi_b(x_2)$

$\langle (x_1 - x_2)^2 \rangle = \langle x_1^2 \rangle + \langle x_2^2 \rangle - 2 \langle x_1 x_2 \rangle$

$\langle x_1^2 \rangle_D = \int dx_1 \int dx_2 \psi_D^* (x_1, x_2) x_1^2 \psi_D(x_1, x_2)$

$= \int dx_1 \psi_a^* (x_1) x_1^2 \psi_a(x_1) \int dx_2 \psi_b^* (x_2) \psi_b(x_2) = \langle x^2 \rangle_a$ (여기서 $\psi_a, \psi_b$는 정규화되어 있다)

유사하게 (Similarly), $\langle x_2^2 \rangle_D = \langle x^2 \rangle_b$

$\langle x_1 x_2 \rangle_D = \int dx_1 \int dx_2 \psi_D^* (x_1, x_2) x_1 x_2 \psi_D(x_1, x_2)$

$= \int dx_1 \psi_a^* (x_1) x_1 \psi_a(x_1) \int dx_2 \psi_b^* (x_2) x_2 \psi_b(x_2) = \langle x \rangle_a \langle x \rangle_b$

$\therefore \langle (x_1 - x_2)^2 \rangle_D = \langle x^2 \rangle_a + \langle x^2 \rangle_b - 2 \langle x \rangle_a \langle x \rangle_b$

***

### **동일 입자 (Identical Particles)**

$\psi_{\pm}(x_1, x_2) = \frac{1}{\sqrt{2}}[\psi_a(x_1)\psi_b(x_2) \pm \psi_b(x_1)\psi_a(x_2)]$

$\langle (x_1 - x_2)^2 \rangle = \langle x_1^2 \rangle + \langle x_2^2 \rangle - 2 \langle x_1 x_2 \rangle$

$$\begin{aligned}
|\psi_{\pm}(x_1, x_2)|^2 &= \frac{1}{2} [ |\psi_a(x_1)\psi_b(x_2)|^2 + |\psi_b(x_1)\psi_a(x_2)|^2 ] \\ &\pm \frac{1}{2} [ \psi_a^* (x_1)\psi_b^* (x_2)\psi_b(x_1)\psi_a(x_2) + \psi_b^* (x_1)\psi_a^* (x_2)\psi_a(x_1)\psi_b(x_2) ]
\end{aligned}$$　

$\langle x_1^2 \rangle_{\pm} = \int dx_1 \int dx_2 \|\psi_{\pm}(x_1, x_2)\|^2 x_1^2 = \frac{1}{2} [ \langle x^2 \rangle_a + \langle x^2 \rangle_b ]$ ($\psi_a, \psi_b$는 직교정규)

유사하게 (Similarly), $\langle x_2^2 \rangle_{\pm} = \frac{1}{2} [ \langle x^2 \rangle_a + \langle x^2 \rangle_b ]$

$\langle x_1 x_2 \rangle_{\pm} = \int dx_1 \int dx_2 \|\psi_{\pm}(x_1, x_2)\|^2 x_1 x_2$

$= \frac{1}{2} [\langle x \rangle_a \langle x \rangle_b + \langle x \rangle_b \langle x \rangle_a] \pm \frac{1}{2} [ \langle x \rangle_{ab}\langle x \rangle_{ba} + \langle x \rangle_{ba}\langle x \rangle_{ab} ] = \langle x \rangle_a \langle x \rangle_b \pm \langle x \rangle_{ab} \langle x \rangle_{ba}$

여기서 $\langle x \rangle_{ab} = \int dx \psi_a^* (x) x \psi_b(x)$

***

$\langle x_1^2 \rangle_{\pm} = \langle x_2^2 \rangle_{\pm} = \frac{1}{2} [ \langle x^2 \rangle_a + \langle x^2 \rangle_b ]$

$\langle (x_1 - x_2)^2 \rangle = \langle x^2_1 \rangle + \langle x^2_2 \rangle - 2 \langle x_1 x_2 \rangle$

$\langle x_1 x_2 \rangle_{\pm} = \langle x \rangle_a \langle x \rangle_b \pm \langle x \rangle_{ab} \langle x \rangle_{ba}$


$\to \langle (x_1 - x_2)^2 \rangle_{\pm} = \langle x^2 \rangle_a + \langle x^2 \rangle_b - 2 \langle x \rangle_a \langle x \rangle_b \mp 2 \langle x \rangle_{ab} \langle x \rangle_{ba}$

$= \langle (x_1 - x_2)^2 \rangle_D \mp 2 \langle x \rangle_{ab} \langle x \rangle_{ba} $

또는 $\langle (\Delta x)^2 \rangle_{\pm} = \langle (\Delta x)^2 \rangle_D \mp 2 \|\langle x \rangle_{ab}\|^2$

$\therefore$ **보손은 구별 가능한 경우보다 더 가깝게 (closer) 위치하며, 페르미온은 더 멀리 (further apart) 위치한다.**

$\to$ **효과적인 교환력 (effective exchange force)은 보손에 대해서는 인력(attractive)이며, 페르미온에 대해서는 척력(repulsive)이다.**

참고 (Note): 만약 입자들이 멀리 떨어져 있으면 $\psi_a, \psi_b$는 중첩되지 않으므로 (don't overlap), $\langle (\Delta x)^2 \rangle_{\pm} = \langle (\Delta x)^2 \rangle_D$.

***

### **간소화된 유도 (Simplified Derivation)**

$\langle A \rangle = \langle \psi \| A \| \psi \rangle$

$\langle (x_1 - x_2)^2 \rangle = \langle x_1^2 \rangle + \langle x_2^2 \rangle - 2 \langle x_1 x_2 \rangle$

$\psi_D(x_1, x_2) = \psi_a(x_1) \psi_b(x_2) \sim \|\psi_D \rangle = \|a b \rangle$

$\langle (x_1 - x_2)^2 \rangle_D = \langle ab \| x_1^2 \| ab \rangle + \langle ab \| x_2^2 \| ab \rangle - 2 \langle ab \| x_1 x_2 \| ab \rangle = \langle x^2 \rangle_a + \langle x^2 \rangle_b - 2 \langle x \rangle_a \langle x \rangle_b$

$\psi_{\pm}(x_1, x_2) = \frac{1}{\sqrt{2}}[\psi_a(x_1)\psi_b(x_2) \pm \psi_b(x_1)\psi_a(x_2)] \sim \|\psi_\pm \rangle = \frac{1}{\sqrt{2}}(\|ab\rangle \pm \|ba\rangle)$

$\langle A \rangle_{\pm} = \frac{1}{2} [\langle ab \| A \| ab \rangle + \langle ba \| A \| ba \rangle \pm \langle ab \| A \| ba \rangle \pm \langle ba \| A \| ab \rangle ]$

$\langle x_1^2 \rangle_{\pm} = \frac{1}{2} [\langle ab \| x_1^2 \| ab \rangle + \langle ba \| x_1^2 \| ba \rangle \pm \langle ab \| x_1^2 \| ba \rangle \pm \langle ba \| x_1^2 \| ab \rangle ]$

$= \frac{1}{2} [\langle x^2 \rangle_a + \langle x^2 \rangle_b \pm \langle x^2 \rangle_{ab} \langle b \| a \rangle \pm \langle x^2 \rangle_{ba} \langle a \| b \rangle ] = \frac{1}{2} [\langle x^2 \rangle_a + \langle x^2 \rangle_b ]$ 

만약 $\langle a \| b \rangle = 0$면, 
여기서 $\langle A \rangle_{ab} \equiv \langle a \| A \| b \rangle$

***

$\langle x_1^2 \rangle_{\pm} = \frac{1}{2} [ \langle x^2 \rangle_a + \langle x^2 \rangle_b ]$

유사하게 (Similarly), $\langle x_2^2 \rangle_{\pm} = \frac{1}{2} [ \langle x^2 \rangle_a + \langle x^2 \rangle_b ]$

$\langle x_1 x_2 \rangle_{\pm} = \frac{1}{2} [\langle x \rangle_a \langle x \rangle_b + \langle x \rangle_b \langle x \rangle_a \pm \langle x \rangle_{ab} \langle x \rangle_{ba} \pm \langle x \rangle_{ba} \langle x \rangle_{ab} ] = \langle x \rangle_a \langle x \rangle_b \pm \langle x \rangle_{ab} \langle x \rangle_{ba}$

$\to \langle (x_1 - x_2)^2 \rangle_{\pm} = \langle x^2 \rangle_a + \langle x^2 \rangle_b - 2 \langle x \rangle_a \langle x \rangle_b \mp 2 \langle x \rangle_{ab} \langle x \rangle_{ba}$

$= \langle (x_1 - x_2)^2 \rangle_D \mp 2 \langle x \rangle_{ab} \langle x \rangle_{ba}$

또는 (or) $\langle (\Delta x)^2 \rangle_{\pm} = \langle (\Delta x)^2 \rangle_D \mp 2 \|\langle x \rangle_{ab}\|^2$

$\therefore$ **보손은 구별 가능한 경우보다 더 가깝게 (closer) 위치하며, 페르미온은 더 멀리 (further apart) 위치한다.**

$\to$ **효과적인 교환력 (effective exchange force)은 보손에 대해서는 인력(attractive)이며, 페르미온에 대해서는 척력(repulsive)이다.**

참고 (Note): 만약 입자들이 멀리 떨어져 있으면 $\psi_a, \psi_b$는 중첩되지 않으므로 (don't overlap), $\langle (\Delta x)^2 \rangle_{\pm} = \langle (\Delta x)^2 \rangle_D$.

***