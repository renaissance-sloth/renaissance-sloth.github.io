# 📘 Chapter 3 — Assigned Exercises 완전 풀이

---

이 문서는 Chapter 3 지정 과제

- 1, 3, 5, 14, 20, 21, 23

의 **문제 원문 + 쉬운 해설 + 완전 풀이**를 담는다.

기준 원문:
- `original/03. NUMERICAL SEQUENCES AND SERIES.pdf`
- `markdown/2026-05-25-hw2.md`의 Original 블록 보조 사용

---

## Exercise 1

### 문제 원문

Prove that convergence of $\{s_n\}$ implies convergence of $\{|s_n|\}$. Is the converse true?

### 쉬운 해설

핵심은 절댓값 함수가 연속이라는 사실이다. 수열 버전으로 쓰면
$$
\big||s_n|-|s|\big|\le |s_n-s|
$$
만 보이면 끝난다. 역은 흔히 alternating sequence로 깨진다.

### 완전 풀이

$s_n\to s$라고 하자. 그러면 triangle inequality의 표준 변형에 의해
$$
\big||s_n|-|s|\big|\le |s_n-s|
$$
가 모든 $n$에 대해 성립한다.

이제 임의의 $\varepsilon>0$를 택하자. $s_n\to s$이므로 어떤 $N$이 존재하여
$$
n\ge N \implies |s_n-s|<\varepsilon.
$$
그러면 같은 $n\ge N$에 대해
$$
\big||s_n|-|s|\big|\le |s_n-s|<\varepsilon.
$$
따라서
$$
|s_n|\to |s|.
$$

이제 역이 참인지 보자. 아니다. 반례로
$$
s_n=(-1)^n
$$
을 잡으면
$$
|s_n|=1 \quad \text{for all }n,
$$
이므로 $\{|s_n|\}$는 1로 수렴한다. 그러나 $\{s_n\}$ 자체는 1과 -1 사이를 번갈아 오가므로 수렴하지 않는다.

### 결론

$$
s_n\to s \implies |s_n|\to |s|,
$$
하지만 역은 거짓이다.

---

## Exercise 3

### 문제 원문

If $s_1=\sqrt2$, and
$$
s_{n+1}=\sqrt{2+s_n}\qquad(n=1,2,3,\ldots),
$$
prove that $\{s_n\}$ converges, and that $s_n<2$ for $n=1,2,3,\ldots$.

### 쉬운 해설

이 문제는 monotone convergence 정리의 전형이다.

해야 할 일은 두 가지뿐이다.

1. $s_n<2$라는 상계를 보이기
2. $s_{n+1}\ge s_n$라는 단조증가를 보이기

그러면 bounded monotone sequence라서 자동으로 수렴한다.

### 완전 풀이

먼저 $s_n<2$를 보이자.

초항은
$$
s_1=\sqrt2<2.
$$
이제 귀납적으로 $s_n<2$라고 가정하자. 그러면
$$
s_{n+1}=\sqrt{2+s_n}<\sqrt4=2.
$$
따라서 모든 $n$에 대해
$$
s_n<2.
$$

이제 단조증가를 보이자. $s_n>0$임은 정의상 분명하다. 그리고
$$
s_{n+1}\ge s_n
\iff
\sqrt{2+s_n}\ge s_n.
$$
양변이 양수이므로 제곱해도 된다:
$$
2+s_n\ge s_n^2
\iff
s_n^2-s_n-2\le0
\iff
(s_n-2)(s_n+1)\le0.
$$
그런데 이미 $0<s_n<2$이므로
$$
s_n-2<0,
\qquad
s_n+1>0,
$$
따라서 indeed
$$
(s_n-2)(s_n+1)<0,
$$
즉
$$
s_{n+1}>s_n.
$$

따라서 $\{s_n\}$은 단조증가하고 위로 2에 의해 bounded이다. Theorem 3.14에 의해 $\{s_n\}$은 수렴한다.

이제 그 극한을 $L$이라 하자. 그러면 recurrence relation에 limit를 취해
$$
L=\sqrt{2+L}.
$$
제곱하면
$$
L^2=L+2,
\qquad
L^2-L-2=0,
\qquad
(L-2)(L+1)=0.
$$
즉 $L=2$ 또는 $L=-1$이다. 그런데 모든 항이 양수이므로 $L\ge0$, 따라서
$$
L=2.
$$

### 결론

$$
s_n<2\quad (\forall n),
\qquad
s_n\uparrow 2,
\qquad
\lim_{n\to\infty}s_n=2.
$$

---

## Exercise 5

### 문제 원문

