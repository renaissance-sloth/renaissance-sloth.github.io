# 📘 Chapter 7 — Assigned Exercises 완전 풀이

---

이 문서는 Chapter 7 지정 과제

- 1, 2, 3, 5, 7, 9, 11, 15, 16, 18

의 **문제 원문 + 쉬운 해설 + 완전 풀이**를 담는다.

기준 원문:
- `original/07. SEQUENCES AND SERIES OF FUNCTIONS.pdf`
- `markdown/2026-06-10-hw4.md`의 Original 블록 보조 사용

---

## Exercise 1

### 문제 원문

Prove that every uniformly convergent sequence of bounded functions is uniformly bounded.

### 쉬운 해설

uniform convergence는 뒤쪽 함수들이 limit function 근처에 한꺼번에 붙는다는 뜻이다. 그러므로 충분히 큰 index 이후의 함수들은 하나의 bounded function 근처에 있으니 전부 bounded다. 앞의 유한 개 함수는 원래 bounded이므로 전체가 uniformly bounded가 된다.

### 완전 풀이

$f_n\to f$ uniformly on $E$라고 하자. 각 $f_n$은 bounded function이라고 가정한다.

uniform convergence에 의해 $\varepsilon=1$을 택하면 어떤 $N$이 존재하여
$$
n\ge N \implies |f_n(x)-f(x)|<1
\qquad (x\in E).
$$

또 $f_N$는 bounded이므로 어떤 상수 $M_N<\infty$가 존재하여
$$
|f_N(x)|\le M_N
\qquad (x\in E).
$$
따라서 모든 $n\ge N$, 모든 $x\in E$에 대해
$$
|f_n(x)|
\le |f_n(x)-f_N(x)|+|f_N(x)|.
$$
여기서
$$
|f_n(x)-f_N(x)|
\le |f_n(x)-f(x)|+|f(x)-f_N(x)|<2,
$$
이므로
$$
|f_n(x)|\le M_N+2.
$$

이제 처음 유한 개 함수 $f_1,\dots,f_{N-1}$는 각각 bounded이므로 상수 $M_1,\dots,M_{N-1}$를 잡아
$$
|f_k(x)|\le M_k 
\qquad (x\in E)
$$
가 되게 할 수 있다.

그러면
$$
M=\max\{M_1,\dots,M_{N-1},M_N+2\}
$$
를 잡으면 모든 $n$과 모든 $x\in E$에 대해
$$
|f_n(x)|\le M.
$$
즉 $\{f_n\}$은 uniformly bounded이다.

### 결론

uniformly convergent sequence of bounded functions는 반드시 uniformly bounded이다.

---

## Exercise 2

### 문제 원문

If $(f_n)$ and $(g_n)$ converge uniformly on a set $E$, prove that $(f_n+g_n)$ converges uniformly on $E$. If, in addition, $(f_n)$ and $$g_n)$ are sequences of bounded functions, prove that $(f_ng_n)$ converges uniformly on $E$.

### 쉬운 해설

합은 triangle inequality로 바로 된다. 곱은
$$
f_ng_n-fg=f_n(g_n-g)+g(f_n-f)
$$
로 쪼개고, 한쪽 factor의 uniform boundedness를 써서 조절하면 된다.

### 완전 풀이

$f_n\to f$, $g_n\to g$ uniformly on $E$라 하자.

#### (i) Sum

임의의 $x\in E$에 대해
$$
|(f_n+g_n)(x)-(f+g)(x)|
\le |f_n(x)-f(x)|+|g_n(x)-g(x)|.
$$
sup를 취하면
$$
\sup_E |(f_n+g_n)-(f+g)|
\le \sup_E|f_n-f|+\sup_E|g_n-g|.
$$
오른쪽이 0으로 가므로 $f_n+g_n\to f+g$ uniformly.

#### (ii) Product

추가로 각 $f_n,g_n$이 bounded function이라 하자. Exercise 1에 의해 $\{f_n\}$과 $\{g_n\}$은 uniformly bounded이다. 또한 uniform limit $g$도 bounded이다.

따라서 상수 $A,B<\infty$가 존재하여
$$
|f_n(x)|\le A,
\qquad
|g(x)|\le B
\qquad (x\in E,
\ n\ge1).
$$

