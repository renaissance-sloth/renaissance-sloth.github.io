# 📘 Chapter 5 — Assigned Exercises 완전 풀이

---

이 문서는 Chapter 5 지정 과제

- 1, 2, 3, 6, 11, 12, 22, 25, 26, 27

의 **문제 원문 + 쉬운 해설 + 완전 풀이**를 담는다.

기준 원문:
- `original/05. DIFFERENTIATION.pdf`
- `markdown/2026-06-07-hw3.md`의 Original 블록 보조 사용

---

## Exercise 1

### 문제 원문

Let $f$ be defined for all real $x$, and suppose that
$$
|f(x)-f(y)|\le (x-y)^2
$$
for all real $x$ and $y$. Prove that $f$ is constant.

### 쉬운 해설

한 번에 $x$에서 $y$로 가지 말고, $[x,y]$를 $n$등분해서 조금씩 이동한다. 각 작은 구간에서의 함수값 차이는 길이의 제곱으로 눌리므로, 전부 더해도 전체 차이가 $(y-x)^2/n$ 이하가 된다. $n\to\infty$를 보내면 차이가 0이다.

### 완전 풀이

임의의 $x<y$를 잡고
$$
x_k=x+\frac{k}{n}(y-x)
\qquad (k=0,1,\dots,n)
$$
로 두자. 그러면 $x_0=x$, $x_n=y$, 그리고
$$
x_k-x_{k-1}=\frac{y-x}{n}.
$$

이제 telescoping sum으로
$$
f(y)-f(x)=\sum_{k=1}^n\bigl(f(x_k)-f(x_{k-1})\bigr).
$$
따라서 triangle inequality와 가정으로
$$
|f(y)-f(x)|
\le \sum_{k=1}^n |f(x_k)-f(x_{k-1})|
\le \sum_{k=1}^n \left(\frac{y-x}{n}\right)^2
=n\cdot\frac{(y-x)^2}{n^2}
=\frac{(y-x)^2}{n}.
$$
이 부등식은 모든 양의 정수 $n$에 대해 성립한다. 따라서 $n\to\infty$를 보내면
$$
0\le |f(y)-f(x)|\le \frac{(y-x)^2}{n}\to0,
$$
즉
$$
f(y)=f(x).
$$
$x,y$가 arbitrary이므로 $f$는 상수함수이다.

### 결론

$$
f(x)=C\qquad (\forall x\in\mathbb R).
$$

---

## Exercise 2

### 문제 원문

Suppose $f'(x)>0$ in $(a,b)$. Prove that $f$ is strictly increasing in $(a,b)$, and let $g$ be its inverse function. Prove that $g$ is differentiable, and that
$$
g'(f(x))=\frac{1}{f'(x)}\qquad (a<x<b).
$$

### 쉬운 해설

증가성은 mean value theorem 한 번이면 끝난다. 역함수의 미분은 difference quotient를 뒤집어서 보면 된다.

### 완전 풀이

먼저 strict increase를 보이자. $a<x_1<x_2<b$를 잡으면 mean value theorem에 의해 어떤 $c\in(x_1,x_2)$가 존재하여
$$
f(x_2)-f(x_1)=(x_2-x_1)f'(c).
$$
그런데 $x_2-x_1>0$이고 $f'(c)>0$이므로
$$
f(x_2)-f(x_1)>0.
$$
따라서 $f$는 $(a,b)$에서 strictly increasing이다.

strictly increasing이므로 $f$는 one-to-one이고 inverse $g=f^{-1}$가 $f((a,b))$ 위에 존재한다.

이제 $y=f(x)$라고 하자. $s\to y$이고 $s\ne y$일 때 $t=g(s)$라 두면 $t\to x$이다. 왜냐하면 $f$가 strictly increasing이고 continuous이므로 역함수 역시 점근적으로 값이 따라오기 때문이다. 이제
$$
\frac{g(s)-g(y)}{s-y}
=\frac{t-x}{f(t)-f(x)}
=\left(\frac{f(t)-f(x)}{t-x}\right)^{-1}.
$$
$s\to y$, 즉 $t\to x$를 보내면
$$
g'(y)=\frac1{f'(x)}.
$$
여기서 $y=f(x)$였으므로
$$
g'(f(x))=\frac1{f'(x)}.
$$

### 결론