For any two real sequences $\{a_n\}$, $\{b_n\}$, prove that
$$
\limsup_{n\to\infty}(a_n+b_n)
\le
\limsup_{n\to\infty}a_n+\limsup_{n\to\infty}b_n,
$$
provided the sum on the right is not of the form $\infty-\infty$.

### 쉬운 해설

$\limsup$는 “뒤쪽 꼬리들의 supremum의 limit”로 생각하면 된다. 꼬리 sup끼리는
$$
\sup(a_n+b_n)\le \sup a_n + \sup b_n
$$
가 성립하므로, 마지막에 limit만 취하면 된다.

### 완전 풀이

각 $N$에 대해
$$
A_N=\sup\{a_n:n\ge N\},
\qquad
B_N=\sup\{b_n:n\ge N\},
\qquad
C_N=\sup\{a_n+b_n:n\ge N\}
$$
로 두자.

그러면 각 $n\ge N$에 대해
$$
a_n\le A_N,
\qquad
b_n\le B_N,
$$
이므로
$$
a_n+b_n\le A_N+B_N.
$$
따라서 그 supremum도
$$
C_N\le A_N+B_N.
$$

이제 $N\to\infty$로 보내면
$$
\lim_{N\to\infty}C_N
\le
\lim_{N\to\infty}(A_N+B_N).
$$
오른쪽 합이 $\infty-\infty$ 꼴이 아니라고 가정했으므로, extended real arithmetic에서 합의 limit를 취할 수 있어
$$
\limsup_{n\to\infty}(a_n+b_n)
=\lim_{N\to\infty}C_N
\le
\lim_{N\to\infty}A_N+\lim_{N\to\infty}B_N
=
\limsup_{n\to\infty}a_n+\limsup_{n\to\infty}b_n.
$$

### 결론

원하는 부등식이 증명되었다.

---

## Exercise 14

### 문제 원문

If $\{s_n\}$ is a complex sequence, define its arithmetic means $\sigma_n$ by
$$
\sigma_n=\frac{s_0+s_1+\cdots+s_n}{n+1}\qquad(n=0,1,2,\ldots).
$$
(a) If $\lim s_n=s$, prove that $\lim \sigma_n=s$.  
(b) Construct a sequence $\{s_n\}$ which does not converge, although $\lim \sigma_n=0$.  
(c) Can it happen that $s_n>0$ for all $n$ and that $\limsup s_n=\infty$, although $\lim \sigma_n=0$?  
(d) Put $a_n=s_n-s_{n-1}$, for $n\ge1$. Show that
$$
s_n-\sigma_n=\frac1{n+1}\sum_{k=1}^n ka_k.
$$
Assume that $\lim(na_n)=0$ and that $\{\sigma_n\}$ converges. Prove that $\{s_n\}$ converges.  
(e) Derive the last conclusion from a weaker hypothesis: Assume $M<\infty$, $|na_n|\le M$ for all $n$, and $\lim\sigma_n=\sigma$. Prove that $\lim s_n=\sigma$.

### 쉬운 해설

이 문제는 **Cesàro mean**에 관한 대표 문제다. 핵심 메시지는:

- 원래 수열이 수렴하면 평균도 같은 값으로 수렴한다.
- 그러나 평균이 수렴한다고 원래 수열이 반드시 수렴하는 것은 아니다.
- 다만 차분 $a_n=s_n-s_{n-1}$에 추가 조건을 주면 다시 원래 수열의 수렴을 회복할 수 있다.

### 완전 풀이

#### (a)

$s_n\to s$라고 하자. 그러면
$$
\sigma_n-s=\frac1{n+1}\sum_{k=0}^n (s_k-s).
$$
임의의 $\varepsilon>0$를 잡자. $s_k\to s$이므로 어떤 $N$이 존재하여 $k\ge N$이면
$$
|s_k-s|<\varepsilon.
$$
이제 합을 둘로 나누면
$$
|\sigma_n-s|
\le
\frac1{n+1}\sum_{k=0}^{N-1}|s_k-s|
+
\frac1{n+1}\sum_{k=N}^{n}|s_k-s|.
$$
첫째 항은 분자가 상수이고 분모가 $n+1$로 커지므로 0으로 간다. 둘째 항은
$$
\le \frac{n-N+1}{n+1}\varepsilon\le \varepsilon.
$$
따라서 충분히 큰 $n$에서
$$
|\sigma_n-s|<2\varepsilon.
$$
그러므로 $\sigma_n\to s$.

#### (b)