이제
$$
f_ng_n-fg=f_n(g_n-g)+g(f_n-f)
$$
이므로
$$
|f_ng_n-fg|
\le |f_n||g_n-g|+|g||f_n-f|
\le A|g_n-g|+B|f_n-f|.
$$
sup를 취하면
$$
\sup_E|f_ng_n-fg|
\le A\sup_E|g_n-g|+B\sup_E|f_n-f|\to0.
$$
따라서 $f_ng_n\to fg$ uniformly on $E$.

### 결론

- uniform convergence는 덧셈에 대해 닫혀 있다.
- boundedness가 추가되면 곱에 대해서도 닫혀 있다.

---

## Exercise 3

### 문제 원문

Construct sequences $(f_n),(g_n)$ which converge uniformly on some set $E$, but such that $(f_ng_n)$ does not converge uniformly on $E$ — of course, $(f_ng_n)$ must converge on $E$.

### 쉬운 해설

boundedness 가정이 빠지면 Exercise 2의 product part는 거짓이다. 가장 쉬운 예는
$$
f_n(x)=x+1/n,
\qquad
g_n(x)=x+1/n
$$
on $E=\mathbb R$이다. 각각은 $x$로 uniformly converge하지만, 곱은 $x^2$로 uniformly converge하지 않는다.

### 완전 풀이

$E=\mathbb R$로 두고
$$
f_n(x)=x+\frac1n,
\qquad
g_n(x)=x+\frac1n
$$
로 정의하자. 그러면
$$
f(x)=x,
\qquad
g(x)=x.
$$

각 $x\in\mathbb R$에 대해
$$
|f_n(x)-f(x)|=\frac1n,
\qquad
|g_n(x)-g(x)|=\frac1n.
$$
따라서
$$
\sup_{x\in\mathbb R}|f_n(x)-x|=\frac1n\to0,
\qquad
\sup_{x\in\mathbb R}|g_n(x)-x|=\frac1n\to0.
$$
즉 둘 다 uniformly converge한다.

한편
$$
f_n(x)g_n(x)=\left(x+\frac1n\right)^2=x^2+\frac{2x}{n}+\frac1{n^2}.
$$
pointwise로는 분명히 $x^2$로 간다. 하지만
$$
|f_n(x)g_n(x)-x^2|=
\left|\frac{2x}{n}+\frac1{n^2}\right|.
$$
예를 들어 $x=n^2$를 넣으면
$$
\left|\frac{2x}{n}+\frac1{n^2}\right|=2n+\frac1{n^2},
$$
따라서 sup가 0으로 갈 수 없다. 즉 $f_ng_n$은 $x^2$로 uniformly converge하지 않는다.

### 결론

uniform convergence의 곱 보존에는 boundedness 가정이 필요하다.

---

## Exercise 5

### 문제 원문

Let
$$
f_n(x)= 
\begin{cases} 
0,& x<\dfrac1{n+1},\$$2mm]
\sin^2\dfrac{\pi}{x},& \dfrac1{n+1}\le x\le \dfrac1n,\$$2mm]
0,& \dfrac1n<x.
\end{cases}
$$
Show that $(f_n)$ converges to a continuous function, but not uniformly. Use the series $\sum f_n$ to show that absolute convergence, even for all $x$, does not imply uniform convergence.

### 쉬운 해설

각 $x\neq0$에 대해서는 충분히 큰 $n$이면 $x$가 support 밖으로 나가므로 결국 0이 된다. 따라서 pointwise limit는 0이고 continuous하다. 하지만 각 $n$마다 support 안에서 1을 찍는 점이 있으므로 sup norm은 줄지 않는다.

### 완전 풀이

먼저 pointwise limit를 보자. $x\neq0$이면 어떤 $N$이 존재하여 $n\ge N$이면 $x\notin [1/(n+1),1/n]$. 따라서 $f_n(x)=0$ for all large $n$. 또한 $x=0$에서도 모든 $n$에 대해 $f_n(0)=0$. 그러므로
$$
f_n(x)\to0
\qquad (\forall x).
$$
따라서 limit function은 $f\equiv0$, 이는 continuous이다.

