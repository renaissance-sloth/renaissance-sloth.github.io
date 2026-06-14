# 📘 Chapter 4 — Limits of Functions 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 Chapter 4 전체의 출발점이다. Chapter 3에서 sequence의 limit를 배웠다면, 이제는 **function의 limit**를 다룬다.

- 먼저 metric space 사이의 function에 대해 limit를 정의한다.
- 그다음 이 정의가 sequence language와 정확히 같다는 사실을 증명한다.
- 이어서 함수의 합, 곱, 몫의 limit 법칙을 정리한다.

핵심 감각은 다음이다.

> sequence의 limit가 “항이 점에 가까워진다”였다면, function의 limit는 “입력이 점에 가까워질 때 출력이 어떤 값에 가까워진다”는 말이다.

그리고 이후의 continuity, differentiability, integration에서도 계속 같은 패턴이 재활용된다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 4.1 — Limit of a function

$X,Y$를 metric spaces라 하자. $E\subset X$이고, $f:E\to Y$, $p$는 $E$의 limit point라고 하자. 이때
$$
\lim_{x\to p}f(x)=q
$$
라고 쓰는 것은, 모든 $\varepsilon>0$에 대해 어떤 $\delta>0$가 존재하여
$$
d_Y(f(x),q)<\varepsilon
$$
가
$$
0<d_X(x,p)<\delta
$$
를 만족하는 모든 $x\in E$에 대해 성립하는 것을 의미한다.

### ▪ Remark

- 여기서 $p$는 $X$의 점이지만 반드시 $E$ 안에 있을 필요는 없다.
- 또 $p\in E$라고 해도 반드시 $f(p)=\lim_{x\to p}f(x)$일 필요는 없다.
- 함수값 자체와 함수의 limit는 다른 개념이다.

### ▪ Theorem 4.2 — Sequential characterization

Definition 4.1의 상황에서
$$
\lim_{x\to p}f(x)=q
$$
일 필요충분조건은, $E$ 안의 모든 sequence $\{p_n\}$에 대해
$$
p_n\ne p,
\qquad
p_n\to p
$$
이면
$$
f(p_n)\to q
$$
가 성립하는 것이다.

### ▪ Proof

먼저 function limit가 성립한다고 하자. $p_n\to p$인 sequence를 잡고 $\varepsilon>0$를 주자. 정의에 의해 어떤 $\delta>0$가 있어서
$$
0<d_X(x,p)<\delta
\implies
d_Y(f(x),q)<\varepsilon.
$$
그리고 $p_n\to p$이므로 충분히 큰 $n$에 대해
$$
0<d_X(p_n,p)<\delta.
$$
따라서 충분히 큰 $n$에 대해
$$
d_Y(f(p_n),q)<\varepsilon.
$$
즉 $f(p_n)\to q$.

역으로, sequential condition이 성립한다고 하자. 만약 function limit가 거짓이면, 어떤 $\varepsilon>0$가 존재하여 모든 $\delta>0$에 대해
$$
0<d_X(x,p)<\delta
\quad\text{but}\quad
d_Y(f(x),q)\ge \varepsilon
$$
인 $x\in E$를 찾을 수 있다. 이제 $\delta_n=1/n$으로 두면 각 $n$마다 그런 $x_n$를 골라
$$
x_n\to p,
\qquad
d_Y(f(x_n),q)\ge\varepsilon
$$
인 sequence를 만들 수 있다. 이는 sequential condition과 모순이다.

### ▪ Corollary

함수의 limit가 존재하면 그 limit는 유일하다.

이는 Theorem 4.2와 Chapter 3의 sequence limit 유일성으로부터 바로 나온다.

### ▪ Definition 4.3

$E$에 정의된 complex functions $f,g$에 대해, 합 $f+g$, 차 $f-g$, 곱 $fg$, 몫 $f/g$를 usual way로 정의한다. 몫은 물론 $g(x)\ne0$인 점에서만 정의한다.

