# 📘 Chapter 6 — Integration and Differentiation 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 적분과 미분이 어떤 의미에서 서로 inverse라는 사실을 다룬다.

- 적분으로 만든 함수 $F(x)=\int_a^x f(t)dt$의 연속성과 미분 가능성
- fundamental theorem of calculus
- integration by parts

즉 Chapter 6의 핵심 climax다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 6.20

$f\in\mathcal R$ on $[a,b]$라 하고
$$
F(x)=\int_a^x f(t)dt
$$
로 두자. 그러면 $F$는 $[a,b]$에서 continuous이다. 또 $f$가 $x_0$에서 continuous이면
$$
F'(x_0)=f(x_0).
$$

### ▪ Proof

$|f(t)|\le M$이면
$$
|F(y)-F(x)|=\left|\int_x^y f(t)dt\right|\le M|y-x|,
$$
따라서 $F$는 continuous이다.

또 $f$가 $x_0$에서 continuous이면, $s,t$가 $x_0$ 근처일 때
$$
\left|\frac{F(t)-F(s)}{t-s}-f(x_0)\right|
=\left|\frac1{t-s}\int_s^t (f(u)-f(x_0))du\right|
<\varepsilon.
$$
따라서 $F'(x_0)=f(x_0)$.

### ▪ Theorem 6.21 — Fundamental Theorem of Calculus

$f\in\mathcal R$ on $[a,b]$이고, differentiable function $F$가 $F'=f$를 만족하면
$$
\int_a^b f(x)dx=F(b)-F(a).
$$

### ▪ Proof

partition $P$를 적당히 잡고, 각 구간마다 mean value theorem으로
$$
F(x_i)-F(x_{i-1})=f(t_i)\Delta x_i
$$
를 얻는다. 모두 더하면 Riemann sum이 $F(b)-F(a)$가 되고, integrability로 한계값을 보내면 결론이 나온다.

### ▪ Theorem 6.22 — Integration by parts

$F,G$가 differentiable, $F'=f\in\mathcal R$, $G'=g\in\mathcal R$이면
$$
\int_a^b F(x)g(x)dx=F(b)G(b)-F(a)G(a)-\int_a^b f(x)G(x)dx.
$$

### ▪ Proof

$H(x)=F(x)G(x)$로 두고 product rule과 fundamental theorem을 적용하면 된다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 핵심은 “적분이 누적합이라면, 미분은 그 누적의 순간변화율을 되찾는다”는 것이다. 다만 아무 함수에나 되는 게 아니라 integrability와 pointwise continuity 같은 가정이 중요하다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 적분으로 정의한 함수의 derivative를 구할 때
- primitive가 있을 때 definite integral을 계산할 때
- 곱적분을 변형할 때

### 📌 문제 풀이 패턴
1. 적분 정의 함수면 Theorem 6.20 사용
2. primitive 있으면 FTC로 계산
3. 곱 구조면 integration by parts

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 1, 2는 적분과 함수값의 구조를 익히게 한다.
- improper integral 쪽 Exercise 7, 8도 이 절의 관점을 확장한 것이다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorems 6.20, 6.21, 6.22 포함
- [x] FTC 설명 포함
- [x] integration by parts 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 $F(x)=\int_a^x f$는 항상 continuous인가?
- 어떤 추가 가정에서 $F'(x)=f(x)$가 되는가?
- FTC와 integration by parts의 관계를 설명하라.
