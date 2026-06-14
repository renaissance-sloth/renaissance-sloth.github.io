# 📘 Chapter 8 — Power Series 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 Chapter 3의 power series 수렴반경 이론을 한 단계 더 밀어붙여, **power series가 실제로 매우 잘 behaved한 함수**라는 사실을 보여준다.

- 수렴구간 안에서 uniform convergence
- 항별 미분 가능
- 모든 고계도함수 존재
- 계수와 도함수의 정확한 관계
- power series expansion의 유일성

즉 power series는 단순한 급수가 아니라, **무한히 미분 가능한 analytic object**임을 보여 주는 절이다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Power series setup

$$
f(x)=\sum_{n=0}^{\infty} c_n x^n
\qquad\text{or more generally}\qquad
f(x)=\sum_{n=0}^{\infty} c_n (x-a)^n
$$
를 power series라 한다. 이 절에서는 real variable case에 집중한다.

### ▪ Theorem 8.1

$$
\sum_{n=0}^{\infty} c_n x^n
$$
이 $|x|<R$에서 수렴한다고 하자. 그리고
$$
f(x)=\sum_{n=0}^{\infty} c_n x^n.
$$
그러면

1. 모든 $\varepsilon>0$에 대해 $[-R+\varepsilon,R-\varepsilon]$에서 uniformly converge한다.
2. $f$는 $(-R,R)$에서 continuous이고 differentiable이다.
3. derivative는 항별 미분으로 주어진다:
   $$
   f'(x)=\sum_{n=1}^{\infty} n c_n x^{n-1}
   \qquad (|x|<R).
   $$

### ▪ Proof idea

수렴반경 내부의 조금 작은 닫힌 구간에서는 Weierstrass M-test로 uniform convergence를 얻는다. derivative series도 같은 수렴반경을 가지므로 Chapter 7의 term-by-term differentiation 정리를 적용할 수 있다.

### ▪ Corollary

모든 고계도함수가 존재하며
$$
f^{(k)}(x)=\sum_{n=k}^{\infty} n(n-1)\cdots(n-k+1)c_n x^{n-k}.
$$
특히
$$
f^{(k)}(0)=k!c_k.
$$

### ▪ Theorem 8.2

$\sum c_n$이 수렴하고
$$
f(x)=\sum_{n=0}^{\infty} c_n x^n
\qquad (-1<x<1)
$$
라 하자. 그러면
$$
\lim_{x\to1^-} f(x)=\sum_{n=0}^{\infty} c_n.
$$

이것은 Abel-type continuity result이다.

### ▪ Theorem 8.3

double sequence $a_{ij}$와 row sums $b_i$가 주어지고 $\sum b_i$가 수렴하면,
$$
\sum_i\sum_j a_{ij}=\sum_j\sum_i a_{ij}
$$
를 얻는 theorem이다. power series coefficient manipulation의 기초 정당화 역할을 한다.

### ▪ Theorem 8.4

power series는 수렴구간 내부의 임의의 점 $a$를 중심으로 다시 power series로 전개된다:
$$
f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n
\qquad (|x-a|<R-|a|).
$$

즉 Taylor series가 실제로 원래 함수와 일치한다.

### ▪ Theorem 8.5

두 power series가 어떤 limit point를 가진 집합에서 일치하면, 계수들이 모두 같고 따라서 전체 수렴구간에서 일치한다. 즉 power series expansion은 유일하다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 결정적 메시지는 다음이다.

> 일반 함수는 Taylor series가 원함수와 같지 않을 수 있지만, power series로 정의된 함수는 수렴구간 안에서 진짜로 자기 Taylor series와 같다.

그래서 analytic function은 smooth function보다 훨씬 강한 개념이다. 계수 하나하나가 함수의 미분 정보와 완전히 연결되어 있다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 항별 미분이 정당한지 보일 때
- 계수를 도함수로 복원할 때
- 함수 전개가 유일한지 보일 때
- Chapter 8 이후 특수함수의 성질을 도출할 때

### 📌 문제 풀이 패턴
1. 수렴반경 내부의 작은 닫힌구간에서 M-test
2. term-by-term differentiation/integration
3. coefficient = derivative formula 활용

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 1의 $e^{-1/x^2}$는 “모든 도함수가 0이지만 함수는 0이 아님”이라는 analytic/non-analytic 차이를 보여주는 핵심 예와 연결된다.
- Exercise 2–5의 극한/이중합 문제도 이 절의 정당화 장치들을 자주 쓴다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorems 8.1–8.5 포함
- [x] 고계도함수 및 coefficient 관계 포함
- [x] 유일성 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 power series는 수렴반경 내부에서 항별 미분할 수 있는가?
- $f^{(k)}(0)=k!c_k$가 왜 중요한가?
- power series expansion의 유일성은 무엇을 뜻하는가?
