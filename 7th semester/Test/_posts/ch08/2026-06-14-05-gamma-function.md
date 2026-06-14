# 📘 Chapter 8 — The Gamma Function 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 factorial을 실수 전체로 확장하는 special function $\Gamma$를 다룬다.

- 정의
$$
\Gamma(x)=\int_0^{\infty} t^{x-1}e^{-t}dt
$$
- functional equation $\Gamma(x+1)=x\Gamma(x)$
- $\Gamma(n+1)=n!$
- log-convexity
- Beta function과의 관계
- $\Gamma(1/2)=\sqrt{\pi}$
- Stirling’s formula

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 8.17

$x>0$에 대해
$$
\Gamma(x)=\int_0^{\infty} t^{x-1}e^{-t}dt.
$$

### ▪ Theorem 8.18

1. functional equation
   $$
   \Gamma(x+1)=x\Gamma(x)
   $$
2. $\Gamma(n+1)=n!$
3. $\log\Gamma$는 $(0,\infty)$에서 convex

### ▪ Theorem 8.19

Bohr–Mollerup-type characterization: positive function $f$가

1. $f(x+1)=xf(x)$
2. $f(1)=1$
3. $\log f$ convex

를 만족하면 $f=\Gamma$.

### ▪ Theorem 8.20

Beta function identity
$$
\int_0^1 t^{x-1}(1-t)^{y-1}dt = \frac{\Gamma(x)\Gamma(y)}{\Gamma(x+y)}.
$$

### ▪ Some consequences 8.21

- trigonometric substitution으로 beta-gamma relation 변형
-
$$
\Gamma(1/2)=\sqrt{\pi}
$$
- Gaussian integral
$$
\int_0^{\infty} e^{-s^2}ds=\sqrt{\pi}/2
$$

### ▪ Stirling’s formula 8.22

$$
\lim_{x\to\infty}\frac{\Gamma(x+1)}{(x/e)^x\sqrt{2\pi x}}=1.
$$

이는 factorial growth의 정밀한 비대칭식을 제공한다.

---

## 🟢 3. 개념 해설 + 엄밀성

$\Gamma$는 factorial의 자연스러운 연속 확장이다. 하지만 단지 interpolation만이 아니라, 적분표현·convexity·beta 관계·asymptotic까지 모두 갖는 중심 special function이다. 이 절은 해석학이 단순 계산을 넘어 special function theory로 가는 입구 역할을 한다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- factorial을 실수/복소 변수로 확장할 때
- beta integrals를 계산할 때
- Gaussian integral을 정당화할 때
- large factorial asymptotics를 구할 때

### 📌 문제 풀이 패턴
1. integration by parts로 functional equation
2. substitution으로 beta/gamma 변환
3. log-convexity로 uniqueness
4. scaling/substitution으로 Stirling 준비

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 20, 30, 31은 Stirling formula와 gamma asymptotics와 연결된다.
- Exercise 22의 binomial theorem 연장도 gamma notation과 친하다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 8.17 포함
- [x] Theorems 8.18–8.22 포함
- [x] Beta/Gamma/$\sqrt\pi$ 연결 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 $\Gamma(x+1)=x\Gamma(x)$가 factorial extension이라고 말할 수 있는가?
- $\Gamma(1/2)=\sqrt{\pi}$가 왜 중요한가?
- Stirling’s formula가 무엇을 근사하는지 설명하라.
