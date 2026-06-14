# 📘 Chapter 6 — Properties of the Integral 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 적분이 어떤 대수적/순서적 성질을 가지는지 정리한다.

- 선형성
- 단조성
- 구간 분할(additivity)
- 절댓값 estimate
- integrator $\alpha$ 쪽 선형성
- 곱과 절댓값의 적분 가능성
- step-function integrator, pure jump integrator, derivative integrator, change of variables

즉 “적분을 실제로 계산하고 다루는 법”을 만든다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 6.12

$f_1,f_2\in\mathcal R(\alpha)$이면

1. $f_1+f_2\in\mathcal R(\alpha)$, $cf\in\mathcal R(\alpha)$
2. 선형성:
   $$
   \int (f_1+f_2)\,d\alpha=\int f_1\,d\alpha+\int f_2\,d\alpha,
   \qquad
   \int cf\,d\alpha=c\int f\,d\alpha
   $$
3. 순서보존:
   $f_1\le f_2\Rightarrow \int f_1\,d\alpha\le\int f_2\,d\alpha$
4. 구간 분할:
   $$
   \int_a^c f\,d\alpha+\int_c^b f\,d\alpha=\int_a^b f\,d\alpha
   $$
5. boundedness estimate:
   $$
   \left|\int_a^b f\,d\alpha\right|\le M[\alpha(b)-\alpha(a)]
   $$
   if $|f|\le M$
6. integrator 쪽 선형성

### ▪ Theorem 6.13

$f,g\in\mathcal R(\alpha)$이면

1. $fg\in\mathcal R(\alpha)$
2. $|f|\in\mathcal R(\alpha)$이고
   $$
   \left|\int_a^b f\,d\alpha\right|\le \int_a^b |f|\,d\alpha.
   $$

### ▪ Definition 6.14

unit step function
$$
I(x)=\begin{cases}0&(x\le0),\\1&(x>0)
\end{cases}
$$

### ▪ Theorem 6.15

$\alpha(x)=I(x-s)$, $f$ bounded and continuous at $s$이면
$$
\int_a^b f\,d\alpha=f(s).
$$

### ▪ Theorem 6.16

$\alpha(x)=\sum c_n I(x-s_n)$ with $c_n\ge0$, $\sum c_n$ convergent, $f$ continuous이면
$$
\int_a^b f\,d\alpha=\sum c_n f(s_n).
$$

### ▪ Theorem 6.17

$\alpha$가 increasing이고 $\alpha'\in\mathcal R$라 하자. bounded real $f$에 대해
$$
f\in\mathcal R(\alpha)
\iff
f\alpha'\in\mathcal R,
$$
그리고 그 경우
$$
\int_a^b f\,d\alpha=\int_a^b f(x)\alpha'(x)\,dx.
$$

### ▪ Theorem 6.19 — Change of variable

$\phi:[A,B]\to[a,b]$가 strictly increasing continuous bijection이고
$$
\beta(y)=\alpha(\phi(y)),\qquad g(y)=f(\phi(y))
$$
라 하자. 그러면
$$
\int_A^B g\,d\beta=\int_a^b f\,d\alpha.
$$

special case로 ordinary change of variable formula도 나온다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 중요한 메시지는 Stieltjes 적분이 series와 ordinary integral을 모두 포함하는 유연한 틀이라는 점이다.

- pure step integrator → weighted sum
- differentiable integrator → ordinary Riemann integral

즉 “적분”은 하나의 공통 언어이고, series와 integrals를 따로 보지 않게 해 준다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 적분의 선형성/분할/estimate를 계산에 쓸 때
- Stieltjes integral을 실제로 sum이나 ordinary integral로 바꾸고 싶을 때
- change of variable을 쓰고 싶을 때

### 📌 문제 풀이 패턴
1. 선형성으로 분해
2. 순서로 부등식 제어
3. step integrator면 discrete sum으로 환원
4. $\alpha'$가 있으면 ordinary integral로 환원

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 3은 step-function integrator의 직접 응용
- Exercise 11, 12는 $L^2$-type norm과 approximation 문제로 이 절의 성질을 적극 사용
- Exercise 19는 curve length invariance와 later sections로 이어진다

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorems 6.12, 6.13 포함
- [x] Definitions/Theorems 6.14–6.17 포함
- [x] Theorem 6.19 포함
- [x] sum/integral unification 설명 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- step integrator가 왜 weighted sum을 주는가?
- $d\alpha=\alpha'(x)dx$ 꼴은 언제 가능한가?
- change of variable이 partition correspondence로 왜 증명되는가?
