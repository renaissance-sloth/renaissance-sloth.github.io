# 📘 Chapter 5 — Mean Value Theorems 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 derivative를 “값 비교”에 연결하는 절이다.

- local extremum에서 derivative가 0이 되는 사실
- generalized mean value theorem
- ordinary mean value theorem
- derivative 부호로 monotonicity를 판정하는 결과

이 절이 끝나면 derivative는 단순 계산 도구가 아니라 함수의 전체적인 모양을 통제하는 도구가 된다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 5.7

metric space $X$ 위 real function $f$가 $p\in X$에서 local maximum을 가진다는 것은, 어떤 $\delta>0$가 존재하여
$$
d(p,q)<\delta \implies f(q)\le f(p)
$$
가 되는 것을 뜻한다. local minimum도 유사하게 정의한다.

### ▪ Theorem 5.8

$f$가 $[a,b]$에 정의되어 있고, $x\in(a,b)$에서 local maximum을 가지며 $f'(x)$가 존재하면
$$
f'(x)=0.
$$
local minimum의 경우도 마찬가지다.

### ▪ Proof

왼쪽에서 $t<x$이면
$$
\frac{f(t)-f(x)}{t-x}\ge0
$$
이고 $t\to x$로 보내면 $f'(x)\ge0$. 오른쪽에서는
$$
\frac{f(t)-f(x)}{t-x}\le0
$$
이므로 $f'(x)\le0$. 따라서 $f'(x)=0$.

### ▪ Theorem 5.9 — Generalized Mean Value Theorem

$f,g$가 $[a,b]$에서 continuous이고 $(a,b)$에서 differentiable이면 어떤 $x\in(a,b)$가 존재하여
$$
[f(b)-f(a)]g'(x)=[g(b)-g(a)]f'(x).
$$

### ▪ Proof

$$
h(t)=[f(b)-f(a)]g(t)-[g(b)-g(a)]f(t)
$$
로 두면 $h(a)=h(b)$. 따라서 Rolle-type argument로 어떤 interior point에서 $h'(x)=0$. 미분하면 식이 나온다.

### ▪ Theorem 5.10 — Mean Value Theorem

$f$가 $[a,b]$에서 continuous, $(a,b)$에서 differentiable이면 어떤 $x\in(a,b)$가 존재하여
$$
f(b)-f(a)=(b-a)f'(x).
$$

### ▪ Proof

Theorem 5.9에서 $g(x)=x$를 택하면 된다.

### ▪ Theorem 5.11

$f$가 $(a,b)$에서 differentiable이라 하자.

1. 모든 $x$에 대해 $f'(x)\ge0$이면 $f$는 increasing
2. 모든 $x$에 대해 $f'(x)=0$이면 $f$는 constant
3. 모든 $x$에 대해 $f'(x)\le0$이면 $f$는 decreasing

### ▪ Proof

임의의 $x_1<x_2$에 대해 mean value theorem으로
$$
f(x_2)-f(x_1)=(x_2-x_1)f'(x)
$$
인 중간점 $x$가 존재한다. 이제 derivative 부호를 보면 결론이 즉시 나온다.

---

## 🟢 3. 개념 해설 + 엄밀성

mean value theorem은 “전체 변화량 = 어떤 한 점의 순간 변화율 × 길이”라는 뜻이다. 이 하나의 등식에서 monotonicity, uniqueness, error estimates가 다 흘러나온다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 함수가 증가/감소하는지 판정할 때
- inverse function 성질을 볼 때
- difference estimate를 얻을 때
- local extremum에서 derivative 조건을 도출할 때

### 📌 문제 풀이 패턴
1. 적당한 $h$를 만들어 Rolle/MVT 적용
2. derivative sign를 global shape로 번역
3. endpoint 차이를 interior derivative로 바꾸기

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 2: $f'(x)>0$이면 strictly increasing, inverse differentiability
- Exercise 3: bounded derivative로 one-to-one 보이기
- Exercise 6: monotone derivative로 quotient monotonicity 제어

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 5.7 포함
- [x] Theorems 5.8–5.11 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- local maximum에서 derivative가 0이 되는 이유를 설명하라.
- generalized MVT와 ordinary MVT의 관계는 무엇인가?
- $f'=0$이면 왜 함수가 constant인가?
