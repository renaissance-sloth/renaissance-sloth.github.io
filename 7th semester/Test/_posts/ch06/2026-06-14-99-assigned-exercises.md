# 📘 Chapter 6 — Assigned Exercises 완전 풀이

---

이 문서는 Chapter 6 지정 과제

- 1, 2, 3, 4, 6, 7, 8, 11, 12, 19

의 **문제 원문 + 쉬운 해설 + 완전 풀이**를 담는다.

기준 원문:
- `original/06. THE RIEMANN-STIELTJES INTEGRAL.pdf`
- `markdown/2026-06-07-hw3.md`의 Original 블록 보조 사용

---

## Exercise 1

### 문제 원문

Suppose $\alpha$ increases on $[a,b]$, $a\le x_0\le b$, $\alpha$ is continuous at $x_0$, $f(x_0)=1$, and $f(x)=0$ if $x\ne x_0$. Prove that $f\in\mathscr R(\alpha)$ and that $\int_a^b f\,d\alpha=0.$

### 쉬운 해설

함수는 한 점 $x_0$에서만 1이고 나머지는 전부 0이다. 적분값이 0일 것 같은 이유는, integrator $\alpha$가 그 점에서 continuous이면 그 점 하나에 “jump mass”가 없기 때문이다. partition을 $x_0$ 주변에서 아주 작게 잡으면 upper-lower gap도 작아진다.

### 완전 풀이

$f$는 bounded이다. $\varepsilon>0$를 주자. $\alpha$가 $x_0$에서 continuous이므로 어떤 $\delta>0$가 존재하여
$$
|x-x_0|<\delta \implies |\alpha(x)-\alpha(x_0)|<\varepsilon.
$$

이제 partition $P$를 $x_0-\delta<x_1\le x_0\le x_2<x_0+\delta$가 되게 잡고, 나머지 구간은 임의로 완성하자. 그러면 $x_0$를 포함하지 않는 모든 구간에서는 $f\equiv0$이므로 그 구간들에 대해
$$
M_i=m_i=0.
$$
오직 $x_0$를 포함하는 한 구간에서만 $M_i=1, m_i=0$일 수 있다. 따라서
$$
U(P,f,\alpha)-L(P,f,\alpha)
\le \alpha(x_2)-\alpha(x_1).
$$
그런데 monotonicity 때문에
$$
\alpha(x_2)-\alpha(x_1)
\le [\alpha(x_2)-\alpha(x_0)]+[\alpha(x_0)-\alpha(x_1)]<2\varepsilon.
$$
따라서 Theorem 6.6에 의해 $f\in\mathscr R(\alpha)$.

또 lower sum은 항상 0이고, 위의 partition들에 대해 upper sum은 0에 임의로 가깝게 만들 수 있으므로
$$
\int_a^b f\,d\alpha=0.
$$

### 결론

$f$는 $\alpha$에 대해 적분 가능하고, 적분값은 0이다.

---

## Exercise 2

### 문제 원문

Suppose $f\ge0$, $f$ is continuous on $[a,b]$, and $\int_a^b f(x)\,dx=0.$ Prove that $f(x)=0$ for all $x\in[a,b]$. Compare this with Exercise 1.

### 쉬운 해설

연속이고 0 이상인 함수가 어느 한 점에서라도 양수라면, 그 주변 작은 구간 전체에서 양수여야 한다. 그러면 적분이 양수가 되어 모순이다.

### 완전 풀이

모순을 위해 어떤 $x_0\in[a,b]$에서 $f(x_0)>0$라 하자. 연속성이 있으므로 어떤 $\delta>0$가 존재하여
$$
|x-x_0|<\delta \implies f(x) > \frac{f(x_0)}{2}>0.
$$
이제 $I=[x_0-\delta,x_0+\delta]\cap[a,b]$를 잡으면 길이 $|I|>0$이고, 모든 $x\in I$에 대해
$$
f(x)\ge \frac{f(x_0)}2.
$$
따라서
$$
\int_a^b f(x)dx\ge \int_I f(x)dx\ge \frac{f(x_0)}2|I|>0,
$$
이는 가정 $\int_a^b f(x)dx=0$와 모순이다. 따라서 모든 $x\in[a,b]$에 대해
$$
f(x)=0.
$$