$f$는 strictly increasing이고, inverse $g$는 differentiable이며
$$
g'(f(x))=\frac1{f'(x)}.
$$

---

## Exercise 3

### 문제 원문

Suppose $g$ is a real function on $\mathbb R^1$, with bounded derivative, say $|g'|\le M$. Fix $\varepsilon>0$, and define
$$
f(x)=x+\varepsilon g(x).
$$
Prove that $f$ is one-to-one if $\varepsilon$ is small enough. An admissible set of values of $\varepsilon$ can be determined which depends only on $M$.

### 쉬운 해설

핵심은 $f'$를 보면 된다.
$$
f'(x)=1+\varepsilon g'(x).
$$
$|g'|\le M$이므로 $\varepsilon M<1$이면 항상 $f'(x)>0$. 그러면 mean value theorem으로 $f$는 strictly increasing, hence one-to-one이다.

### 완전 풀이

$f'(x)=1+\varepsilon g'(x)$이다. 가정 $|g'(x)|\le M$에 의해
$$
f'(x)\ge 1-\varepsilon M.
$$
따라서 만약
$$
0<\varepsilon<\frac1M
\qquad (M>0)
$$
이면 모든 $x$에 대해
$$
f'(x)>0.
$$
그러므로 Exercise 2의 첫 부분 또는 mean value theorem에 의해 $f$는 strictly increasing이다. 따라서 one-to-one.

만약 $M=0$이면 $g'(x)=0$ for all $x$, 따라서 $g$는 constant이고
$$
f(x)=x+\varepsilon C
$$
꼴이므로 모든 $\varepsilon>0$에 대해 one-to-one이다.

### 결론

허용 가능한 범위는
$$
M>0\implies 0<\varepsilon<\frac1M,
$$
그리고 $M=0$이면 모든 $\varepsilon>0$가 가능하다.

---

## Exercise 6

### 문제 원문

Suppose (a) $f$ is continuous for $x\ge 0$, (b) $f'(x)$ exists for $x>0$, (c) $f'(0)=0$, (d) $f'$ is monotonically increasing. Put
$$
g(x)=\frac{f(x)}{x}\qquad (x>0)
$$
and prove that $g$ is monotonically increasing.

### 쉬운 해설

이 문제는 원문 그대로는 **거짓**이다. 반례로 $f(x)=1$을 잡으면 조건 (a), (b), (c), (d)를 만족하지만
$$
g(x)=1/x
$$
는 감소한다. 그래서 실제로는 보통 $f(0)=0$가 추가되어야 맞는 명제가 된다. 아래에서는 원문을 보존하면서, 먼저 반례를 적고, 이어서 **수정된 참 명제**를 증명한다.

### 완전 풀이

#### 1. 원문이 왜 거짓인가

$$
f(x)=1 \qquad (x\ge0)
$$
로 두자. 그러면

- $f$는 $x\ge0$에서 continuous,
- $x>0$에서 $f'(x)=0$,
- one-sided derivative $f'(0)=0$,
- $f'$는 constant이므로 monotonically increasing.

하지만
$$
g(x)=\frac{1}{x}
\qquad (x>0)
$$
는 monotonically decreasing이다. 따라서 원문은 false이다.

#### 2. 수정된 참 명제: 추가로 $f(0)=0$를 가정

이제 $f(0)=0$까지 추가로 가정하고 $g$가 증가함을 보이자.

$x>0$에서
$$
g(x)=\frac{f(x)}x.
$$
quotient rule에 의해
$$
g'(x)=\frac{xf'(x)-f(x)}{x^2}.
$$
따라서 $g'(x)\ge0$임을 보이면 충분하다.

mean value theorem을 $[0,x]$에 적용하면 어떤 $c_x\in(0,x)$가 존재하여
$$
f(x)-f(0)=xf'(c_x).
$$
이제 $f(0)=0$이므로
$$
f(x)=xf'(c_x).
$$
또 $f'$가 증가함수이므로 $c_x<x$에서
$$
f'(c_x)\le f'(x).
$$
따라서
$$
f(x)=xf'(c_x)\le xf'(x).
$$
즉
$$
xf'(x)-f(x)\ge0,
$$
그러므로
$$
g'(x)=\frac{xf'(x)-f(x)}{x^2}\ge0.
$$
따라서 $g$는 $(0,\infty)$에서 monotonically increasing이다.

