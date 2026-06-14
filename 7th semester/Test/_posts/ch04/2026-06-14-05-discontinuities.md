# 📘 Chapter 4 — Discontinuities 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 연속이 깨지는 방식을 분류한다.

- right-hand / left-hand limits를 정의한다.
- discontinuity of the first kind와 second kind를 구분한다.
- 전형적인 예시들을 통해 분류 감각을 만든다.

이 절은 뒤의 monotonic function 절과 exercise 17, 18을 위한 직접 준비다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 4.25 — One-sided limits

$f$가 $(a,b)$에 정의되어 있을 때, $a\le x<b$에 대해
$$
f(x+)=q
$$
라는 것은 $(x,b)$ 안의 모든 sequence $t_n\to x$에 대해 $f(t_n)\to q$라는 뜻이다.

유사하게 $a<x\le b$에 대해 $f(x-)$를 정의한다.

그리고
$$
\lim_{t\to x}f(t)
$$
가 존재하는 것은 precisely
$$
f(x+)=f(x-)
$$
일 때이다.

### ▪ Definition 4.26 — Types of discontinuities

$f$가 $(a,b)$에 정의되어 있고 $x$에서 discontinuous라 하자.

- 만약 $f(x+)$와 $f(x-)$가 존재하면, $x$는 **discontinuity of the first kind** 또는 **simple discontinuity**이다.
- 그렇지 않으면 **discontinuity of the second kind**이다.

simple discontinuity는 두 방식으로 생긴다.

1. $f(x+)\ne f(x-)$
2. $f(x+)=f(x-)\ne f(x)$

### ▪ Examples 4.27

1. 
   $$
   f(x)=\begin{cases}1 & x\in\mathbb Q,\\0 & x\notin\mathbb Q.\end{cases}
   $$
   모든 점에서 second kind discontinuity.

2. 
   $$
   f(x)=\begin{cases}x & x\in\mathbb Q,\\0 & x\notin\mathbb Q.\end{cases}
   $$
   $x=0$에서는 continuous, 다른 모든 점에서는 second kind discontinuity.

3. piecewise linear example은 $x=0$에서 simple discontinuity를 가진다.

4. 
   $$
   f(x)=\begin{cases}\sin(1/x) & x\ne0,\\0 & x=0.\end{cases}
   $$
   $x=0$에서 one-sided limits가 존재하지 않으므로 second kind discontinuity.

---

## 🟢 3. 개념 해설 + 엄밀성

한쪽 극한이 존재한다는 것은 “오른쪽/왼쪽에서 접근할 때는 안정된 값이 있다”는 뜻이다. 그래서 simple discontinuity는 그래도 비교적 얌전한 불연속이다. 반면 second kind discontinuity는 좌우 진동, 무한발산, irrational/rational oscillation처럼 훨씬 거칠다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- piecewise-defined function의 연속성 판정
- rational/irrational 정의 함수 분류
- monotone function 불연속점 구조 분석

### 📌 문제 풀이 패턴
1. 오른쪽/왼쪽 limit를 각각 계산
2. 존재 여부 확인
3. 서로 같은지, 함수값과 같은지 비교

---

## 🔴 5. 대표 문제 & 풀이 전략

### Exercise 18과 직접 연결

Thomae-type 함수는 irrational 점에서는 continuous, rational 점에서는 simple discontinuity를 가진다. 이 절의 분류를 정확히 이해해야 풀 수 있다.

### Example 4.27(d)의 의미

$\sin(1/x)$는 “중간값 성질 같은 단순 직관만으로 continuity를 판단하면 안 된다”는 경고 역할도 한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 4.25 포함
- [x] Definition 4.26 포함
- [x] Examples 4.27 포함
- [x] one-sided limit와 discontinuity 분류 설명 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- simple discontinuity와 second kind discontinuity의 차이를 설명하라.
- $\sin(1/x)$가 왜 0에서 second kind discontinuity인지 설명하라.
- 한쪽 극한이 존재해도 함수가 continuous가 아닐 수 있는 이유는 무엇인가?