Exercise 1과 비교하면, 거기서는 함수가 한 점에서만 1이고 나머지에서 0이었지만 continuous가 아니므로 적분이 0이 될 수 있었다. 여기서는 continuity가 있어 그런 “point mass” 현상이 불가능하다.

### 결론

$f\ge0$, continuous, integral 0이면 $f\equiv0$이다.

---

## Exercise 3

### 문제 원문

Define three functions $\beta_1,\beta_2,\beta_3$ as follows: $\beta_j(x)=0$ if $x<0$, $\beta_j(x)=1$ if $x>0$, for $j=1,2,3$; and $\beta_1(0)=0,\ \beta_2(0)=1,\ \beta_3(0)=\frac12.$ Let $f$ be a bounded function on $[-1,1]$. (a) Prove that $f\in\mathscr R(\beta_1)$ if and only if $f(0+)=f(0)$, and that then $\int f\,d\beta_1=f(0).$ (b) State and prove a similar result for $\beta_2$. (c) Prove that $f\in\mathscr R(\beta_3)$ if and only if $f$ is continuous at $0$. (d) If $f$ is continuous at $0$, prove that $\int f\,d\beta_1=\int f\,d\beta_2=\int f\,d\beta_3=f(0).$

### 쉬운 해설

이 적분자들은 모두 0에서만 jump를 가진다. 그래서 적분은 사실상 0 근처의 함수값 하나를 뽑아내는 장치다. jump가 오른쪽 기준인지, 왼쪽 기준인지, 양쪽 평균인지에 따라 적분 가능 조건이 달라진다.

### 완전 풀이

$\beta_1$은 0에서만 jump를 가진다. partition을 0을 중심으로 잡으면 모든 다른 구간에서는 $\Delta\beta_i=0$, 오직 0을 가로지르는 구간에서만 기여가 생긴다.

#### (a) $\beta_1$

$f\in\mathscr R(\beta_1)$라면, 적분 가능 criterion에 의해 0을 포함하는 작은 오른쪽 구간에서 $M_i-m_i$를 임의로 작게 해야 한다. 그런데 $\Delta\beta_1=1$의 기여는 정확히 오른쪽에서 발생하므로, 이것은 바로
$$
f(0+)=f(0)
$$
와 동치다.

반대로 $f(0+)=f(0)$이면, 0의 오른쪽 작은 구간에서 함수값이 $f(0)$에 가깝고 나머지 구간은 $\Delta\beta=0$이므로 upper-lower gap을 임의로 작게 만들 수 있다. 따라서 적분 가능.

적분값은 0을 가로지르는 구간에서의 대표값 $f(0)$만 남으므로
$$
\int f\,d\beta_1=f(0).
$$

#### (b) $\beta_2$

완전히 대칭적으로
$$
f\in\mathscr R(\beta_2)
\iff
f(0-)=f(0),
\qquad
\int f\,d\beta_2=f(0).
$$

#### (c) $\beta_3$

$\beta_3$는 0에서 jump를 반반 양쪽에 나누는 효과를 가진다. 적분 가능하려면 오른쪽과 왼쪽 모두에서 함수값이 같은 값 $f(0)$에 가까워져야 한다. 즉
$$
f\in\mathscr R(\beta_3)
\iff
f\text{ is continuous at }0.
$$

#### (d)

$f$가 0에서 continuous이면
$$
f(0+)=f(0-)=f(0),
$$
이므로 (a), (b), (c)에서 모두 적분 가능하고, 값은 전부
$$
f(0)
$$
가 된다:
$$
\int f\,d\beta_1=
\int f\,d\beta_2=
\int f\,d\beta_3=f(0).
$$

