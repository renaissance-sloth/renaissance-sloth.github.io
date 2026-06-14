# 📘 Chapter 3 — Convergent Sequences 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절의 흐름은 다음과 같다.

- 먼저 **metric space에서 수열이 수렴한다는 정의**를 세운다.
- 그 다음, 수렴의 가장 기본 성질인 **근방 판정, 극한의 유일성, boundedness**를 증명한다.
- 이어서 complex sequence와 vector-valued sequence에 대해, 수렴이 **합·곱·스칼라배·좌표별 수렴**과 어떻게 연결되는지 정리한다.

이 절을 제대로 이해하면 이후 장들에서 계속 쓰이는 다음 감각이 생긴다.

1. “수렴”은 결국 **거리**가 0으로 가는 것이다.  
2. 극한 계산은 complex number와 Euclidean vector에서는 **대수적으로 밀고 갈 수 있다.**  
3. 나중의 함수의 극한, 연속성, 급수, power series의 대부분은 이 절의 논리를 재활용한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 3.1 — Convergent sequence

metric space $X$의 sequence $\{p_n\}$가 어떤 점 $p\in X$에 대해 다음 성질을 가지면 $\{p_n\}$는 **converge**한다고 한다.

모든 $\varepsilon>0$에 대해, $n\ge N$이면
$$
d(p_n,p)<\varepsilon
$$
가 되게 하는 정수 $N$이 존재한다.

이 경우
$$
p_n\to p,
\qquad \lim_{n\to\infty}p_n=p
$$
라고 쓴다.

수렴하지 않으면 diverge한다고 한다.

### ▪ Remark / Example

- 이 정의는 수열뿐 아니라 **어느 공간에서 보느냐**에도 의존한다.
- 예를 들어 $\{1/n\}$은 $\mathbb R^1$에서는 0으로 수렴하지만, 양의 유리수만 모은 공간에서는 그 limit이 공간 안에 없으므로 수렴하지 않는다.
- sequence의 **range**는 항들의 집합이다.
- range가 bounded이면 sequence도 bounded라고 한다.

예시:
- $s_n=1/n$: 수렴, bounded, range는 무한.
- $s_n=n^2$: diverge, unbounded.
- $s_n=1+(-1)^n/n$: 1로 수렴.
- $s_n=i^n$: bounded지만 diverge.
- $s_n=1$: 상수수열이므로 1로 수렴.

### ▪ Theorem 3.2

$\{p_n\}$을 metric space $X$의 sequence라고 하자.

1. $\{p_n\}$이 $p\in X$로 수렴할 필요충분조건은, $p$의 모든 neighborhood가 유한 개의 항을 제외한 모든 $p_n$을 포함하는 것이다.
2. 만약 $\{p_n\}$이 $p$와 $p'$ 둘 다로 수렴하면 $p=p'$이다.
3. 수렴하는 sequence는 bounded이다.
4. $E\subset X$이고 $p$가 $E$의 limit point이면, $E$ 안의 어떤 sequence $\{p_n\}$가 존재하여 $p_n\to p$가 된다.

### ▪ Proof

**(1)** 먼저 $p_n\to p$라고 하자. $V$를 $p$의 neighborhood라고 하자. 어떤 $\varepsilon>0$가 있어서
$$
d(q,p)<\varepsilon \implies q\in V
$$
가 된다. 수렴의 정의에 의해 $n\ge N$이면 $d(p_n,p)<\varepsilon$가 되는 $N$이 있으므로, 결국 $n\ge N$이면 $p_n\in V$이다.

이제 역을 보자. $p$의 모든 neighborhood가 유한 개를 제외한 모든 $p_n$을 포함한다고 하자. 임의의 $\varepsilon>0$에 대해
$$
V=\{q\in X:d(q,p)<\varepsilon\}
$$
를 잡으면, 가정에 의해 어떤 $N$ 이후로는 $p_n\in V$이다. 즉 $n\ge N$이면 $d(p_n,p)<\varepsilon$. 따라서 $p_n\to p$.

