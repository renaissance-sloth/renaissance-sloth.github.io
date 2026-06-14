# 📘 Chapter 3 — The Root and Ratio Tests 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 급수 판정법의 대표 선수 둘을 소개한다.

- Root Test
- Ratio Test

둘 다 결국 항의 크기가 **기하급수적으로 줄어드는지**를 판정하는 도구다. 그리고 마지막에는 두 판정법의 세기를 비교한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 3.33 — Root Test

series $\sum a_n$에 대해
$$
\alpha=\limsup_{n\to\infty}\sqrt[n]{|a_n|}
$$
로 두자. 그러면

1. $\alpha<1$이면 $\sum a_n$은 수렴한다.
2. $\alpha>1$이면 $\sum a_n$은 발산한다.
3. $\alpha=1$이면 이 test는 결론을 주지 않는다.

### ▪ Proof

**(1)** $\alpha<1$이면 $\alpha<\beta<1$인 $\beta$를 택할 수 있다. Theorem 3.17(b)에 의해 충분히 큰 $n$에서는
$$
\sqrt[n]{|a_n|}<\beta,
$$
즉
$$
|a_n|<\beta^n.
$$
그런데 $\sum \beta^n$은 geometric series이므로 수렴한다. comparison test로 $\sum a_n$이 수렴한다.

**(2)** $\alpha>1$이면 $\sqrt[n_k]{|a_{n_k}|}\to\alpha$인 subsequence를 잡을 수 있다. 따라서 무한히 많은 $n$에 대해 $|a_n|>1$, 특히 $a_n\to0$가 성립하지 않는다. Theorem 3.23에 의해 급수는 발산한다.

**(3)** $\alpha=1$일 때는 두 반례를 보면 된다.
$$
\sum \frac1n\quad \text{(발산)},
\qquad
\sum \frac1{n^2}\quad \text{(수렴)}.
$$
둘 다 $\alpha=1$이다.

### ▪ Theorem 3.34 — Ratio Test

1. 
   $$
   \limsup_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|<1
   $$
   이면 $\sum a_n$은 수렴한다.

2. 어떤 고정된 $n_0$ 이후로 항상
   $$
   \left|\frac{a_{n+1}}{a_n}\right|\ge1
   $$
   이면 $\sum a_n$은 발산한다.

### ▪ Proof

**(1)** $\beta<1$와 충분히 큰 $N$이 있어
$$
\left|\frac{a_{n+1}}{a_n}\right|<\beta
\qquad(n\ge N)
$$
라 하자. 그러면 반복해서
$$
|a_{N+p}|<\beta^p|a_N|.
$$
즉 충분히 뒤에서는 $|a_n|$가 geometric sequence보다 더 빨리 작아진다. 따라서 comparison test로 수렴.

**(2)** 어떤 시점 이후로 $|a_{n+1}|\ge |a_n|$이면, 뒤쪽 항들의 크기가 더 이상 0으로 가지지 못한다. 따라서 necessary condition $a_n\to0$이 깨지고, 급수는 발산한다.

### ▪ Remarks 3.35–3.36

- ratio test는 계산이 쉬운 경우가 많다.
- root test는 더 넓은 범위를 포괄한다.
- 둘 다 divergence에 대해서는 사실상 $a_n\to0$ 실패를 통해 결론내린다.

### ▪ Theorem 3.37

양수수열 $\{c_n\}$에 대해
$$
\liminf \frac{c_{n+1}}{c_n}
\le
\liminf \sqrt[n]{c_n},
\qquad
\limsup \sqrt[n]{c_n}
\le
\limsup \frac{c_{n+1}}{c_n}.
$$

### ▪ Proof idea

본문은 두 번째 부등식을 증명한다. $\alpha=\limsup c_{n+1}/c_n$라 두고, $\beta>\alpha$를 택하면 결국
$$
c_n\le C\beta^n
$$
형태의 estimate를 얻는다. 그러면
$$
\sqrt[n]{c_n}\le \sqrt[n]{C}\,\beta
$$
이므로 limsup이 $\beta$ 이하이고, $\beta>\alpha$ arbitrary로부터 결론이 나온다.

---

## 🟢 3. 개념 해설 + 엄밀성

### root test의 철학

$\sqrt[n]{|a_n|}$는 항 $|a_n|$가 대략 어느 비율의 geometric decay를 가지는지 보는 도구다. 만약 이 값이 1보다 작으면, 결국 $|a_n|$는 $\beta^n$보다 작아진다.

### ratio test의 철학

$|a_{n+1}/a_n|$는 연속된 항 사이의 상대 비율이다. 이게 eventually 1보다 작으면 항들은 geometric하게 감소한다.

### 왜 $=1$이면 실패하는가

경계선에서는 양쪽 사례가 모두 가능하다. 즉 test가 충분히 미세하지 않다. 그래서 다른 판정법이 필요하다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- factorial, power, exponential이 섞인 급수일 때
- power series의 radius of convergence를 잡을 때
- 비교판정을 직접 쓰기 번거로울 때

### 📌 문제 풀이 패턴

1. **ratio first pattern**  
   factorial이 보이면 ratio test를 먼저 의심한다.

2. **root first pattern**  
   $n$승, $c_n^n$ 구조가 보이면 root test를 쓴다.

3. **boundary failure awareness**  
   결과가 1이면 멈추고 다른 test로 넘어간다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### power series와 직접 연결

다음 절의 radius of convergence는 결국 root test를 coefficient에 적용한 것이다. 따라서 이 절은 power series의 바로 전 준비 절이다.

### 대표 예시

- $\sum z^n/n!$: ratio test가 매우 쉽다.
- $\sum 1/n^p$: root test나 ratio test는 경계에서 약할 수 있다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 3.33 포함
- [x] Theorem 3.34 포함
- [x] Remarks 요지 포함
- [x] Theorem 3.37 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

### 개념 확인 질문

1. root test는 왜 결국 geometric series와의 비교인가?
2. ratio test가 계산상 쉬운 이유는 무엇인가?
3. test 값이 1이면 왜 결론을 못 내리는가?

### 간단한 훈련 문제

1. $\sum 1/n!$에 ratio test를 적용하라.
2. $\sum (3/4)^n$에 root test를 적용하라.
3. $\sum 1/n$과 $\sum 1/n^2$가 왜 둘 다 경계값 1을 주는지 확인하라.