### 결론

- $\beta_1$: 오른쪽 연속성이 필요
- $\beta_2$: 왼쪽 연속성이 필요
- $\beta_3$: 양쪽 연속성, 즉 continuity at 0가 필요

---

## Exercise 4

### 문제 원문

If $f(x)=0$ for all irrational $x$, $f(x)=1$ for all rational $x$, prove that $f\notin\mathscr R$ on $[a,b]$ for any $a<b$.

### 쉬운 해설

모든 구간에 rational과 irrational이 둘 다 들어 있으므로, 어느 subinterval에서도 supremum은 1, infimum은 0이다. 따라서 upper sum은 항상 $b-a$, lower sum은 항상 0이다. gap이 절대 줄어들지 않는다.

### 완전 풀이

임의의 partition $P=\{x_0,\dots,x_n\}$를 잡자. 각 subinterval $[x_{i-1},x_i]$에는 rational과 irrational이 둘 다 조밀하게 존재하므로
$$
M_i=1,
\qquad
m_i=0.
$$
따라서
$$
U(P,f)=\sum_{i=1}^n 1\cdot \Delta x_i=b-a,
\qquad
L(P,f)=\sum_{i=1}^n 0\cdot\Delta x_i=0.
$$
즉 모든 partition에 대해
$$
U(P,f)-L(P,f)=b-a>0.
$$
따라서 Theorem 6.6의 criterion이 절대로 만족될 수 없으므로
$$
f\notin\mathscr R\text{ on }[a,b].
$$

### 결론

Dirichlet 함수는 어떤 구간에서도 Riemann 적분 가능하지 않다.

---

## Exercise 6

### 문제 원문

Let $P$ be the Cantor set constructed in Sec. 2.44. Let $f$ be a bounded real function on $[0,1]$ which is continuous at every point outside $P$. Prove that $f\in\mathscr R$ on $[0,1]$. Hint: $P$ can be covered by finitely many segments whose total length can be made as small as desired. Proceed as in Theorem 6.10.

### 쉬운 해설

Cantor set는 measure 0 성질 때문에 총 길이가 임의로 작은 유한 개 구간으로 덮을 수 있다. 나쁜 점은 모두 그 안에 몰아넣고, 나머지 좋은 부분에서는 uniform continuity를 쓰면 된다. Theorem 6.10의 finite discontinuity proof를 그대로 일반화하는 구조다.

### 완전 풀이

$f$는 bounded이므로 $|f|\le M$이라 하자. $\varepsilon>0$를 주자. Cantor set $P$는 총 길이가
$$
<\frac{\varepsilon}{2M}
$$
이 되도록 유한 개의 닫힌 구간
$$
[u_j,v_j]
$$
들로 덮을 수 있다.

이제 이 구간들의 interior를 제거한 나머지 집합을 $K$라 하자. $K$는 compact이고, $f$는 $K$ 위에서 continuous이다. 왜냐하면 $K$의 모든 점은 $P$ 밖에 있으므로 연속점이기 때문이다. 따라서 $f$는 $K$ 위에서 uniformly continuous이다. 그러므로 어떤 $\delta>0$가 존재하여
$$
x,y\in K,\ |x-y|<\delta
\implies
|f(x)-f(y)|<\varepsilon.
$$

이제 partition $P^*$를 다음처럼 잡는다.

- 모든 $u_j,v_j$를 partition point에 포함
- 각 좋은 구간에서는 mesh를 $<\delta$로 만듦
- 나쁜 구간 $[u_j,v_j]$ 안에는 더 이상 점을 넣지 않음

좋은 subinterval들에서는 oscillation이 $<\varepsilon$, 나쁜 subinterval들에서는 oscillation이 최대 $2M$이다. 따라서
$$
U(P^*,f)-L(P^*,f)
\le \varepsilon\cdot 1 + 2M\sum_j (v_j-u_j)
<\varepsilon + 2M\cdot \frac{\varepsilon}{2M}=2\varepsilon.
$$
Theorem 6.6에 의해 $f\in\mathscr R$이다.