### 결론

원문 그대로는 거짓이며, $f(0)=0$가 추가되어야 참이다. 그 수정된 명제 아래에서는 $g(x)=f(x)/x$가 증가한다.

---

## Exercise 11

### 문제 원문

Suppose $f$ is defined in a neighborhood of $x$, and suppose $f''(x)$ exists. Show that
$$
\lim_{h\to0}\frac{f(x+h)+f(x-h)-2f(x)}{h^2}=f''(x).
$$
Show by an example that the limit may exist even if $f''(x)$ does not. Hint: Use Theorem 5.13.

### 쉬운 해설

대칭 차분을 보면 1차항이 서로 지워지고, 2차 미분 정보만 남는다. 반례는 $f'(x)$는 존재하지만 $f''(x)$는 없는 함수 중에서 대칭이 너무 좋아서 위 limit만 우연히 존재하는 경우를 찾으면 된다.

### 완전 풀이

Theorem 5.13의 표준 형태를 $x$와 $x+h$, 또 $x-h$에 적용하면 각각 어떤 $\xi_h^+\in(x,x+h)$, $\xi_h^-\in(x-h,x)$가 존재하여
$$
f(x+h)-f(x)=hf'(x)+\frac{h^2}{2}f''(\xi_h^+),
$$
$$
f(x-h)-f(x)=-hf'(x)+\frac{h^2}{2}f''(\xi_h^-).
$$
이를 더하면
$$
f(x+h)+f(x-h)-2f(x)=\frac{h^2}{2}\bigl(f''(\xi_h^+)+f''(\xi_h^-)\bigr).
$$
따라서
$$
\frac{f(x+h)+f(x-h)-2f(x)}{h^2}
=\frac12\bigl(f''(\xi_h^+)+f''(\xi_h^-)\bigr).
$$
$h\to0$이면 $\xi_h^+,\xi_h^-\to x$. 가정에 의해 $f''(x)$가 존재하므로 우변은 $f''(x)$로 간다. 따라서
$$
\lim_{h\to0}\frac{f(x+h)+f(x-h)-2f(x)}{h^2}=f''(x).
$$

이제 converse가 거짓임을 보이는 예를 들자. $x=0$,
$$
f(t)=
\begin{cases}
t^2,& t\ge0,\\
-t^2,& t<0.
\end{cases}
$$
로 두자. 그러면
$$
f'(t)=
\begin{cases}
2t,& t>0,\\
-2t,& t<0,
\end{cases}
\qquad f'(0)=0,
$$
이므로 $f'$는 0에서 differentiable하지 않다: 오른쪽 derivative는 2, 왼쪽 derivative는 -2이다. 따라서 $f''(0)$는 존재하지 않는다.

하지만 모든 $h\ne0$에 대해
$$
f(h)+f(-h)-2f(0)=h^2-h^2-0=0,
$$
따라서
$$
\frac{f(h)+f(-h)-2f(0)}{h^2}=0.
$$
그러므로 이 limit는 존재하며 값은 0이다.

### 결론

$f''(x)$가 존재하면 대칭 2차 차분 몫은 $f''(x)$로 간다. 그러나 converse는 거짓이다.

---

## Exercise 12

### 문제 원문

If $f(x)=|x|^3$, compute $f'(x), f''(x)$ for all real $x$, and show that $f^{(3)}(0)$ does not exist.

### 쉬운 해설

절댓값 때문에 좌우를 나누어 계산하면 된다. 함수는
$$
f(x)=
\begin{cases}
x^3,& x\ge0,\\
-x^3,& x<0.
\end{cases}
$$
로 쓰인다.

### 완전 풀이

$$
f(x)=|x|^3=
\begin{cases}
x^3,& x\ge0,\\
-x^3,& x<0.
\end{cases}
$$
따라서 $x\ne0$에서
$$
f'(x)=
\begin{cases}
3x^2,& x>0,\\
-3x^2,& x<0.
\end{cases}
$$
또 0에서 정의로 보면
$$
f'(0)=\lim_{h\to0}\frac{|h|^3-0}{h}=\lim_{h\to0}|h|^2\frac{|h|}{h}=0.
$$
따라서
$$
f'(x)=3x|x| 
$$
라고 쓸 수도 있다.

