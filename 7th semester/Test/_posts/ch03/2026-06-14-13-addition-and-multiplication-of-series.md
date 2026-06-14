# 📘 Chapter 3 — Addition and Multiplication of Series 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 수렴급수를 실제로 어떻게 연산할 수 있는지를 다룬다.

- 항별 덧셈과 스칼라배는 안전하다.
- 곱셈은 더 미묘해서 Cauchy product를 정의해야 한다.
- 조건수렴 급수의 곱은 발산할 수도 있다.
- 그러나 적어도 하나가 절대수렴하면 곱은 올바르게 수렴한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 3.47

$\sum a_n=A$, $\sum b_n=B$이면
$$
\sum (a_n+b_n)=A+B,
\qquad
\sum c a_n=cA.
$$

### ▪ Proof

partial sums에 대해
$$
A_n+B_n=\sum_{k=0}^n (a_k+b_k)
$$
이고, $A_n\to A$, $B_n\to B$이므로 결과가 따른다.

### ▪ Definition 3.48 — Cauchy product

$$
c_n=\sum_{k=0}^n a_k b_{n-k}
\qquad (n=0,1,2,\dots)
$$
로 두고, $\sum c_n$을 두 급수의 **product**라고 한다.

### ▪ Example 3.49

조건수렴하는 급수
$$
\sum \frac{(-1)^n}{\sqrt{n+1}}
$$
을 자기 자신과 곱하면, Cauchy product의 일반항 $c_n$이 0으로 가지지 않으므로 product series는 발산할 수 있다.

### ▪ Theorem 3.50 — Mertens theorem

다음을 가정하자.

1. $\sum a_n$이 absolutely convergent
2. $\sum a_n=A$
3. $\sum b_n=B$
4. $c_n=\sum_{k=0}^n a_k b_{n-k}$

그러면
$$
\sum c_n=AB.
$$

### ▪ Proof idea

$C_n$을 product partial sums라 하고,
$$
C_n=A_nB+\gamma_n
$$
형태로 분해한다. $A_nB\to AB$이고, 절대수렴 가정으로 $\gamma_n\to0$를 보이면 된다. 핵심은
$$
\alpha=\sum |a_n|<\infty
$$
를 이용해 error term을 uniform하게 제어하는 것이다.

### ▪ Theorem 3.51 — Abel theorem (announced)

$\sum a_n$, $\sum b_n$, $\sum c_n$이 각각 $A,B,C$로 수렴하고
$$
c_n=a_0b_n+\cdots+a_nb_0
$$
이면
$$
C=AB.
$$

이 정리의 간단한 증명은 나중에 power series continuity를 사용해서 Chapter 8에서 제시된다.

---

## 🟢 3. 개념 해설 + 엄밀성

덧셈은 partial sums에 바로 전달되므로 쉽다. 곱셈은 그렇지 않다. 왜냐하면 product partial sums는 단순히 $A_nB_n$가 아니기 때문이다. 바로 이 미묘함 때문에 Cauchy product와 Mertens theorem이 필요하다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 두 급수의 곱을 계산할 때
- power series 곱셈을 정당화할 때
- 적어도 하나의 절대수렴 여부를 확인할 때

### 📌 문제 풀이 패턴
1. 덧셈은 partial sums로 바로 처리
2. 곱은 Cauchy product 정의부터 시작
3. 절대수렴 하나 확보 → Mertens 적용

---

## 🔴 5. 대표 문제 & 풀이 전략

power series를 곱할 때 coefficient가 convolution처럼 나오는 이유가 바로 Cauchy product이다. Chapter 8의 exponential function 계산에서도 이 구조가 반복된다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 3.47 포함
- [x] Definition 3.48 포함
- [x] Example 3.49 포함
- [x] Theorem 3.50 포함
- [x] Theorem 3.51 언급 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 product partial sums는 $A_nB_n$와 같지 않은가?
- Cauchy product 정의를 써서 처음 몇 항을 직접 계산하라.
- 절대수렴 하나가 왜 결정적으로 필요한가?