### 결론

Cantor set 위에서만 불연속일 수 있는 bounded function은 여전히 Riemann 적분 가능하다.

---

## Exercise 7

### 문제 원문

Suppose $f$ is a real function on $(0,1]$ and $f\in\mathscr R$ on $[c,1]$ for every $c>0$. Define $\int_0^1 f(x)\,dx=\lim_{c\to0}\int_c^1 f(x)\,dx$ if this limit exists and is finite. (a) If $f\in\mathscr R$ on $[0,1]$, show that this definition of the integral agrees with the old one. (b) Construct a function $f$ such that the above limit exists, although it fails to exist with $|f|$ in place of $f$.

### 쉬운 해설

(a)는 구간 분할 성질로 바로 된다. (b)는 부호가 번갈아가며 cancellation이 일어나는 예를 만들면 된다. 가장 전형적인 것은 $\sin(1/x)/x$ 타입이지만 Riemann 설정에서는 piecewise constant oscillating example을 만드는 것이 더 쉽다.

### 완전 풀이

#### (a)

$f\in\mathscr R$ on $[0,1]$라 하자. 그러면 Theorem 6.12(c)에 의해 모든 $c\in(0,1)$에 대해
$$
\int_0^1 f(x)dx= \int_0^c f(x)dx+ \int_c^1 f(x)dx.
$$
$f\in\mathscr R$ on $[0,1]$이므로 $\int_0^c f(x)dx\to0$ as $c\to0^+$. 따라서
$$
\lim_{c\to0^+}\int_c^1 f(x)dx= \int_0^1 f(x)dx.
$$
즉 새 정의는 old one과 일치한다.

#### (b)

예를 들어
$$
f(x)=(-1)^n n
\qquad \text{for }\frac1{n+1}<x\le \frac1n
$$
로 두자. 각 $[c,1]$에서는 유한개 jump만 가지므로 Riemann integrable이다. 또한
$$
\int_{1/(n+1)}^{1/n} f(x)dx = (-1)^n n\left(\frac1n-\frac1{n+1}\right)=(-1)^n\frac1{n+1}.
$$
따라서 improper integral은 essentially alternating harmonic tail이 되어 수렴한다. 즉
$$
\lim_{c\to0^+}\int_c^1 f(x)dx
$$
는 존재한다.

하지만 절댓값을 취하면 각 구간 적분이
$$
\int_{1/(n+1)}^{1/n} |f(x)|dx = \frac1{n+1},
$$
가 되어 harmonic tail이므로
$$
\lim_{c\to0^+}\int_c^1 |f(x)|dx
$$
는 발산한다.

### 결론

- old integral이 존재하면 새 정의와 일치한다.
- cancellation 때문에 improper integral은 존재하지만 absolute version은 존재하지 않는 예가 있다.

---

## Exercise 8

### 문제 원문

Suppose $f\in\mathscr R$ on $[a,b]$ for every $b>a$, where $a$ is fixed. Define $\int_a^\infty f(x)\,dx=\lim_{b\to\infty}\int_a^b f(x)\,dx$ if this limit exists and is finite. In that case, we say that the integral on the left converges. If it also converges after $f$ has been replaced by $|f|$, it is said to converge absolutely. Assume that $f(x)\ge0$ and that $f$ decreases monotonically on $[1,\infty)$. Prove that $\int_1^\infty f(x)\,dx$ converges if and only if $\sum_{n=1}^{\infty} f(n)$ converges. This is the integral test for convergence of series.

### 쉬운 해설

감소함수에서는 각 단위 구간 $[n,n+1]$ 위의 함수값이 $f(n)$와 $f(n+1)$ 사이에 낀다. 그래서 적분은 합과 거의 같은 크기다.

### 완전 풀이

