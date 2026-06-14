# 📘 Chapter 4 — Continuous Functions 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절에서는 “limit”를 “continuity”로 바꾼다.

- 먼저 pointwise continuity를 정의한다.
- limit point에서는
  $$
  f \text{ continuous at }p
  \iff
  \lim_{x\to p}f(x)=f(p)
  $$
  을 보인다.
- composition, open-set characterization, closed-set characterization을 증명한다.
- 마지막으로 complex / vector-valued continuity를 정리한다.

즉 이 절은 continuity의 거의 모든 기본 언어를 완성하는 절이다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 4.5 — Continuity at a point

$X,Y$를 metric spaces, $E\subset X$, $p\in E$, $f:E\to Y$라 하자. $f$가 $p$에서 continuous라는 것은, 모든 $\varepsilon>0$에 대해 어떤 $\delta>0$가 존재하여
$$
d_X(x,p)<\delta
\implies
d_Y(f(x),f(p))<\varepsilon
$$
가 모든 $x\in E$에 대해 성립하는 것이다.

모든 점에서 continuous이면 $E$에서 continuous라고 한다.

### ▪ Remark

- continuity는 반드시 $p\in E$에서만 말할 수 있다.
- isolated point에서는 모든 함수가 자동으로 continuous이다.

### ▪ Theorem 4.6

$p$가 $E$의 limit point라 하자. 그러면
$$
f \text{ is continuous at }p
\iff
\lim_{x\to p}f(x)=f(p).
$$

### ▪ Proof

Definition 4.1과 Definition 4.5를 그대로 비교하면 즉시 나온다. continuity는 “limit가 존재하고 그 값이 함수값과 같다”는 말이다.

### ▪ Theorem 4.7 — Composition of continuous functions

$f:E\to Y$, $g:f(E)\to Z$, $h=g\circ f$라 하자. $f$가 $p\in E$에서 continuous이고 $g$가 $f(p)$에서 continuous이면 $h$는 $p$에서 continuous이다.

### ▪ Proof

$\varepsilon>0$를 주자. $g$의 continuity로부터 $f(p)$ 근처에서 출력 오차 $<\varepsilon$를 보장하는 $\eta$를 잡는다. 다시 $f$의 continuity로부터 $p$ 근처에서 입력을 $\eta$-근처로 보내는 $\delta$를 잡는다. 그러면
$$
d_X(x,p)<\delta
\implies
d_Z(g(f(x)),g(f(p)))<\varepsilon.
$$

### ▪ Theorem 4.8 — Open set characterization

mapping $f:X\to Y$가 continuous일 필요충분조건은, $Y$의 every open set $V$에 대해
$$
f^{-1}(V)
$$
가 $X$에서 open인 것이다.

### ▪ Proof

**($\Rightarrow$)** $f$가 continuous라 하자. $V\subset Y$ open, $p\in f^{-1}(V)$라 하자. 그러면 $f(p)\in V$이고, $V$가 open이므로 $f(p)$ 주위 작은 ball이 $V$ 안에 들어간다. continuity로부터 그 ball의 inverse image 안에 들어가는 $p$ 주위 작은 ball이 생기므로 $p$는 interior point다. 따라서 $f^{-1}(V)$는 open.

**($\Leftarrow$)** 모든 open set의 inverse image가 open이라고 하자. 임의의 $p\in X$와 $\varepsilon>0$에 대해 $f(p)$ 중심 $\varepsilon$-ball을 $V$라 하자. $V$는 open이므로 $f^{-1}(V)$는 open이고 $p\in f^{-1}(V)$. 따라서 $p$ 주변 작은 ball이 $f^{-1}(V)$에 포함된다. 이것이 continuity 정의와 정확히 같다.

### ▪ Corollary

$f:X\to Y$가 continuous일 필요충분조건은, $Y$의 every closed set $C$에 대해
$$
f^{-1}(C)
$$
가 $X$에서 closed인 것이다.

### ▪ Theorem 4.9

$f,g$가 metric space $X$ 위의 complex continuous functions이면, $f+g$, $fg$, 그리고 $g(x)\ne0$일 때 $f/g$도 continuous이다.

### ▪ Proof

isolated point에서는 자명하고, limit point에서는 Theorems 4.4와 4.6을 사용하면 된다.

### ▪ Theorem 4.10

1. $f=(f_1,\dots,f_k):X\to\mathbb R^k$가 continuous일 필요충분조건은 각 component $f_j$가 continuous인 것이다.
2. $f,g:X\to\mathbb R^k$가 continuous이면 $f+g$와 $f\cdot g$도 continuous이다.

### ▪ Proof

component inequality
$$
|f_j(x)-f_j(y)|\le |f(x)-f(y)|
$$
를 쓰면 (1)이 나온다. (2)는 (1)과 Theorem 4.9로부터 나온다.

### ▪ Examples 4.11

- coordinate function $\phi_i(x)=x_i$는 continuous
- 모든 monomial과 polynomial은 continuous
- denominator가 0이 아닌 곳의 rational function도 continuous
- norm map $x\mapsto|x|$도 continuous

### ▪ Remark 4.12

continuity는 function의 정의역 밖 점들과 무관하다. 따라서 subset 위 정의된 continuous function을 따로 생각하기보다, 그냥 metric space 사이의 mapping으로 보는 편이 정리를 더 깔끔하게 만든다.

---

## 🟢 3. 개념 해설 + 엄밀성

### continuity는 “limit = value”다

이 절의 핵심 문장은 사실 Theorem 4.6 하나다. continuity는 전혀 새로운 개념처럼 보이지만, limit 개념을 함수값과 접붙인 것뿐이다.

### open set characterization이 왜 powerful한가

점마다 $\varepsilon$-$\delta$를 쓰는 대신, “open set의 inverse image가 open”이라는 전역적 표현으로 continuity를 다룰 수 있다. connectedness, compactness, inverse map의 연속성 증명에서 이 관점이 훨씬 강하다.

### vector-valued continuity의 핵심

벡터 함수도 결국 componentwise로 쪼개면 된다. 이건 뒤의 multivariable differentiation, integration에서 계속 반복된다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- continuity를 limit 계산으로 바꿀 때
- 합성함수의 continuity를 증명할 때
- open/closed set preimage로 위상적 성질을 전달할 때
- vector-valued function을 componentwise로 다룰 때

### 📌 문제 풀이 패턴

1. **limit equals value pattern**  
   limit를 계산하고 함수값과 일치하는지 본다.

2. **composition pattern**  
   안쪽 함수 연속 + 바깥 함수 연속 → 합성 연속.

3. **preimage pattern**  
   continuity를 open/closed set inverse image로 증명한다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### Exercise 3과 직접 연결

zero set $Z(f)$가 closed임을 보이는 문제는 Corollary의 즉각적인 응용이다. 왜냐하면
$$
Z(f)=f^{-1}(\{0\})
$$
이고 $\{0\}$는 closed set이기 때문이다.

### Exercise 5, 13과 간접 연결

continuous extension, uniformly continuous extension을 다루는 문제들은 결국 “연속함수를 어떻게 안전하게 이어 붙일 것인가”라는 이 절의 철학 위에 서 있다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 4.5 포함
- [x] Theorem 4.6 포함
- [x] Theorem 4.7 포함
- [x] Theorem 4.8 및 corollary 포함
- [x] Theorems 4.9, 4.10 포함
- [x] Examples/Remark 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- continuity를 limit language로 다시 말해 보라.
- open set characterization이 pointwise 정의보다 강력한 이유는 무엇인가?
- vector-valued continuity가 componentwise continuity와 동치인 이유를 설명하라.