이제 uniform convergence가 아님을 보이자. 각 $n$에 대해
$$
x_n=\frac{2}{2n+1}
$$
라 두면
$$
\frac1{n+1}<x_n<\frac1n,
$$
즉 $x_n$는 support 안에 있다. 그리고
$$
\frac{\pi}{x_n}=\frac{2n+1}{2}\pi=
\left(n+\frac12\right)\pi.
$$
따라서
$$
f_n(x_n)=\sin^2\left(\left(n+\frac12\right)\pi\right)=1.
$$
그러므로
$$
\sup_x |f_n(x)-0|\ge1.
$$
즉 $f_n\not\to0$ uniformly.

이제 series $\sum f_n$를 보자. 각 $x$에 대해 많아야 하나의 $n$만 $f_n(x)\neq0$일 수 있다. 실제로 구간들 $[1/(n+1),1/n]$은 서로 interior disjoint이다. 따라서 각 $x$에서
$$
\sum_{n=1}^{\infty} |f_n(x)|
$$
는 사실 유한합이며, 절대수렴한다. 하지만 partial sums는 $0$으로 uniformly converge하지 않는다. 따라서

> 모든 점에서 absolute convergence한다는 것만으로는 uniform convergence가 따라오지 않는다.

### 결론

$f_n\to0$ pointwise with continuous limit, but not uniformly. 또한 $\sum f_n(x)$는 각 $x$에서 절대수렴해도 uniform convergence는 아니다.

---

## Exercise 7

### 문제 원문

For $n=1,2,3,\ldots$, $x$ real, put
$$
f_n(x)=\frac{x}{1+nx^{2}}.
$$
Show that $(f_n)$ converges uniformly to a function $f$, and that the equation
$$
f'(x)=\lim_{n\to\infty}f_n'(x)
$$
is correct if $x\ne0$, but false if $x=0$.

### 쉬운 해설

먼저 limit function은 0이다. uniform convergence는 sup를 직접 계산하면 된다. derivative는
$$
f_n'(x)=\frac{1-nx^2}{(1+nx^2)^2}
$$
이고, $x\ne0$에서는 0으로 가지만, $x=0$에서는 항상 1이라서 실패한다.

### 완전 풀이

각 fixed $x$에 대해
$$
f_n(x)=\frac{x}{1+nx^2}\to0.
$$
따라서 limit function은 $f\equiv0$.

uniform convergence를 보이기 위해 $x\ge0$만 보면 충분하다. $f_n$은 odd function이기 때문이다. $x\ge0$에서
$$
f_n(x)=\frac{x}{1+nx^2}.
$$
이를 미분하면 최대점은
$$
f_n'(x)=\frac{1-nx^2}{(1+nx^2)^2}=0
\iff x=\frac1{\sqrt n}.
$$
그 점에서
$$
f_n\left(\frac1{\sqrt n}\right)=\frac{1/\sqrt n}{1+n(1/n)}=rac1{2\sqrt n}.
$$
따라서
$$
\sup_{x\in\mathbb R}|f_n(x)|=\frac1{2\sqrt n}\to0.
$$
즉 $f_n\to0$ uniformly.

이제 derivative를 보자.
$$
f_n'(x)=\frac{1-nx^2}{(1+nx^2)^2}.
$$
만약 $x\ne0$이면 $nx^2\to\infty$이므로
$$
f_n'(x)\to0=f'(x).
$$
여기서 $f\equiv0$이므로 $f'(x)=0$.

하지만 $x=0$에서는
$$
f_n'(0)=1
\qquad (\forall n),
$$
따라서
$$
\lim_{n\to\infty}f_n'(0)=1\ne0=f'(0).
$$
즉 derivative와 limit의 교환은 $x=0$에서 실패한다.

### 결론

$f_n\to0$ uniformly이지만, derivative limit는 $x\ne0$에서는 맞고 $x=0$에서는 틀리다.

---

## Exercise 9

### 문제 원문

Let $(f_n)$ be a sequence of continuous functions which converges uniformly to a function $f$ on a set $E$. Prove that
$$
\lim_{n\to\infty} f_n(x_n)=f(x)
$$
for every sequence of points $x_n\in E$ such that $x_n\to x$, and $x\in E$. Is the converse of this true?

### 쉬운 해설

uniform convergence로 $f_n(x_n)$와 $f(x_n)$를 가깝게 만들고, continuity of $f$로 $f(x_n)\to f(x)$를 쓰면 된다. 역은 일반적으로 거짓이다.

### 완전 풀이

Theorem 7.12에 의해 uniform limit $f$는 continuous이다. 이제
$$
|f_n(x_n)-f(x)|
\le |f_n(x_n)-f(x_n)|+|f(x_n)-f(x)|.
$$