$f$가 $[1,\infty)$에서 감소하고 $f\ge0$라 하자. 그러면 각 정수 $n\ge1$와 $x\in[n,n+1]$에 대해
$$
f(n+1)\le f(x)\le f(n).
$$
적분하면
$$
f(n+1)\le \int_n^{n+1} f(x)dx \le f(n).
$$
이제 $n=1,\dots,N$에 대해 합하면
$$
\sum_{n=1}^{N} f(n+1)
\le \int_1^{N+1} f(x)dx
\le \sum_{n=1}^{N} f(n).
$$
즉
$$
\sum_{n=2}^{N+1} f(n)
\le \int_1^{N+1} f(x)dx
\le \sum_{n=1}^{N} f(n).
$$

따라서 partial sums와 truncated integrals는 서로 위아래에서 끼어 있다. 한쪽이 bounded이면 다른쪽도 bounded이고, 양쪽 다 monotone increasing이므로 boundedness와 convergence가 동치다. 따라서
$$
\int_1^{\infty} f(x)dx\text{ converges }
\iff
\sum_{n=1}^{\infty} f(n)\text{ converges}.
$$

### 결론

감소하는 양의 함수에 대해 improper integral과 corresponding series는 동시에 수렴하거나 동시에 발산한다.

---

## Exercise 11

### 문제 원문

Let $\alpha$ be a fixed increasing function on $[a,b]$. For $u\in\mathscr R(\alpha)$, define $|u|_2= \left\{ \int_a^b |u|^2\,d\alpha \right\}^{1/2}.$ Suppose $f,g,h\in\mathscr R(\alpha)$, and prove the triangle inequality $|f-h|_2\le |f-g|_2+|g-h|_2$ as a consequence of the Schwarz inequality, as in the proof of Theorem 1.37.

### 쉬운 해설

이건 정확히 $L^2$-norm의 triangle inequality다. scalar inner-product proof를 그대로 쓰면 된다.

### 완전 풀이

$u=f-g$, $v=g-h$라 두면
$$
f-h=u+v.
$$
따라서
$$
|f-h|_2^2
=\int_a^b |u+v|^2\,d\alpha
=\int_a^b (u+v)^2\,d\alpha
$$
실수값으로 생각하면
$$
=\int u^2\,d\alpha +2\int uv\,d\alpha + \int v^2\,d\alpha.
$$
Schwarz inequality에 의해
$$
\left|\int uv\,d\alpha\right|\le \left(\int u^2 d\alpha\right)^{1/2}\left(\int v^2 d\alpha\right)^{1/2}=|u|_2|v|_2.
$$
따라서
$$
|f-h|_2^2\le |u|_2^2+2|u|_2|v|_2+|v|_2^2=(|u|_2+|v|_2)^2.
$$
양변 제곱근을 취하면
$$
|f-h|_2\le |u|_2+|v|_2=|f-g|_2+|g-h|_2.
$$

### 결론

$|\cdot|_2$는 triangle inequality를 만족한다.

---

## Exercise 12

### 문제 원문

With the notations of Exercise 11, suppose $f\in\mathscr R(\alpha)$ and $\varepsilon>0$. Prove that there exists a continuous function $g$ on $[a,b]$ such that $|f-g|_2<\varepsilon.$ Hint: Let $P=\{x_0,\dots,x_n\}$ be a suitable partition of $[a,b]$, define $g(t)=f(x_i)\quad\text{if }x_{i-1}<t<x_i,$ and then modify $g$ in a suitable way.

### 쉬운 해설

적분 가능한 함수는 step function으로 $L^2$에서 가깝게 근사할 수 있고, 그 step function은 끝점에서만 불연속이므로 조금만 다듬으면 continuous function으로 바꿀 수 있다. 다듬는 구간의 $\alpha$-mass를 작게 잡으면 오차는 그대로 작게 유지된다.

### 완전 풀이

$f\in\mathscr R(\alpha)$이고 $\varepsilon>0$라 하자. integrability criterion에 의해 적당한 partition $P=\{x_0,\dots,x_n\}$를 잡아 각 구간에서 oscillation이 작게 되도록 할 수 있다. 힌트대로 step function
$$
s(t)=f(x_i)
\qquad (x_{i-1}<t<x_i)
$$
를 정의하고, 끝점에서는 임의로 정의하자.