다시 미분하면 $x\ne0$에서
$$
f''(x)=
\begin{cases}
6x,& x>0,\\
-6x,& x<0.
\end{cases}
$$
그리고 0에서
$$
f''(0)=\lim_{h\to0}\frac{f'(h)-f'(0)}{h}
=\lim_{h\to0}\frac{3h|h|}{h}
=3|h|\to0.
$$
즉
$$
f''(x)=6|x|.
$$

이제 $f^{(3)}(0)$를 보자. $x\ne0$에서
$$
(f'')'(x)=
\begin{cases}
6,& x>0,\\
-6,& x<0.
\end{cases}
$$
따라서 0에서 좌우 미분계수가 다르다. 즉
$$
f^{(3)}(0)
$$
는 존재하지 않는다.

### 결론

$$
f'(x)=3x|x|,
\qquad
f''(x)=6|x|,
$$
그리고 $f^{(3)}(0)$는 존재하지 않는다.

---

## Exercise 22

### 문제 원문

Suppose $f$ is a real function on $(- \infty, \infty)$. Call $x$ a fixed point of $f$ if $f(x)=x$. (a) If $f$ is differentiable and $f'(t)\ne1$ for every real $t$, prove that $f$ has at most one fixed point. (b) Show that the function $f$ defined by $f(t)=t+(1+e^t)^{-1}$ has no fixed point, although $0<f'(t)<1$ for all real $t$. (c) However, if there is a constant $A<1$ such that $|f'(t)|\le A$ for all real $t$, prove that a fixed point $x$ of $f$ exists, and that $x=\lim x_n$, where $x_1$ is an arbitrary real number and $x_{n+1}=f(x_n)\qquad(n=1,2,3,\dots).$

### 쉬운 해설

고정점을 보려면 $h(x)=f(x)-x$를 보면 된다. (a)는 $h'(x)\neq0$라서 mean value theorem으로 서로 다른 두 근을 가질 수 없다는 이야기다. (c)는 contraction mapping의 1차원 버전이다.

### 완전 풀이

#### (a)

$h(x)=f(x)-x$라 두자. 그러면
$$
h'(x)=f'(x)-1.
$$
가정에 의해 모든 $x$에서 $h'(x)\ne0$이다. 만약 서로 다른 두 fixed point $x_1\ne x_2$가 있다면
$$
h(x_1)=h(x_2)=0.
$$
mean value theorem에 의해 어떤 $c$가 존재하여
$$
h'(c)=\frac{h(x_2)-h(x_1)}{x_2-x_1}=0,
$$
모순. 따라서 fixed point는 많아야 하나다.

#### (b)

$$
f(t)=t+(1+e^t)^{-1}.
$$
여기서
$$
f(t)-t=(1+e^t)^{-1}>0
$$
이므로 $f(t)=t$인 점은 없다. 즉 fixed point가 없다.

한편 미분하면
$$
f'(t)=1-\frac{e^t}{(1+e^t)^2}.
$$
분수항은 항상 양수이고 1보다 작으므로
$$
0<f'(t)<1.
$$

#### (c)

이제 $|f'(t)|\le A<1$를 가정한다. 임의의 $x_1$에서 시작하여
$$
x_{n+1}=f(x_n)
$$
로 두자.

mean value theorem으로 임의의 $u,v$에 대해 어떤 $c$가 존재하여
$$
|f(u)-f(v)|=|f'(c)||u-v|\le A|u-v|.
$$
즉 $f$는 contraction이다. 따라서
$$
|x_{n+1}-x_n|=|f(x_n)-f(x_{n-1})|\le A|x_n-x_{n-1}|\le\cdots\le A^{n-1}|x_2-x_1|.
$$
이제 $m>n$이면 triangle inequality로
$$
|x_m-x_n|
\le \sum_{k=n}^{m-1}|x_{k+1}-x_k|
\le |x_2-x_1|\sum_{k=n}^{m-1}A^{k-1}.
$$
오른쪽은 geometric tail이므로 $n\to\infty$에서 0으로 간다. 따라서 $\{x_n\}$은 Cauchy sequence이고, $\mathbb R$의 completeness에 의해 어떤 $x$로 수렴한다.

연속성 때문에
$$
f(x)=f\left(\lim x_n\right)=\lim f(x_n)=\lim x_{n+1}=x.
$$
즉 $x$는 fixed point이다.

### 결론