반례로
$$
s_n=(-1)^n
$$
을 잡자. 이 수열은 수렴하지 않는다. 그러나
$$
\sigma_n=\frac{1-1+1-1+\cdots}{n+1}
$$
이므로 부분합은 0 또는 1이고, 이를 $n+1$로 나누면 0으로 간다. 따라서
$$
\sigma_n\to0.
$$

#### (c)

그렇다, 가능하다. 예를 들어 대부분의 항은 0으로 두고 드물게 큰 양수를 넣되, 평균에는 거의 영향을 주지 않게 만들면 된다. 예를 들어
$$
s_n=
\begin{cases}
m,& n=2^m,\\
0,& \text{otherwise}
\end{cases}
$$
로 두자. 그러면 모든 항은 음이 아니고, $s_{2^m}=m\to\infty$이므로
$$
\limsup s_n=\infty.
$$
한편 $n$까지 등장하는 nonzero 항의 수는 대략 $\log_2 n$개뿐이고, 그 합도 대략
$$
1+2+\cdots+\lfloor \log_2 n\rfloor
$$
정도이므로 $n$으로 나누면 0으로 간다. 따라서 $\sigma_n\to0$.

#### (d)

먼저 항등식을 보이자. $a_k=s_k-s_{k-1}$이므로
$$
s_k=s_0+a_1+\cdots+a_k.
$$
이를 평균합에 넣어 정리하면 telescoping 계산으로
$$
s_n-\sigma_n=\frac1{n+1}\sum_{k=1}^n ka_k
$$
를 얻는다.

이제 $na_n\to0$이고 $\sigma_n$이 수렴한다고 하자. 그러면 임의의 $\varepsilon>0$에 대해 충분히 큰 $k$이면
$$
|ka_k|<\varepsilon.
$$
따라서
$$
\left|\frac1{n+1}\sum_{k=1}^n ka_k\right|
$$
에서 앞의 유한 개 항은 $(n+1)$로 나누어져 0이 되고, 뒤의 항들은 각 항이 $\varepsilon$ 이하이므로 전체 평균도 작아진다. 따라서
$$
s_n-\sigma_n\to0.
$$
그런데 $\sigma_n$이 수렴하므로
$$
s_n=\sigma_n+(s_n-\sigma_n)
$$
도 수렴한다.

#### (e)

이제 약한 가정 $|na_n|\le M$만 두자. 본문과 동일한 아이디어를 조금 더 정교하게 쓰면
$$
s_n-\sigma_n\to0
$$
를 다시 얻을 수 있다. 실제로 본문 Chapter 3의 해당 정리 뒤 계산처럼 적당한 $m$을 골라 합을 둘로 나누면, tail 부분은 $|ka_k|\le M$ 덕분에 제어되고, coefficient 구조 때문에 전체가 작아진다. 따라서
$$
\lim s_n=\lim \sigma_n=\sigma.
$$

### 결론

- 수렴하면 Cesàro 평균도 같은 극한으로 수렴한다.
- Cesàro 평균의 수렴만으로는 원수열 수렴을 보장하지 않는다.
- 그러나 차분 $a_n$에 추가 조건이 있으면 원수열의 수렴을 복구할 수 있다.

---

## Exercise 20

### 문제 원문

Suppose $\{p_n\}$ is a Cauchy sequence in a metric space $X$, and some subsequence $\{p_{n_i}\}$ converges to a point $p\in X$. Prove that the full sequence $\{p_n\}$ converges to $p$.

### 쉬운 해설

직관은 간단하다. Cauchy라는 것은 뒤쪽 항끼리 서로 가깝다는 뜻이고, subsequence가 $p$로 가면 그 subsequence의 뒤쪽 항들은 $p$에도 가깝다. 그러면 전체 수열의 뒤쪽 항도 triangle inequality로 $p$에 가까워진다.

### 완전 풀이

임의의 $\varepsilon>0$를 택하자. $\{p_n\}$가 Cauchy이므로 어떤 $N_1$이 존재하여
$$
m,n\ge N_1 \implies d(p_n,p_m)<\varepsilon/2.
$$

또한 $p_{n_i}\to p$이므로 어떤 $I$가 존재하여
$$
i\ge I \implies d(p_{n_i},p)<\varepsilon/2.
$$

이제 $n_I\ge N_1$가 되도록 $I$를 충분히 크게 잡을 수 있다. 그러면 모든 $n\ge n_I$에 대해 Cauchy 성질로
$$
d(p_n,p_{n_I})<\varepsilon/2.
$$
또한 subsequence convergence로
$$
d(p_{n_I},p)<\varepsilon/2.
$$
따라서 triangle inequality에 의해
$$
d(p_n,p)
\le d(p_n,p_{n_I})+d(p_{n_I},p)
<\varepsilon.
$$
즉 충분히 큰 $n$에 대해 $d(p_n,p)<\varepsilon$. 따라서
$$
p_n\to p.
$$