적분가능성 때문에 이 step approximation은 $|f-s|_2$를 충분히 작게 만들 수 있다. 왜냐하면 각 subinterval에서 $|f(t)-f(x_i)|^2$가 oscillation 제곱으로 제어되고, 그 weighted sum을 작게 만들 수 있기 때문이다.

이제 $s$는 partition points에서만 불연속이다. 각 partition point 주변의 아주 짧은 interval을 하나씩 잡아 그 안에서 선형보간으로 이어붙인 continuous function $g$를 만든다. 이 수정은 유한 개의 작은 구간에서만 일어나므로, 그 구간들의 전체 $\alpha$-mass를 충분히 작게 잡으면
$$
|g-s|_2<\varepsilon/2
$$
가 되게 할 수 있다.

또 처음부터 $|f-s|_2<\varepsilon/2$가 되게 만들면 triangle inequality로
$$
|f-g|_2\le |f-s|_2+|s-g|_2<\varepsilon.
$$

### 결론

$\mathscr R(\alpha)$의 함수는 $|\cdot|_2$-norm에서 continuous functions로 근사될 수 있다.

---

## Exercise 19

### 문제 원문

Let $\gamma_1$ be a curve in $\mathbb R^k$, defined on $[a,b]$; let $\phi$ be a continuous one-to-one mapping of $[c,d]$ onto $[a,b]$, such that $\phi(c)=a$; and define $\gamma_2(s)=\gamma_1(\phi(s)).$ Prove that $\gamma_2$ is an arc, a closed curve, or a rectifiable curve if and only if the same is true of $\gamma_1$. Prove that $\gamma_2$ and $\gamma_1$ have the same length.

### 쉬운 해설

$\phi$는 parameter만 다시 매기는 것이다. 따라서 geometric image는 바뀌지 않는다. 길이도 partition correspondence를 쓰면 같아진다.

### 완전 풀이

$\phi:[c,d]\to[a,b]$는 continuous one-to-one onto mapping이고 $\phi(c)=a$이다. interval 위 continuous injective map은 monotone이므로, $\phi$는 strictly increasing이다. 따라서 partition
$$
Q=\{y_0,\dots,y_n\}
\subset[c,d]
$$
에 대응하여
$$
P=\{x_i=\phi(y_i)
\}
\subset[a,b]
$$
를 잡을 수 있다.

먼저 arc 성질: $\gamma_2$가 one-to-one iff $\gamma_1$이 one-to-one이다. 왜냐하면 $\phi$가 one-to-one onto이므로 parameter 중복이 정확히 보존되기 때문이다.

closed curve 성질도
$$
\gamma_2(c)=\gamma_1(\phi(c))=\gamma_1(a),
\qquad
\gamma_2(d)=\gamma_1(\phi(d))=\gamma_1(b)
$$
이므로 $\gamma_2(c)=\gamma_2(d)\iff \gamma_1(a)=\gamma_1(b)$.

이제 길이를 보자. 대응하는 partitions에 대해
$$
\Lambda(Q,\gamma_2)
=\sum_{i=1}^n |\gamma_2(y_i)-\gamma_2(y_{i-1})|
=\sum_{i=1}^n |\gamma_1(x_i)-\gamma_1(x_{i-1})|
=\Lambda(P,\gamma_1).
$$
즉 polygonal sums가 정확히 일치한다. 따라서 모든 partition에 대해 supremum을 취하면
$$
\Lambda(\gamma_2)=\Lambda(\gamma_1).
$$
그러므로 한 곡선이 rectifiable iff 다른 곡선도 rectifiable이다.

### 결론

parameter의 연속적 one-to-one 재조정은 arc, closed-curve, rectifiable 성질을 모두 보존하며, 두 곡선의 길이도 같다.
