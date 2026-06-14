# 📘 Chapter 5 — Taylor's Theorem 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

Taylor’s theorem은 smooth function을 polynomial로 근사하는 핵심 정리다.

- 기준점 $\alpha$에서 $n-1$차 Taylor polynomial $P$를 만든다.
- 실제 함수값 $f(\beta)$와 $P(\beta)$의 차이를 remainder term으로 표현한다.
- 이는 mean value theorem의 고차 확장으로 이해할 수 있다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 5.15

$f$가 $[a,b]$에서 real function이고, $n$이 positive integer이며, $f^{(n-1)}$가 $[a,b]$에서 continuous이고 $(a,b)$에서 $f^{(n)}$가 존재한다고 하자. 서로 다른 두 점 $\alpha,\beta\in[a,b]$를 고르고
$$
P(t)=\sum_{k=0}^{n-1}\frac{f^{(k)}(\alpha)}{k!}(t-\alpha)^k
$$
로 두자. 그러면 $\alpha$와 $\beta$ 사이의 어떤 $x$가 존재하여
$$
f(\beta)=P(\beta)+\frac{f^{(n)}(x)}{n!}(\beta-\alpha)^n.
$$

### ▪ Proof

$M$을
$$
f(\beta)=P(\beta)+M(\beta-\alpha)^n
$$
로 정의하고
$$
g(t)=f(t)-P(t)-M(t-\alpha)^n
$$
라 두자. 그러면
$$
g(\alpha)=g'(\alpha)=\cdots=g^{(n-1)}(\alpha)=0,
\qquad
g(\beta)=0.
$$
Mean value theorem을 반복 적용하면 결국 $\alpha$와 $\beta$ 사이 어떤 점 $x$에서
$$
g^{(n)}(x)=0.
$$
그런데
$$
g^{(n)}(t)=f^{(n)}(t)-n!M.
$$
따라서
$$
n!M=f^{(n)}(x),
$$
즉 원하는 remainder formula가 나온다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 정리의 본질은

> 함수 = Taylor polynomial + 오차

라는 분해다. 오차가 정확히 어떤 점에서의 $n$-th derivative로 제어된다는 것이 중요하다. 그래서 derivative bound를 알면 approximation error도 제어할 수 있다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 함수 근사와 error estimate가 필요할 때
- Newton method, convexity, growth estimate를 다룰 때
- 고차 미분이 들어간 존재 증명을 할 때

### 📌 문제 풀이 패턴
1. Taylor polynomial 작성
2. remainder term 형식 확인
3. higher derivative bound로 error estimate

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 15, 17, 18, 20은 모두 Taylor theorem이 핵심이다.
- 특히 Exercise 15의 inequality와 Newton method 관련 exercise들은 remainder를 정확히 써야 한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 5.15 포함
- [x] remainder 구조 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- Taylor polynomial과 remainder를 각각 설명하라.
- 왜 mean value theorem을 반복 적용하는가?
- derivative bound가 error estimate로 어떻게 이어지는가?
