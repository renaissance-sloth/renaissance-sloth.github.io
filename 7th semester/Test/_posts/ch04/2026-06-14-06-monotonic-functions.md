# 📘 Chapter 4 — Monotonic Functions 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 monotone function의 구조를 분석한다.

- monotone function은 좌우 극한이 항상 존재한다.
- 따라서 second kind discontinuity를 가질 수 없다.
- 더 나아가 discontinuity set이 at most countable이라는 매우 강한 결과를 얻는다.

즉 monotonicity는 함수의 불연속을 매우 제한한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 4.28

$f:(a,b)\to\mathbb R$가 있고, $a<x<y<b$이면 항상 $f(x)\le f(y)$이면 monotonically increasing이라고 한다. 부등호를 뒤집으면 decreasing. 둘을 합쳐 monotonic functions라 한다.

### ▪ Theorem 4.29

$f$가 increasing이면 모든 $x\in(a,b)$에서 $f(x+)$, $f(x-)$가 존재하며,
$$
\sup_{a<t<x} f(t)=f(x-)\le f(x)\le f(x+)=\inf_{x<t<b}f(t).
$$
또 $a<x<y<b$이면
$$
f(x+)\le f(y-).
$$

### ▪ Proof idea

왼쪽에서는 $f(x)$가 upper bound가 되므로 $\sup$가 존재한다. 이 supremum을 $A$라 하고, monotonicity를 이용해 $x$의 왼쪽에서 function값이 $A$ 근처에 갇힌다는 것을 보이면 $f(x-)=A$. 오른쪽도 동일하다. 마지막 inequality는 왼쪽 sup와 오른쪽 inf 비교로 나온다.

### ▪ Corollary

monotonic functions는 discontinuity of the second kind를 가지지 않는다.

### ▪ Theorem 4.30

$f$가 $(a,b)$에서 monotonic이면, $f$가 discontinuous인 점들의 집합은 at most countable이다.

### ▪ Proof

명확성을 위해 increasing case만 보자. 불연속점 집합을 $E$라 하자. 각 $x\in E$에 대해
$$
f(x-)<r(x)<f(x+)
$$
를 만족하는 rational number $r(x)$를 하나 고른다. 만약 $x_1<x_2$이면 Theorem 4.29에 의해
$$
f(x_1+)\le f(x_2-),
$$
따라서 같은 rational을 고를 수 없다. 즉 $x\mapsto r(x)$는 $E$를 rationals 안으로 보내는 injective map이다. 유리수는 countable이므로 $E$도 countable이다.

### ▪ Remark 4.31

monotone function의 discontinuities가 isolated일 필요는 없다. 실제로 임의의 countable subset을 정확히 discontinuity set으로 가지는 monotone function을 만들 수 있다. 본문은
$$
f(x)=\sum_{x_n<x} c_n
$$
형태의 고전적 construction을 제시한다.

---

## 🟢 3. 개념 해설 + 엄밀성

monotonicity는 “진동”을 금지한다. 그래서 좌우 극한이 자동으로 존재하고, 거친 second kind discontinuity는 일어나지 못한다. 남을 수 있는 건 jump-type discontinuity뿐이며, 그마저도 countably many밖에 없다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- monotone function의 continuity/discontinuity structure를 분석할 때
- jump discontinuity를 countable하게 세고 싶을 때
- one-sided limit 존재를 보장받고 싶을 때

### 📌 문제 풀이 패턴
1. monotonicity 확인
2. 좌우 sup/inf 정의
3. one-sided limits 존재 도출
4. rational injection으로 discontinuity set countability 증명

---

## 🔴 5. 대표 문제 & 풀이 전략

### Exercise 17과 직접 연결

simple discontinuities가 at most countable이라는 일반 정리가 나오지만, monotone case에서는 훨씬 짧고 구조적인 증명이 된다. 이 절을 이해하면 Exercise 17의 힌트가 왜 rational numbers를 쓰는지 바로 보인다.

### Exercise 16과 간접 연결

floor function과 fractional part는 monotonicity와 jump discontinuity의 대표 예시다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 4.28 포함
- [x] Theorem 4.29 포함
- [x] corollary 포함
- [x] Theorem 4.30 포함
- [x] Remark 4.31 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 monotone function은 second kind discontinuity를 가질 수 없는가?
- 왜 discontinuity set이 countable인가?
- floor function의 discontinuity 구조를 이 절의 언어로 설명하라.
