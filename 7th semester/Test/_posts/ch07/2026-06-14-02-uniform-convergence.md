# 📘 Chapter 7 — Uniform Convergence 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 Chapter 7의 중심 개념인 uniform convergence를 정의하고, 그 기본 판정법들을 세운다.

- uniform convergence 정의
- Cauchy criterion
- sup norm criterion
- Weierstrass M-test

이 절을 이해하면 “pointwise보다 얼마나 강한 조건인지”를 정확히 말할 수 있다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 7.7

함수열 $\{f_n\}$이 집합 $E$에서 함수 $f$로 uniformly converge한다는 것은, 모든 $\varepsilon>0$에 대해 어떤 $N$이 존재하여
$$
n\ge N \implies |f_n(x)-f(x)|\le \varepsilon
$$
가 모든 $x\in E$에 대해 동시에 성립하는 것이다.

pointwise convergence와의 차이는, 여기서 $N$이 $x$에 의존하지 않는다는 점이다.

### ▪ Theorem 7.8 — Cauchy criterion

$\{f_n\}$이 $E$에서 uniformly converge할 필요충분조건은, 모든 $\varepsilon>0$에 대해 어떤 $N$이 존재하여
$$
m,n\ge N \implies |f_n(x)-f_m(x)|\le \varepsilon
$$
가 모든 $x\in E$에 대해 성립하는 것이다.

### ▪ Proof

한 방향은 usual triangle inequality. 역방향은 각 점에서 Cauchy라서 pointwise limit $f$를 만들고, $m\to\infty$를 보내 uniform estimate를 얻는다.

### ▪ Theorem 7.9

pointwise convergence $f_n\to f$를 가정하고
$$
M_n=\sup_{x\in E}|f_n(x)-f(x)|
$$
로 두면,
$$
f_n\to f\text{ uniformly }
\iff M_n\to0.
$$

### ▪ Theorem 7.10 — Weierstrass M-test

$|f_n(x)|\le M_n$ for all $x\in E$, and $\sum M_n$ convergent이면
$$
\sum f_n
$$
은 $E$에서 uniformly converge한다.

### ▪ Proof

꼬리합에 대해
$$
\left|\sum_{i=n}^m f_i(x)\right|\le \sum_{i=n}^m M_i,
$$
오른쪽이 $n,m\to\infty$에서 0으로 가므로 Cauchy criterion으로 uniform convergence.

---

## 🟢 3. 개념 해설 + 엄밀성

uniform convergence는 “그래프 전체가 한 번에 붙는다”는 개념이다. 그래서 좋은 성질을 보존할 가능성이 생긴다. M-test는 특히 가장 실전적인 판정법으로, 절대값을 majorize하는 수치급수만 찾으면 uniform convergence를 얻을 수 있다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 함수급수의 수렴을 강하게 보이고 싶을 때
- limit와 continuity/integral을 교환할 준비를 할 때
- explicit majorant가 있을 때

### 📌 문제 풀이 패턴
1. sup norm으로 직접 계산
2. Cauchy criterion 사용
3. M-test용 수치급수 찾기

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 1, 2는 uniform convergence 기본 성질
- Exercise 11은 M-test와 Dirichlet형 아이디어의 혼합

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 7.7 포함
- [x] Theorems 7.8–7.10 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- uniform convergence에서 왜 $N$이 $x$에 의존하지 않는가?
- M-test는 왜 강력한가?
- sup norm criterion을 직접 예시에 적용해 보라.