- $f'(t)\ne1$ everywhere이면 fixed point는 많아야 하나다.
- $f(t)=t+(1+e^t)^{-1}$는 $0<f'(t)<1$임에도 fixed point가 없다.
- 하지만 uniform contraction bound $|f'|\le A<1$가 있으면 fixed point가 존재하고 iteration이 그 점으로 수렴한다.

---

## Exercise 25

### 문제 원문

Suppose $f$ is twice differentiable on $[a,b]$, $f(a)<0$, $f(b)>0$, $f'(x)\ge \delta>0$, and $0\le f''(x)\le M$ for all $x\in[a,b]$. Let $\xi$ be the unique point in $(a,b)$ at which $f(\xi)=0$. Complete the details in the following outline of Newton’s method for computing $\xi$. (a) Choose $x_1\in(\xi,b)$, and define $\{x_n\}$ by $x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}.$ (b) Prove that $x_{n+1}<x_n$ and that $\lim x_n=\xi.$ (c) Use Taylor’s theorem to show that $x_{n+1}-\xi = \frac{f''(t_n)}{2f'(x_n)}(x_n-\xi)^2$ for some $t_n\in(\xi,x_n)$. (d) If $A=M/2\delta$, deduce that $0\le x_{n+1}-\xi\le \frac1A[A(x_1-\xi)]^{2^n}.$

### 쉬운 해설

이건 Newton method의 고전 분석이다. 핵심은 tangent line이 root의 오른쪽에서 x축을 만나는 점을 다음 iterate로 잡는다는 점, 그리고 Taylor remainder가 오차 제곱을 준다는 점이다.

### 완전 풀이

먼저 $f'(x)\ge\delta>0$이므로 $f$는 strictly increasing이고, 따라서 root $\xi$는 유일하다.

#### (a)–(b)

$x_n>\xi$라 하자. 그러면 $f(x_n)>0$이므로
$$
x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}<x_n.
$$
즉 단조감소.

또 Taylor theorem을 $x_n$에서 $\xi$로 적용하면 어떤 $t_n\in(\xi,x_n)$가 존재하여
$$
0=f(\xi)=f(x_n)+f'(x_n)(\xi-x_n)+\frac12 f''(t_n)(\xi-x_n)^2.
$$
정리하면
$$
x_n-\frac{f(x_n)}{f'(x_n)}-\xi=\frac{f''(t_n)}{2f'(x_n)}(x_n-\xi)^2\ge0.
$$
즉
$$
x_{n+1}\ge \xi.
$$
따라서 $\{x_n\}$은 $\xi$ 아래로 내려가지 않으면서 감소한다. 그러므로 어떤 $L\ge\xi$로 수렴한다.

