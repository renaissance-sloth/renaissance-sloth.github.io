# 📘 Chapter 3 — Some Special Sequences 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 자주 등장하는 기본 수열들의 극한을 한꺼번에 정리하는 절이다.

- $1/n^p\to0$
- $\sqrt[n]{p}\to1$
- $\sqrt[n]{n}\to1$
- 지수함수가 다항식보다 빠르게 커진다는 사실
- $|x|<1$이면 $x^n\to0$

이 절의 결과들은 뒤에서 series 판정, power series, exponential function을 다룰 때 계속 재사용된다. 특히 “지수 vs 다항식”의 성장 비교는 해석학 전체에서 매우 자주 나온다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 3.20

1. $p>0$이면
   $$
   \lim_{n\to\infty}\frac1{n^p}=0.
   $$
2. $p>0$이면
   $$
   \lim_{n\to\infty}\sqrt[n]{p}=1.
   $$
3. 
   $$
   \lim_{n\to\infty}\sqrt[n]{n}=1.
   $$
4. $p>0$, $\alpha\in\mathbb R$이면
   $$
   \lim_{n\to\infty}\frac{n^\alpha}{(1+p)^n}=0.
   $$
5. $|x|<1$이면
   $$
   \lim_{n\to\infty}x^n=0.
   $$

### ▪ Proof

**(1)** 주어진 $\varepsilon>0$에 대해
$$
n>(1/\varepsilon)^{1/p}
$$
이면
$$
\frac1{n^p}<\varepsilon.
$$
따라서 $1/n^p\to0$.

**(2)** 먼저 $p>1$인 경우를 보자. 다음과 같이 두자.
$$
x_n=\sqrt[n]{p}-1.
$$
그러면 $x_n>0$이고,
$$
(1+x_n)^n=p.
$$
이항정리에 의해
$$
1+nx_n\le (1+x_n)^n=p,
$$
따라서
$$
0<x_n\le \frac{p-1}{n}.
$$
우변이 0으로 가므로 $x_n\to0$, 즉
$$
\sqrt[n]{p}\to1.
$$
$p=1$이면 자명하고, $0<p<1$이면 역수를 취해 역시 결론이 성립한다.

**(3)**
$$
x_n=\sqrt[n]{n}-1
$$
로 두자. 그러면 $x_n\ge0$, 그리고
$$
n=(1+x_n)^n.
$$
이항정리로
$$
(1+x_n)^n\ge \frac{n(n-1)}2x_n^2.
$$
따라서
$$
n\ge \frac{n(n-1)}2x_n^2,
$$
즉
$$
0\le x_n\le \sqrt{\frac{2}{n-1}}\qquad(n\ge2).
$$
우변이 0으로 가므로 $x_n\to0$, 따라서
$$
\sqrt[n]{n}\to1.
$$

**(4)** $k>\alpha$, $k>0$인 정수 $k$를 하나 택하자. $n>2k$이면 이항정리에 의해
$$
(1+p)^n>\binom{n}{k}p^k
=\frac{n(n-1)\cdots(n-k+1)}{k!}p^k
>\frac{n^kp^k}{2^kk!}.
$$
따라서
$$
0<\frac{n^\alpha}{(1+p)^n}
<\frac{2^kk!}{p^k}n^{\alpha-k}.
$$
그런데 $\alpha-k<0$이므로 (1)에 의해 $n^{\alpha-k}\to0$. 따라서 원하는 극한은 0이다.

**(5)** (4)에서 $\alpha=0$으로 두면
$$
\frac1{(1+p)^n}\to0.
$$
이제 $|x|<1$이면 $|x|=1/(1+p)$ 꼴로 쓸 수 있으므로
$$
|x|^n\to0,
$$
따라서
$$
x^n\to0.
$$

---

## 🟢 3. 개념 해설 + 엄밀성

### 왜 이 절이 중요한가

이 절의 결과들은 하나하나가 사소해 보이지만, 사실 뒤의 chapter들에서 계속 재등장한다.

- $1/n^p\to0$: p-series, comparison test의 기본 재료
- $\sqrt[n]{p}\to1$, $\sqrt[n]{n}\to1$: root test와 연결
- $n^\alpha/(1+p)^n\to0$: 지수성장이 다항성장을 압도
- $x^n\to0$ for $|x|<1$: geometric series의 토대

### “지수가 다항식을 이긴다”는 말의 정확한 의미

Theorem 3.20(d)는 바로 그 말을 수식으로 쓴 것이다:
$$
\frac{n^\alpha}{(1+p)^n}\to0.
$$
즉 분자에 아무 고정된 거듭제곱을 올려도, 분모의 지수성장을 못 이긴다.

### 이항정리가 왜 반복해서 쓰이는가

$\sqrt[n]{p}\to1$, $\sqrt[n]{n}\to1$를 보일 때 핵심은
$$
(1+x_n)^n
$$
을 아래에서 간단한 항들로 estimate하는 것이다. 이항정리는 바로 그런 estimate를 제공한다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- series의 일반항이 0으로 가는 속도를 비교할 때
- root test 계산에서 $n$제곱근의 극한을 다룰 때
- geometric decay가 나타날 때
- exponential / polynomial / logarithmic growth를 비교할 때

### 📌 문제 풀이 패턴

1. **upper bound squeeze 패턴**  
   $0\le x_n\le s_n$, $s_n\to0$이면 $x_n\to0$.

2. **이항정리 estimate 패턴**  
   $(1+x_n)^n$을 전개해 필요한 항만 남기고 bounding한다.

3. **비교 패턴**  
   복잡한 수열을 $1/n^p$, geometric sequence 같은 익숙한 것과 비교한다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### 이후 장과의 연결

- geometric series는 바로 다음 series 절에서 본격적으로 쓰인다.
- $\sqrt[n]{n}\to1$은 root test 해석의 직감에 중요하다.
- $x^n\to0$ for $|x|<1$은 power series의 convergence interval 이해에 필수다.

### 과제와의 간접 연결

Chapter 3의 Exercise 5나 이후 root test 관련 문제를 풀 때, 결국 이런 기본 극한을 자유롭게 써야 한다. 즉 이 절은 “도구함” 역할을 한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 3.20(a) 포함
- [x] Theorem 3.20(b) 포함
- [x] Theorem 3.20(c) 포함
- [x] Theorem 3.20(d) 포함
- [x] Theorem 3.20(e) 포함
- [x] 쉬운 성장 비교 설명 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

### 개념 확인 질문

1. 왜 $\sqrt[n]{p}\to1$에서 $x_n=\sqrt[n]{p}-1$를 두는가?
2. 왜 지수함수는 다항식보다 빠르게 커지는가?
3. $|x|<1$일 때 $x^n\to0$가 geometric series와 어떤 관계가 있는가?

### 간단한 훈련 문제

1. $\lim_{n\to\infty}1/n^3$을 정의로 다시 증명하라.
2. $\lim_{n\to\infty}\sqrt[n]{5}=1$을 Theorem 3.20(b)의 논리로 직접 써 보라.
3. $\lim_{n\to\infty} n^4/2^n=0$을 Theorem 3.20(d)로 설명하라.
