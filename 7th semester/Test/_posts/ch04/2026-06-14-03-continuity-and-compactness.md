# 📘 Chapter 4 — Continuity and Compactness 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 compactness와 continuity가 만나면 얼마나 강력한 결과가 나오는지를 보여 준다.

- continuous image of compact set is compact
- compact domain 위 continuous real function은 bounded이고 max/min을 가진다
- compact domain 위 continuous bijection의 inverse는 continuous다
- compact domain 위 continuous function은 uniformly continuous다
- compactness 가정이 빠지면 왜 깨지는지 반례도 본다

이 절은 해석학에서 compactness를 실제로 “쓰는” 첫 절이다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 4.13

$E\to\mathbb R^k$인 mapping $f$가
$$
|f(x)|\le M
\qquad (x\in E)
$$
를 만족하는 어떤 실수 $M$를 가지면 bounded라고 한다.

### ▪ Theorem 4.14

continuous mapping $f:X\to Y$와 compact metric space $X$가 주어지면, $f(X)$는 compact이다.

### ▪ Proof

$\{V_\alpha\}$를 $f(X)$의 open cover라 하자. continuity에 의해 각 inverse image $f^{-1}(V_\alpha)$는 open이고, 이들이 $X$를 덮는다. $X$가 compact이므로 유한 부분덮개를 고를 수 있고, 다시 $f$를 적용하면 $f(X)$도 유한 부분덮개를 가진다. 따라서 compact이다.

### ▪ Note

일반적으로 $f(f^{-1}(E))=E$도, $f^{-1}(f(E))=E$도 항상 equality가 되는 것은 아니다. 적절한 포함관계를 조심해야 한다.

### ▪ Theorem 4.15

$f$가 compact metric space $X$에서 $\mathbb R^k$로의 continuous mapping이면, $f(X)$는 closed이고 bounded이다. 따라서 $f$는 bounded이다.

### ▪ Proof

Theorem 4.14로 $f(X)$는 compact이고, $\mathbb R^k$에서는 compact set이 closed and bounded이므로 결론이 나온다.

### ▪ Theorem 4.16 — Extreme value theorem

compact metric space $X$ 위의 continuous real function $f$에 대해
$$
M=\sup_{p\in X}f(p),
\qquad
m=\inf_{p\in X}f(p)
$$
를 두면, 어떤 $p,q\in X$가 존재하여
$$
f(p)=M,
\qquad
f(q)=m.
$$

즉 continuous real function on compact set은 maximum과 minimum을 실제로 달성한다.

### ▪ Proof

Theorem 4.15에 의해 $f(X)\subset\mathbb R$는 closed and bounded이다. 따라서 $\sup f(X)$, $\inf f(X)$가 존재하고 closedness 때문에 실제로 $f(X)$ 안에 들어간다. 그래서 그 값을 찍는 $p,q$가 존재한다.

### ▪ Theorem 4.17

compact metric space $X$에서 metric space $Y$로의 continuous 1-1 mapping $f$가 있으면 inverse mapping
$$
f^{-1}:f(X)\to X
$$
는 continuous이다.

### ▪ Proof

Theorem 4.8을 $f^{-1}$에 적용한다. $X$의 open set $V$를 택하면, $V^c$는 closed이므로 compact이다. 따라서 $f(V^c)$는 compact, hence closed. 그런데 $f$가 1-1 onto on its image이므로 $f(V)$는 $f(V^c)$의 complement이고 따라서 open이다. 그러므로 $f^{-1}$는 continuous.

### ▪ Definition 4.18 — Uniform continuity

mapping $f:X\to Y$가 uniformly continuous라는 것은, 모든 $\varepsilon>0$에 대해 어떤 $\delta>0$가 존재하여
$$
d_X(p,q)<\delta
\implies
d_Y(f(p),f(q))<\varepsilon
$$
가 모든 $p,q\in X$에 대해 성립하는 것이다.

### ▪ Theorem 4.19

compact metric space $X$에서 metric space $Y$로의 continuous mapping $f$는 uniformly continuous이다.

### ▪ Proof

각 점 $p\in X$에 대해 continuity로부터 $\phi(p)>0$를 택해
$$
d_X(p,q)<\phi(p)
\implies
d_Y(f(p),f(q))<\varepsilon/2
$$
가 되게 한다. 이어서
$$
J(p)=\{q\in X:d_X(p,q)<\phi(p)/2\}
$$
를 잡으면 $\{J(p)\}$는 $X$의 open cover이다. compactness로 유한 부분덮개 $J(p_1),\dots,J(p_n)$를 잡고
$$
\delta=\frac12\min\{\phi(p_1),\dots,\phi(p_n)\}
$$
로 둔다. 이제 $d_X(p,q)<\delta$이면 어떤 $p_m$의 근방 안에서 둘 다 제어되어 triangle inequality로
$$
d_Y(f(p),f(q))<\varepsilon.
$$

### ▪ Theorem 4.20

$E\subset\mathbb R^1$가 noncompact이면

1. unbounded continuous function on $E$가 존재한다.
2. bounded but maximum을 갖지 않는 continuous function on $E$가 존재한다.
3. $E$가 bounded라면, uniformly continuous가 아닌 continuous function on $E$도 존재한다.

### ▪ Example 4.21

$[0,2\pi)$에서 원을 parameterize하는
$$
f(t)=(\cos t,\sin t)
$$
는 continuous 1-1 mapping이지만, inverse는 $(1,0)$에서 continuous가 아니다. 따라서 Theorem 4.17에서 compactness는 essential하다.

---

## 🟢 3. 개념 해설 + 엄밀성

compactness는 “finite subcover가 존재한다”는 추상 정의를 가지고 있지만, 실제 계산에서는 다음과 같은 결과들로 체감된다.

- boundedness 보장
- max/min 달성
- inverse continuity 보장
- uniform continuity 보장

즉 compactness는 local continuity를 global control로 바꿔 준다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- 함수값이 bounded인지 보장하고 싶을 때
- maximum/minimum 존재를 보일 때
- inverse map의 continuity를 확보할 때
- continuity를 uniform continuity로 승격하고 싶을 때

### 📌 문제 풀이 패턴

1. **continuous image of compact**  
   먼저 상(image)이 compact임을 보인다.

2. **compact in $\mathbb R^k$**  
   compact이면 closed and bounded를 바로 쓴다.

3. **finite subcover pattern**  
   uniform continuity proof의 핵심.

---

## 🔴 5. 대표 문제 & 풀이 전략

### Exercise 5와 연결

닫힌 집합 위의 continuous function을 extension할 때, continuity와 closedness, boundedness, compactness 주변 논리를 정확히 알고 있어야 한다.

### Exercise 11, 13과 연결

uniform continuity를 sequence/Cauchy 관점으로 다룰 때, Theorem 4.19가 매우 중요하다. compact 위에서는 continuity와 uniform continuity가 같아지므로 extension과 completion 문제에서 강력하게 작동한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 4.13 포함
- [x] Theorems 4.14–4.19 포함
- [x] Theorem 4.20 반례 설명 포함
- [x] Example 4.21 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 continuous image of compact is compact인가?
- compact set 위 continuous real function이 max/min을 갖는 이유를 설명하라.
- continuity와 uniform continuity의 차이는 무엇인가?
- 왜 compactness가 inverse continuity theorem에서 essential한가?