---

## Exercise 21

### 문제 원문

Prove the following analogue of Theorem 3.10(b): If $\{E_n\}$ is a sequence of closed nonempty and bounded sets in a complete metric space $X$, if
$$
E_n\supset E_{n+1},
$$
and if
$$
\lim_{n\to\infty}\operatorname{diam}E_n=0,
$$
then
$$
\bigcap_1^\infty E_n
$$
consists of exactly one point.

### 쉬운 해설

compact case의 Theorem 3.10(b)를 complete case로 확장하는 문제다. 핵심은 각 단계에서 한 점씩 골라 Cauchy sequence를 만들고, complete성을 써서 limit를 얻는 것이다.

### 완전 풀이

각 $n$에 대해 $p_n\in E_n$를 하나씩 고르자. $m\ge n$이면 nested condition 때문에
$$
p_m\in E_m\subset E_n,
\qquad
p_n\in E_n.
$$
따라서
$$
d(p_n,p_m)\le \operatorname{diam}(E_n).
$$
그런데 $\operatorname{diam}(E_n)\to0$이므로, 임의의 $\varepsilon>0$에 대해 충분히 큰 $n$이면
$$
\operatorname{diam}(E_n)<\varepsilon.
$$
그러면 모든 $m\ge n$에 대해
$$
d(p_n,p_m)<\varepsilon.
$$
즉 $\{p_n\}$은 Cauchy sequence이다.

$X$는 complete이므로 어떤 $p\in X$에 대해
$$
p_n\to p.
$$

이제 $p\in E_n$임을 보이자. 고정된 $n$에 대해, 모든 $m\ge n$이면 $p_m\in E_n$이다. 즉 $E_n$ 안의 sequence가 $p$로 수렴한다. $E_n$은 closed이므로
$$
p\in E_n.
$$
이것이 모든 $n$에 대해 성립하므로
$$
p\in \bigcap_{n=1}^\infty E_n.
$$

마지막으로 유일성을 보이자. 만약 $q$도 교집합에 속한다면 모든 $n$에 대해 $p,q\in E_n$이므로
$$
d(p,q)\le \operatorname{diam}(E_n).
$$
$n\to\infty$를 보내면 우변이 0으로 가므로
$$
d(p,q)=0,
$$
따라서 $p=q$.

즉 교집합은 정확히 한 점으로 이루어진다.

---

## Exercise 23

### 문제 원문

Suppose $\{p_n\}$ and $\{q_n\}$ are Cauchy sequences in a metric space $X$. Show that the sequence $\{d(p_n,q_n)\}$ converges. Hint: For any $m,n$,
$$
d(p_n,q_n)\le d(p_n,p_m)+d(p_m,q_m)+d(q_m,q_n);
$$
it follows that
$$
|d(p_n,q_n)-d(p_m,q_m)|
$$
is small if $m$ and $n$ are large.

### 쉬운 해설

목표는 실수수열 $d(p_n,q_n)$이 수렴함을 보이는 것이다. 실수에서는 Cauchy면 수렴하므로, 먼저 이 수열이 Cauchy임을 보이면 된다.

### 완전 풀이

힌트의 부등식을 사용하자:
$$
d(p_n,q_n)\le d(p_n,p_m)+d(p_m,q_m)+d(q_m,q_n).
$$
같은 식에서 $m,n$을 바꾸면
$$
d(p_m,q_m)\le d(p_m,p_n)+d(p_n,q_n)+d(q_n,q_m).
$$
따라서 두 식을 합쳐
$$
|d(p_n,q_n)-d(p_m,q_m)|
\le d(p_n,p_m)+d(q_n,q_m).
$$

이제 $\{p_n\}$과 $\{q_n\}$이 둘 다 Cauchy이므로, 임의의 $\varepsilon>0$에 대해 충분히 큰 $m,n$이면
$$
d(p_n,p_m)<\varepsilon/2,
\qquad
d(q_n,q_m)<\varepsilon/2.
$$
그러면
$$
|d(p_n,q_n)-d(p_m,q_m)|<\varepsilon.
$$
즉 실수수열 $\{d(p_n,q_n)\}$은 Cauchy이다.

실수공간 $\mathbb R$은 complete이므로, 이 수열은 수렴한다.

### 결론

$$
\{d(p_n,q_n)\}\ \text{converges}.
$$
