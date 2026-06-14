# 📘 Chapter 3 — Absolute Convergence 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 “절댓값을 씌운 급수까지 수렴하면 원래 급수는 얼마나 잘 behaved한가?”를 다룬다. 절대수렴은 조건수렴보다 훨씬 강하며, 이후의 곱셈·재배열 정리를 가능하게 만든다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

series $\sum |a_n|$이 수렴하면 $\sum a_n$이 **converge absolutely**한다고 한다.

### ▪ Theorem 3.45

$\sum a_n$이 absolutely convergent이면 $\sum a_n$은 수렴한다.

### ▪ Proof

$$
\left|\sum_{k=n}^m a_k\right|\le \sum_{k=n}^m |a_k|
$$
이고, 오른쪽 꼬리합이 Cauchy criterion으로 0에 가까워지므로 왼쪽도 작아진다. 따라서 $\sum a_n$은 수렴한다.

### ▪ Remarks 3.46

- 양의 항 급수에서는 absolute convergence와 convergence가 같다.
- $\sum a_n$은 수렴하지만 $\sum |a_n|$은 발산하면 **nonabsolute convergence** 또는 조건수렴이라고 한다.
- 예: $\sum (-1)^n/n$은 조건수렴한다.
- comparison/root/ratio test는 사실상 절대수렴 판정법이다.
- power series는 convergence circle의 내부에서 절대수렴한다.

---

## 🟢 3. 개념 해설 + 엄밀성

절대수렴은 “부호 상쇄 없이도 수렴한다”는 뜻이라 매우 강하다. 그래서 연산 안정성이 좋다. 반면 조건수렴은 섬세해서 순서를 바꾸면 합이 달라질 수도 있다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 급수의 연산 안정성을 확보하고 싶을 때
- 비교/root/ratio test를 적용할 때
- Cauchy product나 rearrangement 정리의 가정을 확인할 때

### 📌 문제 풀이 패턴
1. 먼저 $\sum |a_n|$를 판정한다.
2. 되면 원급수 수렴은 자동.
3. 이후 곱, 재배열 등에 적용한다.

---

## 🔴 5. 대표 문제 & 풀이 전략

Chapter 3 Exercise 13은 바로 “두 absolutely convergent series의 Cauchy product가 absolutely convergent”임을 보이는 문제라 이 절의 직접 연장이다.

---

## ⚫ 6. 섹션 체크리스트

- [x] absolute convergence 정의 포함
- [x] Theorem 3.45 포함
- [x] Remarks 3.46 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 절대수렴이면 원급수가 수렴하는가?
- 조건수렴과 절대수렴의 차이를 설명하라.
- $\sum (-1)^n/n$이 왜 절대수렴하지 않는가?
