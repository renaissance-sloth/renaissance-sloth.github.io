# 📘 Chapter 3 — Summation by Parts 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 적분의 integration by parts에 대응하는 급수 도구를 소개한다. 핵심 공식은
$$
\sum a_n b_n
$$
형태를 partial sums $A_n$와 차분 $b_n-b_{n+1}$로 바꿔 주는 것이다.

이 도구로 Dirichlet-type test, alternating series test, 경계 위 power series convergence를 얻는다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 3.41

$A_n=\sum_{k=0}^n a_k$, $A_{-1}=0$라 하자. 그러면 $0\le p\le q$에 대해
$$
\sum_{n=p}^q a_n b_n
=\sum_{n=p}^{q-1} A_n(b_n-b_{n+1})+A_qb_q-A_{p-1}b_p.
$$

### ▪ Proof

$$
\sum_{n=p}^q a_n b_n
=\sum_{n=p}^q (A_n-A_{n-1})b_n
=\sum_{n=p}^q A_n b_n-\sum_{n=p-1}^{q-1}A_n b_{n+1},
$$
정리하면 공식이 나온다.

### ▪ Theorem 3.42

다음을 가정하자.

1. partial sums $A_n$이 bounded이다.
2. $b_0\ge b_1\ge b_2\ge\cdots$.
3. $b_n\to0$.

그러면
$$
\sum a_n b_n
$$
은 수렴한다.

### ▪ Proof

$|A_n|\le M$이라 하자. $b_N\le \varepsilon/(2M)$가 되게 $N$을 잡는다. 그러면 $N\le p\le q$에 대해 summation by parts와 단조성으로
$$
\left|\sum_{n=p}^q a_n b_n\right|
\le M\left(\sum_{n=p}^{q-1}(b_n-b_{n+1})+b_q+b_p\right)
=2Mb_p
\le2Mb_N\le\varepsilon.
$$
따라서 Cauchy criterion으로 수렴한다.

### ▪ Theorem 3.43 — Alternating series test

1. $|c_1|\ge |c_2|\ge |c_3|\ge\cdots$
2. $c_{2m-1}\ge0,\ c_{2m}\le0$
3. $c_n\to0$

이면
$$
\sum c_n
$$
은 수렴한다.

### ▪ Proof

$a_n=(-1)^{n+1}$, $b_n=|c_n|$로 두고 Theorem 3.42를 적용한다.

### ▪ Theorem 3.44

$\sum c_n z^n$의 radius of convergence가 1이고,
$$
c_0\ge c_1\ge c_2\ge\cdots,\qquad c_n\to0
$$
라 하자. 그러면 $|z|=1$ 위에서, 아마도 $z=1$만 제외하고는 모든 점에서
$$
\sum c_n z^n
$$
이 수렴한다.

### ▪ Proof

$a_n=z^n$, $b_n=c_n$로 둔다. $|z|=1, z\neq1$이면
$$
\left|\sum_{m=0}^n z^m\right|=
\left|\frac{1-z^{n+1}}{1-z}\right|
\le \frac2{|1-z|},
$$
즉 partial sums가 bounded이다. 이제 Theorem 3.42를 적용하면 된다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 철학은 “복잡한 $a_n b_n$를 한 번 적분 by parts처럼 재배열하면 수렴성이 드러난다”는 것이다. 특히 $A_n$가 bounded이고 $b_n$이 감소하며 0으로 가면, oscillation이 평균적으로 상쇄된다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- alternating series를 판정할 때
- trig/exponential oscillation이 있는 series를 다룰 때
- power series 경계 수렴을 볼 때

### 📌 문제 풀이 패턴
1. partial sums bounded 확인
2. coefficient monotone 감소 확인
3. $b_n\to0$ 확인
4. Theorem 3.42 적용

---

## 🔴 5. 대표 문제 & 풀이 전략

Leibniz alternating series test는 사실 Theorem 3.42의 특수한 경우다. 또 $\sum z^n/n$ 같은 series의 경계 수렴도 여기서 처리된다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 3.41 포함
- [x] Theorem 3.42 포함
- [x] Theorem 3.43 포함
- [x] Theorem 3.44 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- alternating series test가 Theorem 3.42의 special case인 이유를 설명하라.
- $\sum (-1)^n/n$의 수렴을 설명하라.
- $|z|=1, z\ne1$에서 $1+z+\cdots+z^n$가 왜 bounded인지 보이라.