또 $f,g$가 $E\to\mathbb R^k$이면
$$
(f+g)(x)=f(x)+g(x),
\qquad
(f\cdot g)(x)=f(x)\cdot g(x)
$$
로 정의한다.

### ▪ Theorem 4.4

$p$가 $E\subset X$의 limit point이고, $f,g$가 $E$에 정의된 complex functions이며
$$
\lim_{x\to p}f(x)=A,
\qquad
\lim_{x\to p}g(x)=B
$$
라 하자. 그러면

1. $\lim_{x\to p}(f+g)(x)=A+B$
2. $\lim_{x\to p}(fg)(x)=AB$
3. $B\ne0$이면
   $$
   \lim_{x\to p}\frac{f(x)}{g(x)}=\frac AB.
   $$

벡터값 함수에서는 내적에 대해
$$
\lim_{x\to p}(f\cdot g)(x)=A\cdot B
$$
가 성립한다.

### ▪ Proof

Theorem 4.2로 function limit를 sequence limit 문제로 바꾸면, Chapter 3의 Theorems 3.3, 3.4의 limit algebra에서 즉시 따라온다.

---

## 🟢 3. 개념 해설 + 엄밀성

### 왜 $0<d_X(x,p)<\delta$ 인가

점 $p$ 자신은 제외한다. 함수의 limit는 “근처에서의 거동”을 보는 것이지, 함수값 $f(p)$ 자체를 보는 것이 아니기 때문이다.

### sequence criterion이 왜 중요한가

실전에서는 $\varepsilon$-$\delta$를 직접 다루는 것보다 sequence로 바꾸는 것이 훨씬 편한 경우가 많다. 나중에 continuity, one-sided limits, discontinuities에서도 이 방식이 반복된다.

### limit algebra의 철학

함수의 합·곱·몫 정리는 사실 새로운 내용이 아니라, Chapter 3에서 이미 배운 sequence limit 법칙을 옮겨 온 것이다. 이게 Rudin 스타일의 장점이다: 새 개념을 정의하고 나면, 그 뒤의 정리는 가능한 한 이전 장으로 환원한다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- 함수 limit 존재/부재를 sequence로 판정할 때
- rational function, polynomial, vector function의 limit를 계산할 때
- continuity 정의를 limit equality로 바꿀 준비를 할 때

### 📌 문제 풀이 패턴

1. **direct $\varepsilon$-$\delta$ pattern**  
   가장 기본 정의를 직접 쓴다.

2. **sequence counterexample pattern**  
   limit가 없음을 보일 때 서로 다른 두 sequence를 $p$로 보내고 출력 극한이 다름을 보인다.

3. **algebra transfer pattern**  
   함수 limit를 sequence limit로 바꾼 뒤 Chapter 3 결과를 쓴다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### 대표 패턴 1: limit가 없음을 보이는 법

$x\to p$에서 limit가 없다고 보이고 싶으면, $p$로 가는 두 sequence $x_n,y_n$를 만들어
$$
f(x_n),\ f(y_n)
$$
의 limit가 다르다는 것을 보이면 된다.

### 대표 패턴 2: polynomial / rational function

Theorem 4.4를 반복적으로 쓰면 polynomial, rational expression의 limit는 거의 자동으로 계산된다.

### Chapter 4 exercise와 연결

- Exercise 18 같은 함수는 rational/irrational sequence를 따로 잡는 방식으로 discontinuity를 분석한다.
- Exercise 23, 24의 convexity 문제도 결국 연속성과 limit control을 바탕으로 한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 4.1 포함
- [x] Theorem 4.2 포함
- [x] Corollary (uniqueness) 포함
- [x] Definition 4.3 포함
- [x] Theorem 4.4 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 함수 limit 정의에서 왜 $x=p$를 제외하는가?
- sequence criterion으로 limit 부존재를 보이는 기본 아이디어는 무엇인가?
- $\lim_{x\to p}(f+g)=\lim f+\lim g$가 왜 sequence theorem으로 환원되는가?
