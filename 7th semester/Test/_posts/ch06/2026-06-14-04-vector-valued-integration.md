# 📘 Chapter 6 — Integration of Vector-Valued Functions 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 scalar 적분을 $\mathbb R^k$-valued function으로 확장한다. 핵심은 모든 좌표에 대해 적분을 정의하고, 주요 성질이 좌표별로 그대로 따라온다는 것이다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 6.23

$f=(f_1,\dots,f_k)$가 $[a,b]\to\mathbb R^k$일 때, $f\in\mathcal R(\alpha)$라는 것은 각 좌표 $f_j\in\mathcal R(\alpha)$임을 뜻한다. 그리고
$$
\int_a^b f\,d\alpha=
\left(
\int_a^b f_1\,d\alpha,
\dots,
\int_a^b f_k\,d\alpha
\right).
$$

### ▪ Theorem 6.24

$f,F:[a,b]\to\mathbb R^k$, $f\in\mathcal R$, $F'=f$이면
$$
\int_a^b f(t)dt=F(b)-F(a).
$$

이는 scalar FTC를 각 coordinate에 적용하면 된다.

### ▪ Theorem 6.25

$f:[a,b]\to\mathbb R^k$, $f\in\mathcal R(\alpha)$이면 $|f|\in\mathcal R(\alpha)$이고
$$
\left|\int_a^b f\,d\alpha\right|
\le
\int_a^b |f|\,d\alpha.
$$

### ▪ Proof idea

좌표합으로 $|f|=(f_1^2+\cdots+f_k^2)^{1/2}$를 만들고 scalar integrability closure를 이용한다. 이후 Schwarz inequality로 적분의 norm estimate를 얻는다.

---

## 🟢 3. 개념 해설 + 엄밀성

벡터 적분은 새로운 철학이 아니라 “좌표별 적분 + norm estimate”다. 하지만 scalar case에는 없던 기하적 의미가 생긴다. 이후 rectifiable curves에서 바로 이 점이 중요해진다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- curve, path, velocity를 적분할 때
- 벡터값 primitive를 쓸 때
- 적분의 크기를 norm으로 estimate할 때

### 📌 문제 풀이 패턴
1. coordinatewise 분해
2. scalar theorem 적용
3. norm은 Schwarz inequality로 제어

---

## 🔴 5. 대표 문제 & 풀이 전략

- Chapter 6의 curve-length 문제들과 Exercise 19는 이 절의 직접 응용이다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 6.23 포함
- [x] Theorems 6.24, 6.25 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 벡터 적분을 왜 좌표별로 정의할 수 있는가?
- Theorem 6.25의 inequality는 어떤 점에서 scalar case와 다른가?
- curve를 적분할 때 이 절이 왜 필요한가?
