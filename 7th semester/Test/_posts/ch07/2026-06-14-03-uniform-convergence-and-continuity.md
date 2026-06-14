# 📘 Chapter 7 — Uniform Convergence and Continuity 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 uniform convergence가 continuity를 보존하는 핵심 이유를 다룬다.

- limit와 pointwise limit의 교환 정리
- continuous functions의 uniform limit는 continuous
- monotone pointwise convergence + compactness → uniform convergence (Dini-type theorem)
- $\mathscr C(X)$와 sup norm complete metric 구조

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 7.11

$f_n\to f$ uniformly on $E$, $x$가 $E$의 limit point이고
$$
\lim_{t\to x} f_n(t)=A_n
$$
가 존재하면 $\{A_n\}$은 수렴하고
$$
\lim_{t\to x}f(t)=\lim_{n\to\infty}A_n.
$$

즉
$$
\lim_{t\to x}\lim_{n\to\infty}f_n(t)=\lim_{n\to\infty}\lim_{t\to x}f_n(t).
$$

### ▪ Proof idea

uniform convergence가 주는 global estimate와 각 $f_n$의 limit estimate를 triangle inequality로 결합한다.

### ▪ Theorem 7.12

continuous functions의 sequence $f_n$이 $E$에서 $f$로 uniformly converge하면 $f$는 continuous이다.

### ▪ Theorem 7.13

$K$ compact, $f_n$ continuous, $f_n\to f$ pointwise, 그리고 $f_n(x)\ge f_{n+1}(x)$ for all $x$. 그러면 $f_n\to f$는 uniformly on $K$.

### ▪ Proof idea

$g_n=f_n-f$를 두고 $K_n=\{x:g_n(x)\ge\varepsilon\}$를 보자. $K_n$은 nested compact sets이며 교집합이 empty다. compactness로 어느 시점부터 empty가 되어 uniform convergence를 얻는다.

### ▪ Definition 7.14

$\mathscr C(X)$: domain이 $X$인 모든 bounded continuous complex-valued functions의 집합. sup norm
$$
\|f\|=\sup_{x\in X}|f(x)|
$$
를 도입한다.

### ▪ Theorem 7.15

sup norm metric은 $\mathscr C(X)$를 complete metric space로 만든다.

---

## 🟢 3. 개념 해설 + 엄밀성

uniform convergence가 continuity를 보존하는 이유는 “모든 점에서 동시에 작은 오차”를 보장하기 때문이다. pointwise convergence는 각 점에서 다른 속도로 붙을 수 있으므로 continuity를 망칠 수 있다.

또 $\mathscr C(X)$를 complete metric space로 보는 관점은 Stone–Weierstrass로 가는 길을 연다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- continuous limit를 보장하고 싶을 때
- pointwise monotone convergence를 uniform으로 승격하고 싶을 때
- function space를 metric space로 다룰 때

### 📌 문제 풀이 패턴
1. uniform convergence + triangle inequality
2. compactness + nested closed sets
3. sup norm으로 function space completion

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 9: $x_n\to x$와 uniform convergence를 섞어 함수값 limit를 다루는 표준 응용
- Exercise 16: equicontinuity + pointwise convergence → uniform convergence와 밀접

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorems 7.11–7.13 포함
- [x] Definition 7.14 포함
- [x] Theorem 7.15 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 uniform limit of continuous functions는 continuous인가?
- Dini-type theorem에서 compactness가 왜 중요한가?
- $\mathscr C(X)$의 complete metric 구조가 왜 유용한가?