첫 항은 uniform convergence 때문에 0으로 가고,
둘째 항은 $x_n\to x$와 $f$의 continuity 때문에 0으로 간다. 따라서
$$
f_n(x_n)\to f(x).
$$

역은 거짓이다. 왜냐하면 이 성질은 함수값을 sequence along diagonal에서만 통제할 뿐, 전체 sup norm이 0으로 가는 것을 강제하지 않기 때문이다. 표준 반례는 적당한 moving spike sequence로 줄 수 있다.

### 결론

uniform convergence이면 diagonal evaluation limit가 따라오지만, converse는 일반적으로 거짓이다.

---

## Exercise 11

### 문제 원문

Suppose $(f_n),(g_n)$ are defined on $E$, and (a) $\sum f_n$ has uniformly bounded partial sums; (b) $g_n\to0$ uniformly on $E$; (c) $g_1(x)\ge g_2(x)\ge g_3(x)\ge\cdots$ for every $x\in E$. Prove that $\sum f_ng_n$ converges uniformly on $E$. Hint: Compare with Theorem 3.42.

### 쉬운 해설

이건 summation by parts / Dirichlet test의 uniform version이다. 각 $x$에 대해만 보는 대신, partial sums boundedness와 $g_n\to0$가 E 전체에서 uniform하게 주어진다.

### 완전 풀이

각 $x$와 $N\le p\le q$에 대해
$$
\sum_{n=p}^q f_n(x)g_n(x)
$$
에 summation by parts를 적용하자. partial sums
$$
F_n(x)=\sum_{k=1}^n f_k(x)
$$
가 uniformly bounded이므로 어떤 $M$이 존재하여
$$
|F_n(x)|\le M
\qquad (x\in E,
\ n\ge1).
$$

또 $g_n\to0$ uniformly이므로 임의의 $\varepsilon>0$에 대해 어떤 $N$이 존재하여
$$
|g_n(x)|<\frac{\varepsilon}{2M}
\qquad (x\in E,
\ n\ge N).
$$
그리고 각 $x$마다 $g_n(x)$는 감소한다. 따라서 scalar Theorem 3.42의 증명과 완전히 같은 estimate가 uniform하게 성립하여
$$
\left|\sum_{n=p}^q f_n(x)g_n(x)\right|<\varepsilon
\qquad (x\in E,
\ q\ge p\ge N).
$$
즉 uniform Cauchy criterion이 성립한다. 따라서
$$
\sum f_ng_n
$$
은 $E$에서 uniformly converge한다.

### 결론

Dirichlet-type 조건의 uniform version 아래에서는 $\sum f_ng_n$이 uniformly converge한다.

---

## Exercise 15

### 문제 원문

Suppose $f$ is a real continuous function on $\mathbb R^1$, $f_n(t)=f(nt)$ for $n=1,2,3,\ldots$, and $(f_n)$ is equicontinuous on $[0,1]$. What conclusion can you draw about $f$?

### 쉬운 해설

equicontinuity on $[0,1]$ means one single $\delta$ works for all $f(nt)$. 그런데 $n$이 커질수록 입력이 빠르게 늘어나므로, 이게 가능하려면 원래 함수 $f$가 사실상 constant여야 한다.

### 완전 풀이

$\{f_n\}$이 $[0,1]$에서 equicontinuous라 하자. 임의의 $\varepsilon>0$에 대해 어떤 $\delta>0$가 존재하여
$$
|s-t|<\delta 
\implies
|f_n(s)-f_n(t)|<\varepsilon
\qquad (n\ge1).
$$

이제 임의의 $x,y\ge0$를 잡자. $n$을 충분히 크게 택해
$$
s=\frac{x}{n},
\qquad
t=\frac{y}{n}
$$
가 둘 다 $[0,1]$ 안에 있고 또한
$$
|s-t|=\frac{|x-y|}{n}<\delta
$$
가 되게 한다. 그러면
$$
|f(x)-f(y)|
=|f_n(s)-f_n(t)|<\varepsilon.
$$
$\varepsilon$ arbitrary이므로 $f(x)=f(y)$ for all $x,y\ge0$. 즉 $[0,\infty)$에서 constant이다.

