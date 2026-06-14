# 📘 Chapter 3 — Cauchy Sequences 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절의 중심 질문은 다음이다.

> 극한점을 미리 모르더라도, 수열이 수렴하는지 판정할 수 있는가?

이를 위해 **Cauchy sequence**를 정의한다. 이 개념은 “뒤쪽 항들끼리 서로 가까워진다”는 조건만으로 수렴을 판정하려는 시도다.

이 절의 흐름은 다음과 같다.

- Cauchy sequence를 정의한다.
- diameter를 도입해 tail의 크기를 기하적으로 측정한다.
- compact case에서 nested compact sets와 diameter shrinking을 이용해 Cauchy sequence의 수렴을 증명한다.
- $\mathbb R^k$에서는 모든 Cauchy sequence가 수렴한다는 **Cauchy criterion**을 얻는다.
- 마지막으로 **complete metric space**를 정의한다.

이 절은 해석학 전체의 기초다. “실수의 완비성”이 sequence 언어로 어떻게 나타나는지 보여 주기 때문이다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 3.8 — Cauchy sequence

metric space $X$의 sequence $\{p_n\}$가 다음을 만족하면 **Cauchy sequence**라고 한다.

모든 $\varepsilon>0$에 대해, 어떤 정수 $N$이 존재하여
$$
n\ge N,\ m\ge N
\implies
d(p_n,p_m)<\varepsilon.
$$

즉 충분히 뒤쪽 항들끼리는 서로 임의로 가깝다.

### ▪ Definition 3.9 — Diameter

$E$를 metric space $X$의 nonempty subset이라 하자. $p,q\in E$인 모든 거리
$$
d(p,q)
$$
의 집합의 supremum을 $E$의 **diameter**라고 한다.

만약 $E_N=\{p_N,p_{N+1},p_{N+2},\dots\}$라면,
$$
\{p_n\}\ \text{is Cauchy}
\iff
\lim_{N\to\infty}\operatorname{diam}E_N=0.
$$

### ▪ Theorem 3.10

1. $\overline E$가 metric space $X$에서 $E$의 closure이면
   $$
   \operatorname{diam}(\overline E)=\operatorname{diam}(E).
   $$
2. $K_n$이 compact set의 sequence이고
   $$
   K_n\supset K_{n+1},
   \qquad
   \lim_{n\to\infty}\operatorname{diam}K_n=0,
   $$
   이면
   $$
   \bigcap_{n=1}^{\infty}K_n
   $$
   은 정확히 한 점으로 이루어진다.

### ▪ Proof

**(1)** 먼저 $E\subset\overline E$이므로
$$
\operatorname{diam}E\le \operatorname{diam}\overline E.
$$

