# 📘 Chapter 8 — The Exponential and Logarithmic Functions 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 power series로부터 exponential function을 만들고, inverse로 logarithm을 정의하며, 복소지수와 삼각함수까지 연결한다.

- $E(z)=\sum z^n/n!$ 정의
- addition formula $E(z+w)=E(z)E(w)$
- real exponential $e^x$의 미분, 단조성, 성장성
- logarithm $L$의 inverse 정의와 $L'(y)=1/y$
- 복소지수의 주기성과 unit circle parameterization

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Exponential series

$$
E(z)=\sum_{n=0}^{\infty}\frac{z^n}{n!}
$$
는 모든 complex $z$에서 수렴한다.

absolute convergence와 Cauchy product를 사용하면
$$
E(z+w)=E(z)E(w)
$$
를 얻는다. 특히
$$
E(z)E(-z)=1.
$$

### ▪ Theorem 8.6

real line 위에서 $e^x$에 대해

1. $e^x$는 모든 $x$에서 continuous and differentiable
2. $(e^x)'=e^x$
3. strictly increasing and positive
4. $e^{x+y}=e^x e^y$
5. $x\to+\infty$이면 $e^x\to+\infty$, $x\to-\infty$이면 $e^x\to0$
6. 모든 $n$에 대해
   $$
   x^n e^{-x}\to0
   \qquad (x\to+\infty)
   $$

### ▪ Logarithm

$e^x$는 strictly increasing이므로 inverse $L$을 가진다. domain은 $(0,\infty)$이고,
$$
L(e^x)=x,
\qquad
E(L(y))=y.
$$
chain rule로 미분하면
$$
L'(y)=\frac1y
\qquad (y>0).
$$
또 $L(1)=0$이므로
$$
L(y)=\int_1^y \frac{dx}{x}.
$$

### ▪ Theorem 8.7

복소지수와 삼각함수에 대해

1. $E$는 period $2\pi i$를 가진다.
2. cosine/sine은 period $2\pi$.
3. $0<t<2\pi$이면 $E(it)\ne1$.
4. $|z|=1$인 모든 complex number는 유일한 $t\in[0,2\pi)$에 대해 $E(it)=z$로 쓸 수 있다.

즉 unit circle이 $e^{it}$로 parameterize된다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 중요한 포인트는 exponential과 logarithm을 별도 가정 없이 **power series와 inverse function theorem**으로부터 구축한다는 점이다. 또 복소지수 $e^{it}$가 unit circle geometry와 즉시 연결되면서, 해석학·기하·삼각함수가 한 줄로 이어진다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 지수/로그의 기본 미분공식을 쓸 때
- growth comparison을 할 때
- unit circle parameterization을 쓸 때
- later Fourier analysis에서 $e^{inx}$를 다룰 때

### 📌 문제 풀이 패턴
1. exponential series에서 직접 출발
2. addition formula로 구조 만들기
3. inverse function으로 log 도출
4. complex case는 unit circle와 연결

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 4, 5, 6은 이 절의 직접 응용이다.
- 특히 $(1+x)^{1/x}\to e$, $\log(1+x)/x\to1$, multiplicative Cauchy-type equation 문제들은 여기의 성질을 자유롭게 써야 한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] exponential series와 addition formula 포함
- [x] Theorems 8.6, 8.7 포함
- [x] logarithm inverse construction 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 $E(z+w)=E(z)E(w)$가 중요한가?
- $L'(y)=1/y$를 어떻게 얻는가?
- unit circle의 모든 점이 $e^{it}$ 꼴이라는 말은 무슨 뜻인가?
