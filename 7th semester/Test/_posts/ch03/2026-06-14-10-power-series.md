# 📘 Chapter 3 — Power Series 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절에서는 급수에 변수 $z$를 넣은
$$
\sum c_n z^n
$$
형태를 다룬다. 핵심은 “어떤 $z$에서는 수렴하고, 어떤 $z$에서는 발산하는가?”이다.

- power series를 정의한다.
- root test를 계수 $c_n$에 적용하여 **radius of convergence**를 구한다.
- 내부에서는 수렴, 외부에서는 발산한다는 원리를 얻는다.

이 절은 Chapter 8 전체의 입구다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 3.38

복소수열 $\{c_n\}$가 주어졌을 때
$$
\sum_{n=0}^{\infty} c_n z^n
$$
을 **power series**라고 한다. $c_n$은 coefficient, $z$는 complex number이다.

일반적으로 이 series는 $z$의 값에 따라 수렴하거나 발산한다.

### ▪ Theorem 3.39

power series $\sum c_n z^n$에 대해
$$
\alpha=\limsup_{n\to\infty}\sqrt[n]{|c_n|},
\qquad
R=\frac1\alpha
$$
라 두자. ($\alpha=0$이면 $R=+\infty$, $\alpha=+\infty$이면 $R=0$.) 그러면

- $|z|<R$이면 수렴하고
- $|z|>R$이면 발산한다.

### ▪ Proof

$a_n=c_n z^n$로 두고 root test를 적용하면
$$
\limsup_{n\to\infty}\sqrt[n]{|a_n|}
=|z|\limsup_{n\to\infty}\sqrt[n]{|c_n|}
=\frac{|z|}{R}.
$$
따라서 $|z|/R<1$, 즉 $|z|<R$이면 수렴, $|z|/R>1$, 즉 $|z|>R$이면 발산한다.

### ▪ Remark

숫자 $R$을 **radius of convergence**라고 한다. 경계 $|z|=R$ 위의 거동은 훨씬 섬세해서 일반 원리 하나로는 결정되지 않는다.

### ▪ Examples 3.40

1. $\sum n^n z^n$: $R=0$
2. $\sum z^n/n!$: $R=+\infty$
3. $\sum z^n$: $R=1$, 경계 $|z|=1$에서는 발산
4. $\sum z^n/n$: $R=1$, $z=1$에서는 발산, 다른 일부 경계점에서는 수렴
5. $\sum z^n/n^2$: $R=1$, $|z|=1$의 모든 점에서 수렴

---

## 🟢 3. 개념 해설 + 엄밀성

power series의 핵심은 “수렴 영역이 원판 모양으로 정리된다”는 점이다. 일반 급수는 항마다 복잡할 수 있지만, power series는 계수 $c_n$와 $|z|^n$의 결합 때문에 root test가 정확히 들어맞는다.

즉 문제는 결국 $z$의 위상보다 $|z|$의 크기 비교로 내려온다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- power series의 수렴 반경을 구할 때
- Chapter 8의 special functions를 급수로 다룰 때
- 함수의 국소적 표현을 준비할 때

### 📌 문제 풀이 패턴
1. 계수에 root test 적용
2. 또는 factorial이 있으면 ratio test 사용
3. 경계 $|z|=R$는 따로 개별 분석

---

## 🔴 5. 대표 문제 & 풀이 전략

Chapter 3 Exercise 9, 10은 이 절의 직접 응용이다. 핵심은 항상
$$
R=\frac1{\limsup \sqrt[n]{|c_n|}}
$$
또는 ratio test로 $R$를 구하는 것이다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 3.38 포함
- [x] Theorem 3.39 포함
- [x] Examples 3.40 포함
- [x] 수렴반경 설명 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- $\sum 2^n z^n$의 radius of convergence를 구하라.
- $\sum z^n/n!$에서 ratio test가 왜 쉬운지 설명하라.
- 경계 $|z|=R$에서 왜 따로 분석이 필요한가?