반대로 임의의 $\varepsilon>0$를 잡고 $p,q\in\overline E$를 택하자. closure의 정의에 의해 $E$ 안에서
$$
d(p,p')<\varepsilon,
\qquad
d(q,q')<\varepsilon
$$
인 $p',q'$를 찾을 수 있다. 그러면 triangle inequality로
$$
d(p,q)
\le d(p,p')+d(p',q')+d(q',q)
<2\varepsilon+d(p',q')
\le 2\varepsilon+\operatorname{diam}E.
$$
따라서
$$
\operatorname{diam}\overline E\le 2\varepsilon+\operatorname{diam}E.
$$
$\varepsilon$가 arbitrary이므로
$$
\operatorname{diam}\overline E\le \operatorname{diam}E.
$$
결국 equality가 성립한다.

**(2)**
$$
K=\bigcap_{n=1}^{\infty}K_n
$$
로 두자. nested compact sets의 교집합은 비어 있지 않다. 만약 $K$가 둘 이상의 점을 가진다면
$$
\operatorname{diam}K>0.
$$
그런데 $K\subset K_n$이므로 모든 $n$에 대해
$$
\operatorname{diam}K_n\ge \operatorname{diam}K>0.
$$
이것은 $\operatorname{diam}K_n\to0$와 모순이다. 따라서 $K$는 정확히 한 점만 가진다.

### ▪ Theorem 3.11

1. 임의의 metric space에서, convergent sequence는 Cauchy sequence이다.
2. $X$가 compact metric space이고 $\{p_n\}$이 $X$의 Cauchy sequence이면, $\{p_n\}$은 $X$의 어떤 점으로 수렴한다.
3. $\mathbb R^k$에서 모든 Cauchy sequence는 수렴한다.

### ▪ Proof

**(1)** $p_n\to p$라 하자. 임의의 $\varepsilon>0$에 대해 충분히 큰 $n,m$이면
$$
d(p_n,p)<\varepsilon,
\qquad
d(p_m,p)<\varepsilon.
$$
따라서
$$
d(p_n,p_m)\le d(p_n,p)+d(p,p_m)<2\varepsilon.
$$
즉 Cauchy이다.

**(2)** $E_N=\{p_N,p_{N+1},\dots\}$라 하자. Cauchy 성질과 Definition 3.9에 의해
$$
\operatorname{diam}E_N\to0.
$$
그리고 Theorem 3.10(a)에 의해
$$
\operatorname{diam}(\overline E_N)\to0.
$$
각 $\overline E_N$은 compact이고,
$$
\overline E_N\supset \overline E_{N+1}.
$$
따라서 Theorem 3.10(b)에 의해 모든 $\overline E_N$에 공통으로 들어가는 유일한 점 $p\in X$가 존재한다.

이제 임의의 $\varepsilon>0$에 대해 충분히 큰 $N$이면
$$
\operatorname{diam}(\overline E_N)<\varepsilon.
$$
그런데 $p\in\overline E_N$이고 $p_n\in E_N\subset\overline E_N$ for $n\ge N$ 이므로
$$
d(p_n,p)<\varepsilon
\qquad(n\ge N).
$$
따라서 $p_n\to p$.

**(3)** $\{\mathbf x_n\}$을 $\mathbb R^k$의 Cauchy sequence라 하자. 어떤 $N$ 이후 tail의 diameter가 1보다 작다. 따라서 tail은 bounded이고, 앞의 유한 개 항과 합치면 전체 수열이 bounded이다. $\mathbb R^k$의 bounded subset은 compact closure를 가지므로, (2)를 적용하면 $\{\mathbf x_n\}$은 수렴한다.

### ▪ Definition 3.12 — Complete metric space

모든 Cauchy sequence가 수렴하는 metric space를 **complete**하다고 한다.

### ▪ Remark

- 모든 compact metric space는 complete이다.
- 모든 Euclidean space $\mathbb R^k$도 complete이다.
- complete space의 closed subset 역시 complete이다.
- 유리수 전체 $\mathbb Q$는 usual metric 아래 complete하지 않다.

---

## 🟢 3. 개념 해설 + 엄밀성

### Cauchy가 왜 좋은가

수렴의 정의는 limit $p$를 미리 알아야 한다. 하지만 실제 문제에서는 limit를 모르는 경우가 많다. Cauchy 정의는 그런 점을 피한다.

즉
$$
\text{convergence: “어떤 }p\text{에 가까워진다”}
$$
를
$$
\text{Cauchy: “서로서로 가까워진다”}
$$
로 바꾼 것이다.

### complete의 의미

complete하다는 것은 “서로 가까워질 가능성이 있는 수열은 실제로 공간 안에서 limit를 가진다”는 뜻이다. 그래서 완비성은 **구멍이 없는 공간**이라는 직관과 연결된다.

예를 들어 $\sqrt2$로 가는 유리수 수열은 $\mathbb Q$ 안에서는 Cauchy이지만, limit가 $\mathbb Q$ 안에 없으므로 $\mathbb Q$는 complete하지 않다.

### diameter를 왜 쓰는가

tail 전체가 얼마나 퍼져 있는지 한 숫자로 측정하려면 diameter가 편하다. Cauchy의 정의를 tail diameter가 0으로 가는 조건으로 다시 쓰면, nested compact set argument와 바로 연결된다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- limit를 직접 guess하기 어려울 때
- 수열의 수렴을 “tail끼리 가까움”으로 판정하고 싶을 때
- complete / incomplete 여부를 보일 때
- fixed-point iteration, function space, improper integral convergence 등 후반부 도구의 기반으로 쓸 때

### 📌 문제 풀이 패턴

1. **수렴 ⇒ Cauchy**  
   triangle inequality 한 번이면 끝난다.

2. **Cauchy + convergent subsequence ⇒ full convergence**  
   Chapter 3 Exercise 20의 표준 패턴이다.

3. **tail diameter shrinking 패턴**  
   nested sets와 complete/compactness를 연결할 때 쓴다.

4. **complete하지 않음 보이기**  
   Cauchy지만 공간 안에서 수렴하지 않는 수열을 하나 제시한다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### Exercise 20과 직접 연결

문제:
어떤 Cauchy sequence가 수렴하는 subsequence를 가지면 전체가 같은 점으로 수렴함을 보여라.

전략:
- Cauchy 성질로 전체 꼬리를 subsequence의 한 뒤쪽 항과 가깝게 만든다.
- subsequence convergence로 그 한 항을 limit와 가깝게 만든다.
- triangle inequality로 전체 항도 limit와 가깝게 만든다.

### Exercise 21과 직접 연결

nested closed bounded sets in a complete space에서 diameter가 0으로 가면 교집합이 한 점이라는 문제는 바로 이 절의 핵심 논리를 연습시키는 문제다.

### 이 절을 배우고 나면 익혀야 할 감각

- 실수/유클리드 공간에서는 Cauchy 판정이 매우 강력하다.
- 하지만 일반 metric space에서는 Cauchy라고 해서 자동 수렴하지 않는다. complete가 필요하다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 3.8 포함
- [x] Definition 3.9 포함
- [x] Theorem 3.10 포함
- [x] Theorem 3.11 포함
- [x] Definition 3.12 포함
- [x] 완비성 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

### 개념 확인 질문

1. Cauchy sequence와 convergent sequence의 차이는 무엇인가?
2. 왜 complete space에서는 Cauchy가 곧 convergence가 되는가?
3. $\mathbb Q$가 complete하지 않다는 말은 구체적으로 무슨 뜻인가?

### 간단한 훈련 문제

1. convergent sequence가 반드시 Cauchy임을 직접 증명하라.
2. $1,1.4,1.41,1.414,\dots$가 $\mathbb Q$ 안에서 Cauchy임을 설명하라.
3. complete metric space의 closed subset이 complete임을 보여라.
