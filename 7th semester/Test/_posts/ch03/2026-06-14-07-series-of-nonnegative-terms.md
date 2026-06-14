# 📘 Chapter 3 — Series of Nonnegative Terms 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 **비음수 항 급수**에 대한 표준 모델들을 정리한다.

- geometric series
- Cauchy condensation test
- p-series
- logarithmic correction이 들어간 표준 borderline series

이 절의 역할은 매우 실전적이다. 앞으로 나오는 대부분의 비교판정은 결국 이 절의 몇 개 대표급수와 비교하는 방식으로 돌아간다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 3.26 — Geometric series

$0\le x<1$이면
$$
\sum_{n=0}^{\infty}x^n=\frac1{1-x}.
$$
$x\ge1$이면 급수는 발산한다.

### ▪ Proof

$x\neq1$일 때 partial sum은
$$
s_n=\sum_{k=0}^n x^k=\frac{1-x^{n+1}}{1-x}.
$$
$0\le x<1$이면 $x^{n+1}\to0$이므로
$$
s_n\to \frac1{1-x}.
$$
$x=1$이면
$$
1+1+1+\cdots
$$
이므로 발산한다. $x>1$이면 일반항조차 0으로 가지 않으므로 역시 발산한다.

### ▪ Theorem 3.27 — Cauchy condensation test

$$
a_1\ge a_2\ge a_3\ge\cdots\ge0
$$
라고 하자. 그러면
$$
\sum_{n=1}^{\infty}a_n
$$
이 수렴할 필요충분조건은
$$
\sum_{k=0}^{\infty}2^ka_{2^k}
$$
이 수렴하는 것이다.

### ▪ Proof

partial sums를
$$
s_n=a_1+\cdots+a_n,
\qquad
t_k=a_1+2a_2+\cdots+2^ka_{2^k}
$$
로 두자.

단조감소 조건 때문에 각 dyadic block에서 항들을 한꺼번에 estimate할 수 있다.

- $n<2^k$이면
  $$
  s_n\le t_k.
  $$
- $n>2^k$이면
  $$
  2s_n\ge t_k.
  $$

따라서 $\{s_n\}$과 $\{t_k\}$는 둘 다 bounded이거나 둘 다 unbounded이다. Theorem 3.24에 의해 두 급수의 수렴성이 동치가 된다.

### ▪ Theorem 3.28 — p-series

$$
\sum \frac1{n^p}
$$
는 $p>1$이면 수렴하고, $p\le1$이면 발산한다.

### ▪ Proof

- $p\le0$이면 일반항이 0으로 가지 않으므로 발산.
- $p>0$이면 condensation test를 적용하면
  $$
  \sum 2^k\cdot \frac1{2^{kp}}=\sum 2^{(1-p)k}
  $$
  로 바뀐다.
- 이것은 geometric series이므로 $2^{1-p}<1$, 즉 $p>1$일 때만 수렴한다.

### ▪ Theorem 3.29

$p>1$이면
$$
\sum_{n=2}^{\infty}\frac1{n(\log n)^p}
$$
는 수렴하고, $p\le1$이면 발산한다.

### ▪ Proof

$1/[n(\log n)^p]$는 충분히 뒤에서 단조감소하므로 condensation test를 적용한다. 그러면
$$
\sum_{k=1}^{\infty}2^k\cdot \frac1{2^k(\log 2^k)^p}
=\sum_{k=1}^{\infty}\frac1{(k\log2)^p}
=\frac1{(\log2)^p}\sum_{k=1}^{\infty}\frac1{k^p}.
$$
이제 Theorem 3.28로 결론이 나온다.

### ▪ Remark

이 절차를 계속 반복하면
$$
\sum \frac1{n\log n\log\log n}
$$
처럼 아주 천천히 감소하는 발산급수와,
$$
\sum \frac1{n\log n(\log\log n)^2}
$$
처럼 거의 구별되지 않지만 수렴하는 급수를 얻을 수 있다. 즉 convergence/divergence의 경계는 매우 섬세하다.

---

## 🟢 3. 개념 해설 + 엄밀성

### 왜 geometric series가 기준급수인가

지수적으로 줄어드는 항은 너무 빨리 작아져서 항상 수렴한다. 그래서 많은 복잡한 급수를 결국 geometric type과 비교하려고 한다.

### condensation test의 직관

감소하는 양의 급수에서는 항을 하나하나 다 보는 대신, 길이가 1,2,4,8,\dots인 block으로 묶어서 봐도 본질이 바뀌지 않는다. 이게 Cauchy condensation test의 철학이다.

### p-series가 왜 핵심 경계인가

$$
\sum \frac1n
$$
은 발산, $\sum 1/n^2$는 수렴. 즉 지수가 1을 넘느냐가 첫 번째 중요한 경계선이다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- 양의 항 급수의 수렴/발산을 빠르게 판정할 때
- logarithmic correction이 달린 급수의 경계를 볼 때
- comparison test의 기준급수를 정할 때

### 📌 문제 풀이 패턴

1. **geometric comparison**  
   결국 $Cr^n$ 꼴로 눌리면 수렴.

2. **p-series comparison**  
   결국 $1/n^p$와 비교해 판정.

3. **condensation pattern**  
   감소하는 양의 급수면 $2^ka_{2^k}$로 바꿔 본다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### 표준 판정 표

- $\sum x^n$: $|x|<1$이면 수렴
- $\sum 1/n^p$: $p>1$이면 수렴
- $\sum 1/[n(\log n)^p]$: $p>1$이면 수렴

이 세 줄은 실제 문제 풀이에서 거의 암기 도구처럼 쓰인다.

### Chapter 3와의 연결

뒤의 root test, ratio test, power series convergence 논리도 결국 geometric series와 비교하는 구조를 갖는다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 3.26 포함
- [x] Theorem 3.27 포함
- [x] Theorem 3.28 포함
- [x] Theorem 3.29 포함
- [x] 핵심 remark 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

### 개념 확인 질문

1. condensation test는 왜 감소하는 양의 항 급수에서만 쓰는가?
2. $p=1$이 왜 중요한 경계선인가?
3. $\sum 1/[n(\log n)^p]$의 경계가 왜 $p=1$인가?

### 간단한 훈련 문제

1. $\sum (1/3)^n$의 합을 구하라.
2. $\sum 1/n^{3/2}$의 수렴 여부를 판정하라.
3. $\sum 1/[n(\log n)^2]$의 수렴 여부를 판정하라.