같은 논리로 $(- \infty,0]$에서도 constant이다. continuity at 0 때문에 양쪽 constant value는 같아야 하므로 $f$는 전체 $\mathbb R$에서 constant이다.

### 결론

주어진 가정 아래 $f$는 constant function이다.

---

## Exercise 16

### 문제 원문

Suppose $(f_n)$ is an equicontinuous sequence of functions on a compact set $K$, and $(f_n)$ converges pointwise on $K$. Prove that $(f_n)$ converges uniformly on $K$.

### 쉬운 해설

pointwise limit를 $f$라 두면, equicontinuity 덕분에 각 함수의 진동이 uniformly controlled된다. compactness로 유한개 점만 보면 되고, pointwise convergence를 거기서 uniform convergence로 퍼뜨릴 수 있다.

### 완전 풀이

pointwise limit를 $f$라 하자. 먼저 $f$가 continuous임을 보이자. $x_n\to x$와 equicontinuity를 쓰면 $f_n(x_n)$와 $f_n(x)$의 차이를 uniformly 작게 만들 수 있고, pointwise convergence를 보내면 $f(x_n)\to f(x)$. 따라서 $f$는 continuous이다.

이제 $g_n=f_n-f$라 두자. $g_n\to0$ pointwise이고, $\{g_n\}$도 equicontinuous이다. 임의의 $\varepsilon>0$에 대해 equicontinuity로 $\delta>0$를 잡는다. compactness로 $K$를 finitely many $\delta$-balls로 덮는 점들 $x_1,\dots,x_m$을 잡는다.

각 $x_j$에서 $g_n(x_j)\to0$이므로, 어떤 $N$이 존재하여
$$
n\ge N \implies |g_n(x_j)|<\varepsilon
\qquad (1\le j\le m).
$$

이제 임의의 $x\in K$를 잡으면 어떤 $j$가 있어 $d(x,x_j)<\delta$. 그러면
$$
|g_n(x)|
\le |g_n(x)-g_n(x_j)|+|g_n(x_j)|.
$$
equicontinuity로 첫 항은 $<\varepsilon$, 두 번째도 $<\varepsilon$, 따라서
$$
|g_n(x)|<2\varepsilon
\qquad (n\ge N,
\ x\in K).
$$
즉 $g_n\to0$ uniformly, 따라서 $f_n\to f$ uniformly.

### 결론

compact set 위에서는 equicontinuity + pointwise convergence가 uniform convergence를 강제한다.

---

## Exercise 18

### 문제 원문

Let $(f_n)$ be a uniformly bounded sequence of functions which are Riemann-integrable on $[a,b]$, and put
$$
F_n(x)=\int_a^x f_n(t)\,dt \qquad (a\le x\le b).
$$
Prove that there exists a subsequence $(F_{n_k})$ which converges uniformly on $[a,b]$.

### 쉬운 해설

$F_n$들을 보면 모두 적분으로 정의된 함수라서 Lipschitz 상수가 공통으로 bounded된다. 즉 equicontinuous family가 된다. 게다가 한 점 $x=a$에서는 전부 0이다. 그래서 Arzelà–Ascoli-type 논리로 uniformly convergent subsequence를 뽑을 수 있다.

### 완전 풀이

$|f_n(t)|\le M$인 공통 상수 $M$가 존재한다고 하자. 그러면 모든 $x,y\in[a,b]$에 대해 (say $x<y$)
$$
|F_n(y)-F_n(x)|
=\left|\int_x^y f_n(t)dt\right|
\le M|y-x|.
$$
따라서 $\{F_n\}$은 $[a,b]$에서 equicontinuous이다.

또한
$$
F_n(a)=0
\qquad (\forall n),
$$
그리고 위 부등식에서
$$
|F_n(x)|=|F_n(x)-F_n(a)|\le M|x-a|\le M(b-a),
$$
이므로 $\{F_n\}$은 uniformly bounded이다. 따라서 pointwise bounded이기도 하다.

이제 $[a,b]$는 compact이고, $F_n\in\mathscr C([a,b])$이며, equicontinuous + pointwise bounded이므로 Theorem 7.25에 의해 $\{F_n\}$은 uniformly convergent subsequence $\{F_{n_k}\}$를 가진다.

### 결론

$F_n(x)=\int_a^x f_n(t)dt$로 만든 함수열은 반드시 uniformly convergent subsequence를 갖는다.
