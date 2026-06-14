# 📘 Chapter 3 — Rearrangements 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 조건수렴 급수의 위험성을 정면으로 보여 준다.

- rearrangement를 정의한다.
- 조건수렴 급수는 순서를 바꾸면 합이 달라질 수 있음을 본다.
- 심지어 liminf, limsup를 원하는 대로 만들 수 있다는 Riemann rearrangement theorem을 제시한다.
- 반대로 절대수렴 급수는 어떤 rearrangement를 해도 같은 합을 가진다는 정리를 증명한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 3.52

모든 양의 정수를 정확히 한 번씩 나열한 수열 $\{k_n\}$에 대해
$$
a_n'=a_{k_n}
$$
로 두면, $\sum a_n'$을 $\sum a_n$의 **rearrangement**라고 한다.

### ▪ Example 3.53

alternating harmonic series
$$
1-\frac12+\frac13-\frac14+\cdots
$$
의 항들을 두 개의 양수 뒤에 하나의 음수가 오도록 재배열하면, 원래 합과 다른 값을 향하게 된다. 즉 조건수렴 급수는 순서에 민감하다.

### ▪ Theorem 3.54 — Riemann rearrangement theorem

$\sum a_n$이 실수들의 급수이고, 수렴하지만 절대수렴하지는 않는다고 하자. 또
$$
-\infty\le \alpha\le \beta\le \infty
$$
라 하자. 그러면 어떤 rearrangement를 취하면 그 partial sums $s_n'$에 대해
$$
\liminf s_n'=\alpha,
\qquad
\limsup s_n'=\beta
$$
가 되게 만들 수 있다.

### ▪ Proof idea

양수 부분과 음수 부분의 절댓값을 따로 떼어내면 둘 다 발산해야 한다. 그렇지 않으면 절대수렴이 되어 버리기 때문이다. 이제 양수 항을 충분히 더해 $\beta_n$을 넘고, 음수 항을 충분히 더해 $\alpha_n$ 아래로 내려가게 하는 과정을 반복하면 원하는 $\alpha,\beta$를 만든다.

### ▪ Theorem 3.55

$\sum a_n$이 absolutely convergent complex series이면, 그 모든 rearrangement는 수렴하고, 모두 같은 sum으로 수렴한다.

### ▪ Proof

rearranged partial sums를 $s_n'$, 원래 partial sums를 $s_n$라 하자. 절대수렴이므로 꼬리 절댓값 합이 작다:
$$
\sum_{i=n}^m |a_i|\le \varepsilon
$$
for sufficiently large indices. rearrangement의 충분히 뒤에서는 앞의 유한 개 항이 모두 이미 등장했으므로, 원래 partial sum과 rearranged partial sum의 차이는 tail 부분에서만 생긴다. 따라서
$$
|s_n-s_n'|\le \varepsilon
$$
가 되고, 결국 rearranged series도 같은 sum으로 수렴한다.

---

## 🟢 3. 개념 해설 + 엄밀성

조건수렴은 “부호 상쇄 덕분에 겨우 수렴하는” 상태다. 그래서 순서를 바꾸면 상쇄 방식이 바뀌어 합도 바뀐다. 반면 절대수렴은 상쇄에 의존하지 않으므로 순서가 바뀌어도 안전하다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 조건수렴과 절대수렴을 구분해야 할 때
- rearrangement가 허용되는지 판단할 때
- 무한급수 연산의 안정성을 설명할 때

### 📌 문제 풀이 패턴
1. 먼저 absolute convergence 여부를 본다.
2. 절대수렴이면 rearrangement 안전.
3. 조건수렴이면 순서 변경 매우 위험.

---

## 🔴 5. 대표 문제 & 풀이 전략

alternating harmonic series는 이 절 전체의 대표 예시다. 실제 계산에서 급수 전개를 마음대로 재배열해도 되는지 먼저 확인해야 하는 이유가 바로 여기에 있다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 3.52 포함
- [x] Example 3.53 포함
- [x] Theorem 3.54 포함
- [x] Theorem 3.55 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 절대수렴 급수는 재배열해도 안전한가?
- 왜 조건수렴 급수는 순서가 중요해지는가?
- alternating harmonic series를 대표 예시로 설명하라.
