# 📘 Chapter 7 — Uniform Convergence and Differentiation 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

미분과 limit의 교환은 적분보다 훨씬 더 민감하다. 이 절은 어떤 강한 가정 아래에서만 differentiation이 limit를 통과할 수 있는지를 설명한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 7.17

$f_n$이 $[a,b]$에서 differentiable이고, 어떤 한 점 $x_0$에서 $f_n(x_0)$가 수렴한다고 하자. 또 $f_n'$이 $[a,b]$에서 uniformly converge한다고 하자. 그러면 $f_n$은 $[a,b]$에서 어떤 함수 $f$로 uniformly converge하고,
$$
f'(x)=\lim_{n\to\infty} f_n'(x)
\qquad (a\le x\le b).
$$

### ▪ Proof idea

먼저 derivative의 uniform convergence와 한 점에서의 수렴을 이용해 $f_n$ 자체가 uniformly Cauchy임을 mean value theorem으로 보인다. 그 후 difference quotient sequence에 Theorem 7.11을 적용해 derivative limit를 얻는다.

### ▪ Theorem 7.18

nowhere differentiable continuous real function이 존재한다.

본문은
$$
f(x)=\sum_{n=0}^{\infty}\left(\frac34\right)^n \varphi(4^n x)
$$
형태의 classical construction을 준다.

---

## 🟢 3. 개념 해설 + 엄밀성

uniform convergence of derivatives만으로도 부족하고, 함수값을 한 점에서 anchor해야 한다는 점이 중요하다. derivative는 적분과 달리 상수 하나가 빠질 수 있기 때문이다. Theorem 7.17은 그 상수를 $x_0$에서 고정해 준다.

Theorem 7.18은 “continuous하면 웬만하면 미분 가능할 것”이라는 직관이 얼마나 틀릴 수 있는지를 보여 준다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 함수열의 derivative limit를 정당화할 때
- parameter-dependent families를 미분할 때
- 반례를 통해 미분과 limit 교환의 위험성을 설명할 때

### 📌 문제 풀이 패턴
1. derivative sequence uniform convergence 확인
2. 한 점에서 함수값 convergence 확보
3. MVT로 함수열 자체 uniform Cauchy 도출
4. difference quotient에 limit theorem 적용

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 7은 이 절의 직접 응용이다.
- Exercise 18은 continuous yet nowhere differentiable 현상을 이해하는 이론적 배경이다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 7.17 포함
- [x] Theorem 7.18 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 $f_n(x_0)$의 수렴을 따로 가정해야 하는가?
- 왜 derivative uniform convergence만으로는 충분하지 않은가?
- nowhere differentiable continuous function의 존재가 무엇을 보여 주는가?
