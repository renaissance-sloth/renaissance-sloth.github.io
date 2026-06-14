# 📘 Chapter 6 — Definition and Existence of the Integral 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 Riemann 적분과 Riemann–Stieltjes 적분의 정의를 세우고, 어떤 함수가 적분 가능한지 판정하는 기준을 만든다.

- partition, upper sum, lower sum 정의
- Riemann 적분을 Stieltjes 적분의 special case로 포함
- refinement가 upper/lower sum에 주는 영향 분석
- integrability criterion
- continuous / monotone / 유한개 불연속 함수의 적분 가능성 증명

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definitions 6.1, 6.2

$[a,b]$의 partition $P=\{x_0,\dots,x_n\}$와 bounded real function $f$에 대해
$$
M_i=\sup f(x),\quad m_i=\inf f(x)
\qquad (x_{i-1}\le x\le x_i)
$$
를 두고 upper/lower sums를 정의한다.

Riemann case에서는
$$
U(P,f)=\sum M_i\Delta x_i,
\qquad
L(P,f)=\sum m_i\Delta x_i.
$$

Stieltjes case에서는 increasing function $\alpha$에 대해
$$
\Delta \alpha_i=\alpha(x_i)-\alpha(x_{i-1}),
$$
그리고
$$
U(P,f,\alpha)=\sum M_i\Delta\alpha_i,
\qquad
L(P,f,\alpha)=\sum m_i\Delta\alpha_i.
$$

upper integral과 lower integral이 같으면
$$
\int_a^b f\,d\alpha
$$
를 정의하고 $f\in\mathcal R(\alpha)$라 쓴다.

### ▪ Definition 6.3

$P^*\supset P$이면 $P^*$를 refinement라 한다. 두 partitions의 union은 common refinement이다.

### ▪ Theorem 6.4

refinement $P^*$에 대해
$$
L(P,f,\alpha)\le L(P^*,f,\alpha),
\qquad
U(P^*,f,\alpha)\le U(P,f,\alpha).
$$

### ▪ Proof idea

점 하나를 추가한 refinement부터 보이면 된다. 구간을 둘로 쪼개면 inf는 올라가고 sup는 내려간다. 여러 점을 추가하는 일반 경우는 반복하면 된다.

### ▪ Theorem 6.5

항상
$$
\underline{\int_a^b} f\,d\alpha \le \overline{\int_a^b} f\,d\alpha.
$$

### ▪ Theorem 6.6 — Integrability criterion

$f\in\mathcal R(\alpha)$일 필요충분조건은 모든 $\varepsilon>0$에 대해 어떤 partition $P$가 존재하여
$$
U(P,f,\alpha)-L(P,f,\alpha)<\varepsilon
$$
가 되는 것이다.

### ▪ Theorem 6.7

위 criterion의 refinement stability와 Riemann sum estimate:

1. 한 partition에서 gap이 작으면 모든 refinement에서도 작다.
2. 같은 subinterval 안의 sample points $s_i,t_i$에 대해
   $$
   \sum |f(s_i)-f(t_i)|\Delta\alpha_i<\varepsilon.
   $$
3. 따라서 Riemann sums가 적분값에 가깝다.

### ▪ Theorem 6.8

$f$가 $[a,b]$에서 continuous이면 $f\in\mathcal R(\alpha)$.

### ▪ Proof idea

compact interval 위 continuous function은 uniformly continuous이므로, partition mesh를 충분히 잘게 하면 각 subinterval에서 $M_i-m_i$를 작게 만들 수 있고, 따라서 upper-lower gap도 작아진다.

### ▪ Theorem 6.9

$f$가 monotone이고 $\alpha$가 continuous이면 $f\in\mathcal R(\alpha)$.

### ▪ Proof idea

$\alpha$-increments를 균등하게 나누는 partition을 잡으면 telescope처럼
$$
U-L=\frac{\alpha(b)-\alpha(a)}{n}[f(b)-f(a)]
$$
형태가 되어 0으로 보낼 수 있다.

### ▪ Theorem 6.10

$f$가 bounded이고 불연속점이 유한 개뿐이며, $\alpha$가 그 불연속점들에서 continuous이면 $f\in\mathcal R(\alpha)$.

### ▪ Theorem 6.11

$f\in\mathcal R(\alpha)$, $m\le f\le M$, $\phi$가 $[m,M]$에서 continuous이면
$$
h(x)=\phi(f(x))
$$
도 $\mathcal R(\alpha)$에 속한다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 핵심은 적분 가능성을 “upper/lower sum 차이를 얼마나 작게 만들 수 있느냐”로 보는 것이다. 즉 적분은 계산이 아니라 **oscillation control** 문제다. continuous function이 적분 가능한 이유도, monotone function이 적분 가능한 이유도 결국 각 구간에서 함수의 진동 폭을 제어할 수 있기 때문이다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 어떤 함수가 Riemann/Stieltjes 적분 가능한지 증명할 때
- step function, monotone function, finite discontinuity function을 다룰 때
- 이후의 integral identities를 쓰기 전 integrability를 확보할 때

### 📌 문제 풀이 패턴
1. partition을 잘 골라서 $U-L$를 작게 만든다.
2. continuous면 uniform continuity 사용
3. monotone면 telescoping 사용
4. 유한개 불연속이면 나쁜 구간만 따로 잘라낸다.

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 1, 3, 4, 6은 이 절의 직접 응용이다.
- 특히 step-function type $\alpha$와 discontinuity structure를 이해하면 Chapter 6 과제의 절반이 쉬워진다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definitions 6.1–6.3 포함
- [x] Theorems 6.4–6.11 포함
- [x] integrability criterion 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- refinement가 왜 upper sum은 내리고 lower sum은 올리는가?
- continuous function의 적분 가능성이 왜 uniform continuity와 연결되는가?
- monotone function 적분 가능성 증명에서 telescoping이 어디서 나오나?