이제 recurrence와 continuity를 사용하면
$$
L=L-\frac{f(L)}{f'(L)},
$$
즉 $f(L)=0$. root의 유일성 때문에 $L=\xi$. 따라서
$$
x_n\downarrow \xi.
$$

#### (c)

위 계산이 곧 원하는 식이다:
$$
x_{n+1}-\xi=\frac{f''(t_n)}{2f'(x_n)}(x_n-\xi)^2,
\qquad t_n\in(\xi,x_n).
$$

#### (d)

$0\le f''(t_n)\le M$, $f'(x_n)\ge\delta$이므로
$$
0\le x_{n+1}-\xi\le \frac{M}{2\delta}(x_n-\xi)^2.
$$
$A=M/(2\delta)$라 두면
$$
0\le x_{n+1}-\xi\le A(x_n-\xi)^2.
$$
이제 귀납으로 보이면
$$
0\le x_{n+1}-\xi\le \frac1A[A(x_1-\xi)]^{2^n}.
$$
실제로 $n=1$은 바로 성립하고, 귀납가정에서 한 번 더 제곱하면 된다.

### 결론

Newton iteration은 $x_n\downarrow\xi$로 수렴하며, 오차는 대략 제곱 속도로 줄어든다.

---

## Exercise 26

### 문제 원문

Suppose $f$ is differentiable on $[a,b]$, $f(a)=0$, and there is a real number $A$ such that $|f'(x)|\le A|f(x)|$ on $[a,b]$. Prove that $f(x)=0$ for all $x\in[a,b]$.

### 쉬운 해설

nonzero가 되는 첫 점이 있다고 가정하고 모순을 내면 된다. 더 구조적으로는
$$
|f'|\le A|f|
$$
는 “0에서 떠나려면 derivative도 함께 커져야 하는데, 초기에 0이므로 못 떠난다”는 부등식이다.

### 완전 풀이

모순을 위해 $f$가 항등적으로 0이 아니라고 하자. 그러면 어떤 $x_0\in[a,b]$에서 $f(x_0)\ne0$. 연속성에 의해 $|f|$는 어떤 닫힌 부분구간 $[a,c]$에서 positive maximum을 가진다. 더 직접적으로 다음을 두자:
$$
M(x)=\max_{a\le t\le x}|f(t)|.
$$
그러면 $M(a)=0$.

임의의 $x\in[a,b]$에 대해 mean value estimate로
$$
|f(x)|=|f(x)-f(a)|\le \sup_{a\le t\le x}|f'(t)|(x-a).
$$
가정에 의해
$$
|f'(t)|\le A|f(t)|\le A M(x)
\qquad(a\le t\le x),
$$
따라서
$$
|f(x)|\le A(x-a)M(x).
$$
특히 max를 취하면
$$
M(x)\le A(x-a)M(x).
$$
만약 $x$가 $a$에 충분히 가까워서 $A(x-a)<1$이면 위 부등식은
$$
M(x)=0
$$
를 강제한다. 따라서 $a$ 근처 어떤 구간에서는 $f\equiv0$.

이제
$$
S=\{x\in[a,b]: f\equiv0\text{ on }[a,x]\}
$$
를 생각하자. 위에서 $S$는 nonempty이다. $s=\sup S$라 두자. continuity 때문에 $f(s)=0$. 동일한 논리를 $[s,b]$의 시작점 $s$에 대해 다시 적용하면, $s$보다 조금 오른쪽에서도 $f\equiv0$가 되어야 한다. 이는 $s$의 maximality와 모순. 따라서 $s=b$여야 한다.

즉 $f\equiv0$ on $[a,b]$.

### 결론

주어진 미분부등식과 초기조건 $f(a)=0$ 아래에서는 반드시
$$
f(x)=0 \qquad (a\le x\le b)
$$
이다.

---

## Exercise 27

### 문제 원문

Let $\phi$ be a real function defined on a rectangle $R$ in the plane, given by $a\le x\le b,\ \alpha\le y\le \beta.$ A solution of the initial-value problem $y'=\phi(x,y),\ y(a)=c\ (\alpha\le c\le\beta)$ is, by definition, a differentiable function $f$ on $[a,b]$ such that $f(a)=c$, $\alpha\le f(x)\le\beta$, and $f'(x)=\phi(x,f(x))\ (a<x\le b).$ Prove that such a problem has at most one solution if there is a constant $A$ such that $|\phi(x,y_2)-\phi(x,y_1)|\le A|y_2-y_1|$ whenever $(x,y_1)\in R$ and $(x,y_2)\in R$.

### 쉬운 해설

두 해 $f,g$가 있다고 가정하고 차이 $h=f-g$를 본다. Lipschitz 조건이
$$
|h'(x)|\le A|h(x)|
$$
를 준다. 그리고 초기값은 같으므로 $h(a)=0$. 그러면 바로 Exercise 26을 적용할 수 있다.

### 완전 풀이

두 해 $f,g$가 있다고 가정하자. 둘 다 $[a,b]$에서 differentiable이고
$$
f(a)=g(a)=c,
\qquad
f'(x)=\phi(x,f(x)),
\qquad
g'(x)=\phi(x,g(x)).
$$

$h=f-g$라 두면 $h$는 differentiable이고
$$
h(a)=0.
$$
또한
$$
h'(x)=f'(x)-g'(x)=\phi(x,f(x))- \phi(x,g(x)).
$$
Lipschitz condition에 의해
$$
|h'(x)|
=|\phi(x,f(x))- \phi(x,g(x))|
\le A|f(x)-g(x)|
=A|h(x)|.
$$
따라서 Exercise 26의 가정을 $h$가 만족한다. 그러므로
$$
h(x)=0\qquad (a\le x\le b).
$$
즉
$$
f(x)=g(x)
\qquad (a\le x\le b).
$$
따라서 해는 많아야 하나다.

### 결론

$y$-변수에 대한 Lipschitz 조건이 있으면 initial-value problem의 해는 **uniqueness**를 가진다.