**(2)** $\varepsilon>0$를 택하자. 수렴 가정에 의해
$$
n\ge N \implies d(p_n,p)<\varepsilon/2,
\qquad
n\ge N' \implies d(p_n,p')<\varepsilon/2
$$
가 되는 $N,N'$가 있다. 그러면 $n\ge \max(N,N')$일 때
$$
d(p,p')\le d(p,p_n)+d(p_n,p')<\varepsilon.
$$
$\varepsilon$가 임의이므로 $d(p,p')=0$, 따라서 $p=p'$.

**(3)** $p_n\to p$라 하자. 어떤 $N$ 이후에는 $d(p_n,p)<1$이다. 이제
$$
r=\max\{1,d(p_1,p),\dots,d(p_N,p)\}
$$
로 두면 모든 $n$에 대해 $d(p_n,p)\le r$. 따라서 bounded.

**(4)** $p$가 $E$의 limit point이면, 각 양의 정수 $n$에 대해
$$
d(p_n,p)<1/n
$$
을 만족하는 $p_n\in E$를 고를 수 있다. 그러면 $\varepsilon>0$에 대해 $1/N<\varepsilon$가 되는 $N$ 이후에는
$$
d(p_n,p)<1/n<\varepsilon.
$$
따라서 $p_n\to p$.

### ▪ Theorem 3.3

$\{s_n\},\{t_n\}$이 complex sequence이고
$$
s_n\to s,
\qquad
t_n\to t
$$
라 하자. 그러면

1. $s_n+t_n\to s+t$
2. 임의의 상수 $c$에 대해 $cs_n\to cs$, 또 $c+s_n\to c+s$
3. $s_nt_n\to st$
4. 모든 $n$에 대해 $s_n\ne0$이고 $s\ne0$이면
$$
\frac1{s_n}\to \frac1s
$$

### ▪ Proof

**(1)** $\varepsilon>0$에 대해 충분히 큰 $n$이면
$$
|s_n-s|<\varepsilon/2,
\qquad
|t_n-t|<\varepsilon/2.
$$
그러면
$$
|(s_n+t_n)-(s+t)|
\le |s_n-s|+|t_n-t|<\varepsilon.
$$

**(2)** 스칼라배와 상수 더하기는 위 부등식과 절댓값 성질로 바로 따라온다.

**(3)** 항등식
$$
s_nt_n-st=(s_n-s)(t_n-t)+s(t_n-t)+t(s_n-s)
$$
를 쓴다. 첫 항은 두 작은 양의 곱이라 0으로 가고, 나머지 둘도 각각 0으로 간다. 따라서 전체가 0으로 간다.

**(4)** 먼저 충분히 큰 $n$에 대해 $|s_n-s|<|s|/2$가 되게 하면
$$
|s_n|>|s|/2
$$
이다. 이제
$$
\left|\frac1{s_n}-\frac1s\right|
=\left|\frac{s-s_n}{ss_n}\right|
\le \frac{2}{|s|^2}|s_n-s|.
$$
우변이 0으로 가므로 결론이 따른다.

### ▪ Theorem 3.4

$\mathbf x_n\in\mathbb R^k$이고
$$
\mathbf x_n=(\alpha_{1,n},\dots,\alpha_{k,n})
$$
라 하자.

1. $\mathbf x_n\to \mathbf x=(\alpha_1,\dots,\alpha_k)$일 필요충분조건은 모든 $j$에 대해
$$
\alpha_{j,n}\to \alpha_j
$$
가 성립하는 것이다.
2. 만약 $\mathbf x_n\to\mathbf x$, $\mathbf y_n\to\mathbf y$, $\beta_n\to\beta$이면
$$
\mathbf x_n+\mathbf y_n\to \mathbf x+\mathbf y,
\quad
\mathbf x_n\cdot \mathbf y_n\to \mathbf x\cdot\mathbf y,
\quad
\beta_n\mathbf x_n\to \beta\mathbf x.
$$

### ▪ Proof

**(1)** 만약 $\mathbf x_n\to\mathbf x$이면
$$
|\alpha_{j,n}-\alpha_j|\le |\mathbf x_n-\mathbf x|
$$
이므로 각 좌표가 수렴한다.

반대로 각 좌표가 수렴한다고 하자. 임의의 $\varepsilon>0$에 대해 충분히 큰 $n$이면 각 $j$에 대해
$$
|\alpha_{j,n}-\alpha_j|<\varepsilon/\sqrt{k}.
$$
그러면
$$
|\mathbf x_n-\mathbf x|
=\left(\sum_{j=1}^k |\alpha_{j,n}-\alpha_j|^2\right)^{1/2}
<\varepsilon.
$$
따라서 $\mathbf x_n\to\mathbf x$.

**(2)** 좌표별 수렴을 (1)로 바꾼 뒤, 각 좌표마다 Theorem 3.3을 적용하면 된다.

---

## 🟢 3. 개념 해설 + 엄밀성

### 왜 $\varepsilon$-정의가 핵심인가

수렴은 “언젠가부터 limit에 아주 가깝다”는 뜻이다. 여기서 “아주”를 수치화한 것이 $\varepsilon$이고, “언젠가부터”를 수치화한 것이 $N$이다.

즉
$$
\forall \varepsilon>0\ \exists N\ \forall n\ge N:
d(p_n,p)<\varepsilon
$$

이 양화사 구조를 정확히 읽는 것이 제일 중요하다.

### 극한이 왜 유일한가

metric space에서 서로 다른 두 점은 양의 거리를 가진다. 그런데 한 sequence가 둘 다로 수렴한다면, 충분히 뒤쪽 항들은 두 점에 동시에 매우 가까워야 하므로, triangle inequality에 의해 두 점 사이 거리도 0이 되어야 한다. 그래서 결국 같은 점일 수밖에 없다.

### 좌표별 수렴이 왜 중요한가

$\mathbb R^k$에서는 벡터 전체의 수렴을 직접 다루기보다, 각 좌표의 수렴으로 바꾸면 계산이 쉬워진다. 이후 연속성, 미분, 적분에서도 같은 철학이 반복된다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- sequence의 수렴 여부를 정의로 직접 증명할 때
- limit가 유일함을 써서 역설을 만들 때
- complex sequence의 합, 곱, 역수 limit를 계산할 때
- vector sequence를 좌표별 문제로 분해할 때

### 📌 문제 풀이 패턴

1. **정의 직공법**  
   $\varepsilon>0$를 잡고, 원하는 부등식이 나오도록 $N$을 만든다.

2. **sandwich / triangle inequality 패턴**  
   합의 극한, 유일성, boundedness 증명에서 반복된다.

3. **좌표 분해 패턴**  
   $\mathbb R^k$ 문제를 각 coordinate limit로 바꾼다.

4. **대수 연산 패턴**  
   complex sequence에서는 먼저 차이를 전개하고, 각 항이 0으로 가는지 확인한다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### Exercise 1과 연결

문제:
If $\{s_n\}$ converges, prove that $\{|s_n|\}$ converges. Is the converse true?

전략:
- triangle inequality의 변형
  $$
  ||s_n|-|s||\le |s_n-s|
  $$
  를 쓰면 바로 끝난다.
- 역은 $s_n=(-1)^n$로 반례를 준다.

### Exercise 3과 연결

문제:
$$
s_{n+1}=\sqrt{2+s_n}
$$
형 재귀수열의 수렴과 상계 증명.

전략:
- 먼저 $s_n<2$를 귀납으로 보인다.
- 그 다음 $s_{n+1}\ge s_n$를 보여 단조증가를 얻는다.
- bounded + monotone 이면 뒤 절의 Theorem 3.14를 써서 수렴한다.

이 문제는 현재 절과 다음 절·단조수열 절이 합쳐지는 대표 예시다.

### 이 절을 배우고 바로 풀 수 있어야 하는 기본 연습

- 상수수열의 수렴 증명
- $1/n\to0$의 정의형 증명
- 두 complex sequence의 합과 곱의 극한 계산
- $\mathbb R^2$에서 좌표별 수렴 판정

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 3.1 포함
- [x] Theorem 3.2 포함
- [x] Theorem 3.3 포함
- [x] Theorem 3.4 포함
- [x] 예시와 핵심 remark 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

### 개념 확인 질문

1. 수렴의 정의에서 $N$은 왜 $\varepsilon$에 의존하지만 $n$에는 의존하지 않는가?
2. 극한의 유일성 증명에서 왜 triangle inequality가 핵심인가?
3. $\mathbb R^k$에서 좌표별 수렴과 벡터 수렴이 동치인 이유는 무엇인가?

### 간단한 훈련 문제

1. $s_n=3+1/n$이 3으로 수렴함을 정의로 증명하라.
2. $s_n\to s$, $t_n\to t$일 때 $s_n-t_n\to s-t$를 직접 보여라.
3. $\mathbf x_n=(1/n,(-1)^n/n)$의 수렴 여부를 판정하라.
