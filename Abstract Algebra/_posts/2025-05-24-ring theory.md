---
title: "Ring Theory"
excerpt: "책 기준 4장 내용"
tags: math abstract algebra 
header:
  teaser: https://media.wiley.com/product_data/coverImage300/92/04713687/0471368792.jpg
---

# 4 Ring Theory

## 1. Definitions and Examples

지금까지 추상대수를 공부하면서, 오늘날 대수학에서 중심적 역할을 하는 하나의 추상적 체계를 소개받았다. 그것이 바로 **group**의 개념이다. **group**은 연산이 하나뿐이며, 반드시 $ab = ba$가 성립할 필요는 없다는 점에서 우리가 이전에 알고 있던 대수 체계와는 다소 다르게 느껴졌다. 우리는 일반적으로 덧셈과 곱셈이 모두 가능한 체계를 접해왔고, 곱셈에서는 $ab = ba$가 성립하는 경우가 대부분이었다. 또한, 우리가 익숙한 그러한 체계는 일반적으로 정수, 유리수, 실수, 그리고 경우에 따라서는 복소수와 같은 수들의 집합에서 유래하였다.

이번에 다룰 다음 대수적 객체는 **ring**이다. 여러 면에서, **ring**은 이전에 우리가 알고 있던 체계, 즉 수 체계와 더욱 닮아 있다. 무엇보다도 **ring**은 덧셈과 곱셈 두 가지 연산을 가지며, 이들 연산은 우리가 산술에서 알고 있는 많은 친숙한 규칙을 따른다. 그러나 **ring**은 반드시 기존의 수 체계에서 유래하지 않으며, 실제로는 그러한 경우가 드물다. 비록 산술의 형식적 규칙 중 많은 부분이 적용되지만, 그 안에서는 우리가 낯설게 여길 수 있는 특이한 현상들이 종종 발생한다. 이러한 예시들을 통해 이러한 특이점을 직접 확인해볼 수 있다.

이제 본격적으로 시작하자. 당연히 우리가 제일 먼저 해야 할 일은 우리가 논의할 대상인 **ring**을 정의하는 것이다.

---

### Definition

집합 $R$가 공집합이 아니고, 두 개의 연산 $+$와 $\cdot$이 다음의 성질을 만족하면 $R$을 **ring**이라 한다.

* (a) $a, b \in R \Rightarrow a + b \in R$
* (b) $a + b = b + a$ for $a, b \in R$
* (c) $(a + b) + c = a + (b + c)$ for $a, b, c \in R$
* (d) 어떤 원소 $0 \in R$가 존재하여 모든 $a \in R$에 대해 $a + 0 = a$
* (e) 임의의 $a \in R$에 대해 $a + b = 0$이 되는 어떤 $b \in R$가 존재한다. (이때 우리는 $b = -a$라고 쓴다.)

지금까지는 $R$이 $+$에 대해 **abelian group**이라는 사실만 말한 셈이다. 이제 곱셈 연산에 대한 규칙을 명시하자.

* (f) $a, b \in R \Rightarrow a \cdot b \in R$
* (g) $a \cdot (b \cdot c) = (a \cdot b) \cdot c$ for $a, b, c \in R$

이것이 곱셈 연산에 대해 요구하는 전부이다. 하지만 $+$와 $\cdot$는 서로 독립적으로 존재할 수 없다. 이 둘은 다음 두 개의 **분배법칙**에 의해 서로 연결된다.

* (h) $a \cdot (b + c) = a \cdot b + a \cdot c$  
  $(b + c) \cdot a = b \cdot a + c \cdot a$, for all $a, b, c \in R$

이러한 **ring**의 공리는 익숙하게 느껴질 수 있다. 실제로 **ring**이라는 개념은 정수에서 관찰되는 성질들을 일반화하여 도입된 것이다. 위에서 언급한 곱셈의 결합법칙인 공리 (g) 덕분에, 우리가 정의한 **ring**은 일반적으로 **associative ring**이라 불린다. **nonassociative ring**도 존재하고 수학에서 중요한 역할을 하기도 하지만, 본 책에서는 다루지 않는다. 따라서 여기에서 말하는 “ring”은 항상 “associative ring”을 의미한다.

공리 (a)부터 (h)까지는 익숙하지만, 이 공리들에 포함되어 있지 않은 규칙들도 있다. 우리가 익히 알고 있는 규칙들 중 몇 가지가 일반적인 **ring**에서는 성립하지 않는다.

첫째, 모든 $a \in R$에 대해 $a \cdot 1 = 1 \cdot a = a$를 만족하는 **단위원** $1 \in R$의 존재를 우리는 가정하지 않았다. 우리가 접할 예제들 중 많은 경우에는 그러한 단위원이 존재하며, 이 경우 우리는 $R$이 **ring with unit**이라고 한다. 일부 대수학자들은 모든 **ring**에 단위원이 존재해야 한다고 주장하기도 한다. 단, 우리는 $1 \neq 0$이어야 한다는 점을 명시한다. 즉, 원소가 $0$ 하나뿐인 집합은 단위원을 가지는 **ring**이 아니다.

둘째, 이전의 수 체계에서는 $a \cdot b = 0$이면 $a = 0$ 또는 $b = 0$이라 결론지었다. 그러나 일반적인 **ring**에서는 반드시 그런 결론이 나오지 않는다. 이러한 성질이 성립하는 **ring**은 특별히 좋은 성질을 가지며, **domain**이라 부른다.

셋째, 곱셈의 교환법칙 $a \cdot b = b \cdot a$는 **ring**의 공리로 요구되지 않았다. 실제로 이 성질을 만족하지 않는 **noncommutative ring**도 존재하며, 이후에 그런 예시를 보게 될 것이다. 비록 이 장에서는 주로 **commutative ring**을 다루겠지만, 초반의 여러 정리에서는 이러한 교환법칙을 가정하지 않고 논의를 전개한다.

우리는 위에서 언급했듯, 어떤 성질을 가진 **ring**들이 특히 좋은 구조를 갖는 경우가 있어 특별한 이름을 부여한다. 그 예시들을 빠르게 살펴보자.

---

### Definition

**commutative ring** $R$에서 $a \cdot b = 0$이면 $a = 0$ 또는 $b = 0$이 성립할 때, $R$을 **integral domain**이라 한다.

일부 대수학 책에서는 **integral domain**이 반드시 단위원을 포함해야 한다고 요구하기도 한다. 다른 책을 읽을 때는 이 점을 확인할 필요가 있다. 정수의 집합 $\mathbb{Z}$는 자명한 **integral domain**의 예시를 제공한다. 이후에 이보다 덜 자명한 예시들도 살펴보게 될 것이다.

---

### Definition

단위원을 갖는 **ring** $R$에서 $a \neq 0$인 모든 $a \in R$에 대해 $a \cdot a^{-1} = a^{-1} \cdot a = 1$이 되는 어떤 $a^{-1} \in R$이 존재하면 $R$을 **division ring**이라 한다.

이러한 **ring**을 **division ring**이라 부르는 이유는 명확하다. 나눗셈이 가능한 구조를 의미하기 때문이다 (비록 좌우 구분을 명시해야 할 수도 있지만). 비가환적인 **division ring**도 상당히 자주 등장하며, **noncommutative algebra**에서 중요한 역할을 한다. 다만 그 구조가 복잡하여, 본 책에서는 이러한 예시 중 고전적인 하나만 소개한다. 그것은 해밀턴이 1843년에 소개한 고전적인 예시인 **quaternions**이다. (Example 13 참조)

---

### Definition

**ring** $R$가 **commutative division ring**일 때, $R$을 **field**라 한다.

즉, **field**는 $0$이 아닌 모든 원소에 대해 나눗셈이 가능한 **commutative ring**이다. 다시 말하면, $R$의 $0$이 아닌 원소들이 곱셈에 대해 **abelian group**을 이루면 $R$은 **field**이다.

---

### Examples

#### Example 1

첫 번째 예시로 가장 자연스럽게 선택할 수 있는 **ring**은 정수의 집합 $\mathbb{Z}$이다. 이는 정수의 일반적인 덧셈과 곱셈 아래에서 **integral domain**의 예시가 된다.


#### Example 2

두 번째 예시는 마찬가지로 자명하다. $\mathbb{Q}$를 유리수 전체의 집합이라 하자. 우리가 잘 알다시피, $\mathbb{Q}$는 **field**의 모든 공리를 만족하므로, $\mathbb{Q}$는 **field**이다.


#### Example 3
실수 $\mathbb{R}$ 역시 **field**의 예이다.


#### Example 4
복소수 $\mathbb{C}$도 역시 **field**를 이룬다.

여기서 $\mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$임을 주목하라. 우리는 이를 두고 $\mathbb{Q}$가 $\mathbb{R}$ (및 $\mathbb{C}$)의 **subfield**라고 말한다.


#### Example 5
$R = \mathbb{Z}_6$이라 하자. 즉, 정수의 모듈로 6 연산 아래의 집합이며, 그 덧셈과 곱셈은 다음과 같이 정의된다:

$$
[a] + [b] = [a + b], \quad [a][b] = [ab]
$$

여기서 $[0]$은 **ring**의 0 원소이며, $[1]$은 단위원이다. 하지만 $\mathbb{Z}_6$는 **integral domain**이 아니다. 왜냐하면

$$
[2][3] = [6] = [0]
$$

이면서도 $[2] \ne [0]$, $[3] \ne [0]$이기 때문이다. 즉, $R$은 **unit**을 갖는 **commutative ring**이지만, **integral domain**은 아니다.

이 예시는 다음 정의를 유도한다.

---

### Definition

**ring** $R$에서 $a \ne 0$이고 어떤 $b \ne 0 \in R$에 대해 $ab = 0$일 때, $a$를 **zero-divisor**라 한다.

사실, 우리는 위에서 정의한 것을 엄밀히 말하면 **left zero-divisor**라 불러야 하지만, 대부분 **commutative ring**만을 다룰 예정이므로 좌우의 구분은 생략한다.

$\mathbb{Z}_6$에서 $[2]$와 $[3]$은 모두 **zero-divisor**임을 주목하라. **integral domain**이란 결국 **zero-divisor**가 존재하지 않는 **commutative ring**을 뜻한다.


#### Example 6

$R = \mathbb{Z}_5$라고 하자. 즉, 5를 법으로 하는 정수들의 **ring**이다. 이는 단위원을 갖는 **commutative ring**이며, 더 나아가 **field**이다. $[1], [2], [3], [4]$는 모두 0이 아닌 원소이며, $[2][3] = [6] = [1]$, 그리고 $[1]$, $[4]$는 자기 자신에 대한 역원을 가진다. 따라서 $\mathbb{Z}_5$의 모든 0이 아닌 원소가 역원을 가지므로, 이는 **field**이다.

이를 일반화하면 다음과 같다.


#### Example 7

$\mathbb{Z}_p$, 즉 $p$가 소수일 때의 정수의 모듈로 $p$ **ring**을 생각하자. 이 역시 단위원을 갖는 **commutative ring**임이 자명하다. 우리는 $\mathbb{Z}_p$가 **field**임을 주장한다.

이를 보이기 위해 $[a] \ne [0]$이라고 하자. 그렇다면 $p \nmid a$이고, **Fermat's Theorem**에 의해:

$$
a^{p-1} \equiv 1 \pmod{p}
$$

따라서 $[a^{p-1}] = [1]$이 되고, $[a]^{p-1} = [1]$이므로 $[a]^{p-2}$는 $[a]$의 역원이다. 그러므로 $\mathbb{Z}_p$는 **field**이다.

이처럼 유한한 원소 개수를 가진 **field**를 **finite field**라 부른다. 우리는 나중에 $\mathbb{Z}_p$와는 다른 형태의 **finite field**도 구성하게 될 것이다.


#### Example 8

$\mathbb{Q}$의 원소 중, 기약형으로 표현했을 때 분모가 홀수인 모든 유리수의 집합 $R$을 생각하자. $R$은 $\mathbb{Q}$에서의 일반적인 덧셈과 곱셈 아래에서 **ring**을 이룬다. 이는 단위원을 갖는 **integral domain**이지만 **field**는 아니다. 왜냐하면 2의 역원인 $\frac{1}{2}$는 분모가 짝수이므로 $R$에 속하지 않기 때문이다.

그렇다면 $R$의 어떤 원소가 $R$ 내에서 역원을 가지는가?


#### Example 9

이번에는 $\mathbb{Q}$의 원소 중, 기약형으로 썼을 때 분모가 특정 소수 $p$로 나누어지지 않는 모든 유리수의 집합 $R$을 생각하자. 위와 마찬가지로 $R$은 일반적인 덧셈과 곱셈 아래에서 **ring**을 이루며, 단위원을 가지는 **integral domain**이지만 **field**는 아니다.

$R$의 어떤 원소가 역원을 가지는가?

위의 예제 8번과 9번은 다음 정의를 뒷받침한다.

---

### Definition

**ring** $R$가 주어졌을 때, $S \subset R$이 다음 조건을 만족하면 $S$는 $R$의 **subring**이라 한다:

* $S$는 공집합이 아니며
* 임의의 $a, b \in S$에 대해 $ab, a \pm b \in S$

(증명해보라!)

우리는 **commutative ring**의 또 다른 예제를 소개한다. 이번에는 **미적분학**에서 유래한 것이다.


#### Example 10
$R$을 $[0,1]$ 구간에서 정의된 실수값 **연속 함수** 전체의 집합이라 하자. $f, g \in R$, $x \in [0,1]$에 대해

$$
(f + g)(x) = f(x) + g(x)
$$

$$ 
\quad (f \cdot g)(x) = f(x)g(x)
$$

로 연산을 정의하자. 미적분학의 결과에 따라 $f + g$, $f \cdot g$ 역시 연속함수이므로, 이 연산 아래에서 $R$은 **commutative ring**이다.

그러나 이는 **integral domain**이 아니다. 예를 들어,

* $f(x) = -x + \frac{1}{2}$ (단, $0 \le x \le \frac{1}{2}$), 그 외에는 0
* $g(x) = 2x - 1$ (단, $\frac{1}{2} < x \le 1$), 그 외에는 0

이라 하면, $f \cdot g = 0$임에도 불구하고 $f, g \ne 0$이다.

이 **ring**은 단위원을 가지며, 이는 모든 $x \in [0,1]$에 대해 $e(x) = 1$로 정의되는 함수 $e$이다.

그렇다면 $R$의 어떤 원소가 자기 자신의 역원을 가지는가?

---

우리는 이제 **noncommutative**한 예시들을 살펴보고자 한다. 이러한 예시들은 풍부하게 존재하지만, 독자가 선형대수학에 익숙하다는 전제를 하지 않기 때문에 그리 쉽게 찾을 수는 없다. 가장 쉽고 자연스러운 출발점은 **field** 위의 행렬이다. 따라서 우리의 첫 **noncommutative** 예시는 실수 계수의 $2 \times 2$ 행렬 집합이 될 것이다.

---

#### Example 11

$F$를 실수의 **field**라 하자. 그리고 $R$을 다음과 같은 모든 정사각 배열의 집합이라 하자:

$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}, \quad \text{단 } a, b, c, d \in \mathbb{R}
$$

이러한 배열에 대해 덧셈은 자연스럽게 다음과 같이 정의된다:

$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
+
\begin{pmatrix}
r & s \\
t & u
\end{pmatrix}
=
\begin{pmatrix}
a + r & b + s \\
c + t & d + u
\end{pmatrix}
$$

이 연산 하에서 $R$은 덧셈에 대해 **abelian group**을 이루며, 영원소는

$$
\begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix}
$$

이고, 음원소는 각 성분의 부호를 반대한 행렬이다.

**ring** 구조를 갖추기 위해서는 곱셈 연산이 필요하다. 우리는 다음과 같이 정의한다:

$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
\begin{pmatrix}
r & s \\
t & u
\end{pmatrix}
=
\begin{pmatrix}
ar + bt & as + bu \\
cr + dt & cs + du
\end{pmatrix}
$$

이 곱셈 연산이 다소 인위적으로 보일 수 있지만, 이 연산과 위 덧셈 연산을 함께 사용할 경우 $R$은 **noncommutative ring**이 된다. 이때,

$$
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

은 단위원으로 작용한다.

한 가지 흥미로운 점은 다음과 같다:

$$
\begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix}
=
\begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix}
$$

이므로 이는 자명하지 않은 원소인데도 제곱하면 0이 된다. 즉, **zero-divisor**이다.

이 $R$은 실수 **field** $F$ 위의 모든 $2 \times 2$ 행렬로 구성된 **ring**이다.

이러한 행렬 곱셈에 익숙하지 않은 독자를 위해, 이 곱셈이 어떻게 작동하는지 설명하자.

* 곱의 왼쪽 위 항목은 A의 첫 번째 행과 B의 첫 번째 열을 "곱하여" 계산한다.
* 오른쪽 위 항목은 A의 첫 번째 행과 B의 두 번째 열
* 왼쪽 아래는 A의 두 번째 행과 B의 첫 번째 열
* 오른쪽 아래는 A의 두 번째 행과 B의 두 번째 열

예를 들어 다음과 같은 두 행렬을 곱해보자:

$$
A =
\begin{pmatrix}
1 & \pi \\
-3 & 2
\end{pmatrix},
\quad
B =
\begin{pmatrix}
\frac{1}{2} & \frac{1}{2} \\
1 & \pi
\end{pmatrix}
$$

그러면

* 왼쪽 위 항목: $1 \cdot \frac{1}{2} + \pi \cdot 1 = \frac{1}{2} + \pi$
* 오른쪽 위: $1 \cdot \frac{1}{2} + \pi \cdot \pi = \frac{1}{2} + \pi^2$
* 왼쪽 아래: $-3 \cdot \frac{1}{2} + 2 \cdot 1 = -\frac{3}{2} + 2 = \frac{1}{2}$
* 오른쪽 아래: $-3 \cdot \frac{1}{2} + 2 \cdot \pi = -\frac{3}{2} + 2\pi$

이렇게 행렬곱이 정의된다.

---

#### Example 12

임의의 **ring** $R$에 대해, 다음과 같은 형태의 행렬 집합을 생각하자:

$$
S = \left\{
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
\mid a, b, c, d \in R
\right\}
$$

덧셈과 곱셈은 Example 11과 동일하게 정의한다. 이 경우에도 $S$는 **ring**이 되며, 이는 $R$ 위의 모든 $2 \times 2$ 행렬로 구성된 **ring**이다.

---

#### Example 13 — The Quaternions

고전적인 예시 중 하나인 실수 **quaternion**을 보자. 이는 해밀턴이 복소수의 **noncommutative**한 확장을 목표로 1843년에 도입하였다.

실수 **field** $\mathbb{R}$에 대해, 다음과 같은 형식의 기호를 가진 집합을 정의한다:

$$
a_0 + a_1 i + a_2 j + a_3 k \quad \text{단 } a_0, a_1, a_2, a_3 \in \mathbb{R}
$$

이들 사이의 등식과 덧셈은 다음과 같이 정의된다:

* 등식: 두 quaternion이 같으려면, 대응하는 모든 계수가 같아야 한다.
* 덧셈: $(a_0 + a_1 i + a_2 j + a_3 k)$ $+ (b_0 + b_1 i + b_2 j + b_3 k)$ $= (a_0 + b_0) + (a_1 + b_1)i$ $+ (a_2 + b_2)j + (a_3 + b_3)k$

이제 곱셈 규칙을 소개한다. 해밀턴은 1843년 10월 6일 더블린의 브루엄 다리(Brougham Bridge)에서 이를 발견하고 다리에 새겨넣었다. 기본 규칙은 다음과 같다:

$$
i^2 = j^2 = k^2 = -1, \quad ij = k, \quad jk = i, \quad ki = j
$$

$$
ji = -k, \quad kj = -i, \quad ik = -j
$$

이들 규칙을 기반으로, 다음과 같이 두 quaternion의 곱을 정의한다: $(a_0 + a_1 i + a_2 j + a_3 k)$ $(b_0 + b_1 i + b_2 j + b_3 k)$ $= c_0 + c_1 i + c_2 j + c_3 k$

여기서

$$
\begin{aligned}
c_0 &= a_0 b_0 - a_1 b_1 - a_2 b_2 - a_3 b_3 \\
c_1 &= a_0 b_1 + a_1 b_0 + a_2 b_3 - a_3 b_2 \\
c_2 &= a_0 b_2 - a_1 b_3 + a_2 b_0 + a_3 b_1 \\
c_3 &= a_0 b_3 + a_1 b_2 - a_2 b_1 + a_3 b_0
\end{aligned}
$$

계산은 복잡해 보이지만, 이 모든 것은 분배법칙과 위의 곱셈 규칙을 반복 적용함으로써 얻어진다.

만약 $x = a_0 + a_1 i + a_2 j + a_3 k \ne 0$이라면, 다음 항등식이 성립한다:

$$
x \cdot \bar{x} = a_0^2 + a_1^2 + a_2^2 + a_3^2
$$

이 값이 $\ne 0$이므로, 역원이 존재함을 보여준다. 따라서 quaternion의 집합은 단위원을 갖는 **noncommutative division ring**이다.

이 **quaternion**은 종종 수학자들이 접하는 유일한 **noncommutative division ring**이기도 하다.

---

## 2. Some Simple Results

우리는 이제 여러 **ring** 예시를 살펴보았고, 이를 직접 다뤄보기도 했다. 따라서 이제는 계산에서 자주 발생할 수 있는 번거로운 사소한 오류들을 피할 수 있도록 몇 가지 계산 규칙들을 정리하는 것이 바람직하다.

이 단원에서 증명할 결과들은 특별히 놀랍지도, 흥미롭지도, 흥분되지도 않는 것들이다. 그러나 알파벳을 처음 배울 때와 마찬가지로, 더 크고 훌륭한 것을 배우기 위해서는 반드시 거쳐야 하는 기본 요소들이다.

**ring** $R$은 적어도 덧셈에 대해 **abelian group**이므로, **group theory**에서 다음과 같은 사실들을 알고 있다:

* $-(-a) = a$
* $-(a + b) = (-a) + (-b)$
* $a + b = a + c \Rightarrow b = c$

등이 성립한다.

---

### Lemma 4.2.1

**임의의 ring $R$, 그리고 $a, b \in R$**에 대해 다음이 성립한다:

* (a) $a \cdot 0 = 0 \cdot a = 0$
* (b) $a \cdot (-b) = (-a) \cdot b = -(ab)$
* (c) $(-a)(-b) = ab$
* (d) $1 \in R$일 때, $(-1) \cdot a = -a$

**Proof.** 각 항목을 차례대로 증명한다:

(a) $0 = 0 + 0$이므로,

$$
a \cdot 0 
= a \cdot (0 + 0) 
= a \cdot 0 + a \cdot 0
$$

양변에서 $a \cdot 0$을 소거하면 $a \cdot 0 = 0$.
같은 방식으로 $0 \cdot a = 0$도 오른쪽 분배법칙을 이용해 증명할 수 있다.

---

(b) $ab + a(-b) = a(b + (-b)) = a \cdot 0 = 0$이므로,

$$
a(-b) = -(ab)
$$

같은 방식으로 $(-a)b = -(ab)$.

---

(c) 위 결과로부터,

$$
(-a)(-b) 
= -((-a) \cdot b) 
= -(-(ab)) 
= ab
$$

왜냐하면 우리는 $R$에서 덧셈이 **abelian group**이므로 부호가 두 번 적용되면 원래 값으로 돌아온다.

---

(d) $(-1)a + a = (-1 + 1)a = 0 \cdot a = 0$, 따라서 정의에 따라 $(-1)a = -a$. □

---

### Lemma 4.2.2

**임의의 ring $R$, 그리고 $a, b \in R$**에 대해 다음이 성립한다:

$$
(a + b)^2 = a^2 + b^2 + ab + ba
$$

**Proof.** 이는 정수에서의 항등식 $(a + b)^2 = a^2 + 2ab + b^2$의 일반화이다. 단, **ring** $R$이 비가환일 수 있으므로 $ab \ne ba$일 수 있다.

오른쪽 분배법칙을 이용하면:

$$
(a + b)^2 
= (a + b)(a + b) 
= (a + b)a + (a + b)b
$$

왼쪽 분배법칙을 다시 적용하면:

$$
= a^2 + ba + ab + b^2
$$

즉,

$$
= a^2 + b^2 + ab + ba
$$

□

---

이제 $(a + b)^3$의 비가환 버전을 직접 시도해 보라. (힌트: $(a + b)^3 = (a + b)(a + b)^2$)

---

다음은 흥미로운 결과이다. 어떤 **ring** $R$이 단위원을 가질 경우, 두 개의 분배법칙만으로도 덧셈의 교환법칙이 유도될 수 있다.

---

### Lemma 4.2.3

**단위원을 갖는 $R$**가 있고, 이 $R$이 **ring**의 모든 공리를 만족하지만 **덧셈의 교환법칙** $a + b = b + a$는 보장되지 않는다고 하자. 이 경우에도 $R$은 **ring**이다. (즉, $a + b = b + a$가 성립한다.)

**Proof.** 우리는 $a + b = b + a$임을 보여야 한다.

단위원 $1 \in R$이 존재하므로, 오른쪽 분배법칙을 적용하면:

$$
(a + b)(1 + 1) 
= (a + b)1 + (a + b)1 
= a + b + a + b
$$

왼쪽 분배법칙을 적용하면:

$$
= a(1 + 1) + b(1 + 1) 
= a + a + b + b
$$

따라서

$$
a + b + a + b = a + a + b + b
$$

양변에서 $a$를 왼쪽에서, $b$를 오른쪽에서 각각 소거하면 $b + a = a + b$가 된다. 그러므로 덧셈은 교환법칙을 만족하므로 $R$은 **ring**이다. □

---

마지막으로 보다 흥미로운 결과를 소개한다. **Boolean ring**이라는 개념은 다음과 같다.

---

### Definition

모든 원소 $x \in R$에 대해 $x^2 = x$를 만족하는 **ring** $R$을 **Boolean ring**이라 한다.

---

### Lemma 4.2.4

모든 **Boolean ring**은 **commutative**하다.

**Proof.** $x, y \in R$가 주어졌다고 하자. $R$은 **Boolean ring**이므로,

$$
x^2 = x, \quad y^2 = y, \quad (x + y)^2 = x + y
$$

한편 Lemma 4.2.2에 의해:

$$
(x + y)^2 = x^2 + y^2 + xy + yx
= x + y + xy + yx
$$

따라서

$$
x + y + xy + yx = x + y \Rightarrow xy + yx = 0
$$

양변에 $x$를 곱하면:

$$
x(xy + yx) = x^2 y + xyx = xy + xyx = 0
$$

또한:

$$
(xy + yx)x = xyx + yx^2 = xyx + yx = 0
$$

이 두 식을 비교하면:

$$
xy + xyx = xyx + yx \Rightarrow xy = yx
$$

따라서 $R$은 **commutative ring**이다. □

---

## 3. Ideals, Homomorphisms, and Quotient Rings

**group**을 공부하면서 우리는 **homomorphism**과 그 **kernel**, 즉 **normal subgroup**이 중심적인 역할을 한다는 것을 보았다. 이는 **ring**에서도 마찬가지일 것으로 예상할 수 있다. 실제로, **homomorphism**과 **normal subgroup**에 해당하는 개념은 **ring** 이론에서도 중요한 역할을 한다.

우리가 이미 **group theory**를 통해 그러한 개념에 대한 기초를 쌓았기 때문에, **ring**에서의 평행적인 전개는 비교적 간단하고 빠르게 진행될 것이다.

---

### Definition

**ring** $R$에서 $R'$로 가는 사상 $\varphi : R \to R'$가 다음 조건을 만족하면, 이를 **homomorphism**이라 한다:

* (a) $\varphi(a + b) = \varphi(a) + \varphi(b)$
* (b) $\varphi(ab) = \varphi(a)\varphi(b)$
  for all $a, b \in R$

**ring**은 두 개의 연산을 가지므로, 두 연산 모두가 보존되는 것이 당연하고 정당하다. 또한, 조건 (a)는 $R$을 단순히 $+$ 연산 아래에서의 **abelian group**으로 보았을 때의 **group homomorphism**이라는 의미이므로, 이 사실만으로도 몇 가지 결과들을 유도할 수 있다.

**group**에서와 마찬가지로, $\varphi : R \to R'$가 **homomorphism**일 때 $\varphi(R)$는 $R'$의 **subring**이다. (증명해보라!)

이제 $\varphi : R \to R'$가 **homomorphism**일 때, 다음과 같이 정의하자:

$$
\ker \varphi = \{ x \in R \mid \varphi(x) = 0 \}
$$

여기서 0은 $R'$의 영원소이다. **group theory**로부터 $\ker \varphi$는 $R$의 **additive subgroup**이라는 것을 알 수 있다. 그러나 이보다 더 많은 성질을 가진다.
만약 $k \in \ker \varphi$, $r \in R$이면:

$$
\varphi(kr) = \varphi(k)\varphi(r) = 0 \cdot \varphi(r) = 0
$$

$$
\varphi(rk) = \varphi(r)\varphi(k) = \varphi(r) \cdot 0 = 0
$$

따라서 $kr \in \ker \varphi$, $rk \in \ker \varphi$이다. 즉, $\ker \varphi$는 임의의 원소에 대한 곱을 좌우 양쪽에서 흡수한다.

이러한 성질을 일반화하면, **ring** 이론에서의 **normal subgroup**에 해당하는 개념을 다음과 같이 정의할 수 있다.

---

### Definition

**ring** $R$에서 공집합이 아닌 부분집합 $I \subset R$가 다음 두 조건을 만족하면, 이를 $R$의 **ideal**이라 한다:

* (a) $I$는 $R$의 덧셈에 대한 **subgroup**이다.
* (b) 임의의 $r \in R$, $a \in I$에 대해 $ra \in I$, $ar \in I$

곧 **homomorphism**과 **ideal**의 예시들을 살펴보게 될 것이다.
그러나 먼저 위 정의의 조건 (b)가 사실상 좌우 두 가지 조건으로 나뉜다는 점을 언급해두자.

만약 어떤 집합 $L \subset R$이 $R$의 **additive subgroup**이고, 임의의 $r \in R$, $a \in L$에 대해 $ra \in L$이면, $L$을 **left ideal**이라 한다. 반대로 $ar \in L$만 만족하면 **right ideal**이다.

우리가 앞서 정의한 **ideal**은 좌우 양쪽 조건을 모두 만족하므로, 이를 정확히는 **two-sided ideal**이라 부른다. 비가환 **ring** 이론에서는 이러한 용어 구분이 중요하지만, 본 장에서는 특별히 언급하지 않는 한 “ideal”이라 하면 **two-sided ideal**을 의미한다.

---

위에서 $\ker \varphi$에 대해 한 논의를 다음과 같이 정리할 수 있다.

### Lemma 4.3.1

$\varphi : R \to R'$가 **homomorphism**이면, $\ker \varphi$는 $R$의 **ideal**이다.

---

우리는 곧 모든 **ideal**이 어떤 **homomorphism**의 **kernel**로 표현될 수 있음을 보게 된다. 이는 마치 모든 **normal subgroup**이 어떤 **homomorphism**의 **kernel**이 되는 것과 같다.

---

이제 $K$를 $R$의 **ideal**이라 하자. $K$는 덧셈에 대해 **subgroup**이므로, **quotient group** $R/K$는 존재한다. 이는 $R$의 모든 **coset** $a + K$의 집합이다.

그러나 $R$은 단순한 **group**이 아니라 **ring**이며, $K$ 또한 단순한 **subgroup**이 아닌 $R$의 **ideal**이다. 따라서 우리는 $R/K$에 **ring** 구조를 부여할 수 있어야 한다.

자연스러운 곱셈 정의는 다음과 같다:

$$
(a + K)(b + K) = ab + K
$$

이 곱셈이 **well-defined**임을 보여야 한다. 즉,

$$
a + K = a' + K,\quad b + K = b' + K 
$$

$$
\Rightarrow ab + K = a'b' + K
$$

이 성립함을 보여야 한다. $a - a' \in K$, $b - b' \in K$이므로,

$$
ab - a'b = (a - a')b \in K
$$

$$
a'b - a'b' = a'(b - b') \in K
$$

$$
\Rightarrow ab - a'b' \in K
$$

따라서 $ab + K = a'b' + K$, 즉 곱셈이 **well-defined**하다.

---

이제 $R/K$에는 덧셈과 곱셈이 정의되며, **ring**이 된다. 그리고 사상

$$
\varphi : R \to R/K,\quad \varphi(a) = a + K
$$

는 $R$에서 $R/K$로의 **homomorphism**이며, 그 **kernel**은 $K$이다.

---

### Theorem 4.3.2

$K$가 $R$의 **ideal**이면, **quotient group** $R/K$는 곱셈

$$
(a + K)(b + K) = ab + K
$$

을 통해 **ring**이 된다. 또한, 사상

$$
\varphi : R \to R/K,\quad \varphi(a) = a + K
$$

는 $R$에서 $R/K$로의 **homomorphism**이며, **kernel**은 $K$이다. 따라서 $R/K$는 $R$의 **homomorphic image**이다.

---

**group** 이론에서처럼, $\varphi$가 **injective**이면 $\ker \varphi = \{0\}$이다.
이와 같이, **injective homomorphism**을 **monomorphism**, **bijective**한 경우를 **isomorphism**이라 하며, $R$과 $R'$이 **isomorphic**이면 구조적으로 동일하다고 본다.

$R$에서 자기 자신으로 가는 **isomorphism**은 **automorphism**이라 하며, 예를 들어 $R = \mathbb{C}$일 때, 복소수 켤레 사상은 $\mathbb{C}$의 **automorphism**이다. (증명해보라!)

---

이제 누가 봐도 회의적인 사람이 아닌 이상, Chapter 2의 Section 7에서 증명한 **homomorphism** 정리가 **ring**의 경우에도 성립하지 않을 것이라 기대하지는 않을 것이다. 실제로 이 정리들은 이 맥락에서도 그대로 성립하며, 단지 약간의 적응만으로도 그 증명을 동일하게 수행할 수 있다. 여기서는 이 정리들을 아무런 추가 논의 없이 명시하고, 증명에 필요한 세부적인 사항들은 독자에게 맡긴다.

---

### Theorem 4.3.3 (First Homomorphism Theorem)

사상 $\varphi : R \to R'$가 $R$에서 $R'$로의 **homomorphism**이며 $\ker \varphi = K$라 하자. 그렇다면:

$$
R' \cong R/K
$$

즉, 사상 $\psi : R/K \to R'$를 다음과 같이 정의하면

$$
\psi(a + K) = \varphi(a)
$$

이는 $R/K$에서 $R'$로의 **isomorphism**을 정의한다.

---

### Theorem 4.3.4 (Correspondence Theorem)

$\varphi : R \to R'$가 **homomorphism**이고 $\ker \varphi = K$라 하자.
$I' \subset R'$가 **ideal**이면,

$$
I = \{ a \in R \mid \varphi(a) \in I' \}
$$

는 $R$의 **ideal**이며, $I \supset K$, 그리고

$$
I/K \cong I'
$$

이러한 대응은 $R'$의 모든 **ideal**들과 $R$의 $K \supset$인 모든 **ideal**들 사이의 1-1 대응을 제공한다.

---

### Theorem 4.3.5 (Second Homomorphism Theorem)

$A \subset R$가 $R$의 **subring**, $I \subset R$가 $R$의 **ideal**일 때,

$$
A + I = \{ a + i \mid a \in A, i \in I \}
$$

는 $R$의 **subring**이고, $I$는 $A + I$의 **ideal**이다. 또한,

$$
(A + I)/I \cong A/(A \cap I)
$$

---

### Theorem 4.3.6 (Third Homomorphism Theorem)

$\varphi : R \to R'$가 **homomorphism**, $\ker \varphi = K$라고 하자.
$I' \subset R'$가 **ideal**이고,

$$
I = \{ a \in R \mid \varphi(a) \in I' \}
$$

라 하면,

$$
R/I \cong R'/I'
$$

즉, $K \subset I$가 $R$의 **ideal**이면,

$$
R/I \cong (R/K)/(I/K)
$$

---

이제 이 섹션을 마무리하며, 앞서 논의한 개념들이 실제로 어떻게 작동하는지 예제를 통해 살펴보자.

---

### Examples

#### Example 1
 $\mathbb{Z}$, 즉 정수의 **ring**을 고려하자. 정수 $n > 1$에 대해 $I_n = \{ kn \mid k \in \mathbb{Z} \}$는 $\mathbb{Z}$의 **ideal**이다.
   $\mathbb{Z}_n$은 모듈로 $n$의 정수 **ring**이고, 사상

$$
\varphi : \mathbb{Z} \to \mathbb{Z}_n,\quad \varphi(a) = [a]
$$

는 $\ker \varphi = I_n$을 가지는 **homomorphism**이다. 따라서 Theorem 4.3.3에 의해:

$$
\mathbb{Z}_n \cong \mathbb{Z}/I_n
$$

이 결과는 전혀 놀랍지 않다. 왜냐하면 이것이 바로 우리가 $\mathbb{Z}_n$을 처음 정의할 때의 방식이었기 때문이다.

---


#### Example 2

$F$를 **field**라 하자. $F$의 **ideal**들은 무엇일까?
$I \ne (0)$이 $F$의 **ideal**이라 하자. $a \ne 0 \in I$라면,
$a^{-1}a = 1 \in I$, 그리고 $r \cdot 1 = r \in I$이므로, 결국 $I = F$가 된다.
따라서 **field**의 **ideal**은 오직 $(0)$과 $F$뿐이다.

---


#### Example 3
$R$을 기약형으로 나타냈을 때 분모가 홀수인 유리수 전체의 **ring**이라 하자.
$I$를 기약형에서 분자가 짝수인 유리수들의 집합이라 하면, 이는 $R$의 **ideal**이다.
다음 사상을 정의하자:

$$
\varphi : R \to \mathbb{Z}_2,\quad \varphi(a/b) =
\begin{cases}
0, & \text{if } a \text{ is even} \\
1, & \text{if } a \text{ is odd}
\end{cases}
$$

이는 $R$에서 $\mathbb{Z}_2$로의 **homomorphism**이며 $\ker \varphi = I$이다.
따라서

$$
R/I \cong \mathbb{Z}_2
$$

가 된다.

---


#### Example 4
$R$을 기약형에서 분모가 고정된 소수 $p$로 나누어지지 않는 유리수들의 집합이라 하자.
$I$를 기약형에서 분자가 $p$로 나누어지는 유리수들의 집합이라 하면, $I$는 $R$의 **ideal**이고,

$$
R/I \cong \mathbb{Z}_p
$$

(증명해보라!)

---


#### Example 5
$R$을 닫힌 구간 $[0,1]$에서 정의되는 실수값 연속함수들의 집합이라 하자.
$f, g \in R$, $x \in [0,1]$일 때,

$$
(f + g)(x) = f(x) + g(x), \quad (fg)(x) = f(x)g(x)
$$

이라 정의된다. 이제

$$
I = \{ f \in R \mid f(\tfrac{1}{2}) = 0 \}
$$

이라 하자. $I$는 $R$의 **ideal**이다.
모든 $f \in R$에 대해 다음과 같이 쓸 수 있다:

$$
f(x) = (f(x) - f(\tfrac{1}{2})) + f(\tfrac{1}{2}) = g(x) + f(\tfrac{1}{2})
$$

여기서 $g(x) = f(x) - f(\tfrac{1}{2}) \in I$이므로,

$$
f + I = f(\tfrac{1}{2}) + I
$$

따라서 $R/I$는 실수 $a \in \mathbb{R}$에 대해 $a + I$ 형태의 **coset**들로 구성된다.
각 $a \in \mathbb{R}$에 대해 $f \in R$로 $f(\tfrac{1}{2}) = \beta$라 하면,

$$
a\beta^{-1}f + I = a + I
$$

이므로 모든 실수 $a$가 등장한다. 즉,

$$
R/I \cong \mathbb{R}
$$

그리고 $\varphi : R \to \mathbb{R},\quad \varphi(f) = f(\tfrac{1}{2})$는
**surjective homomorphism**이며 $\ker \varphi = I$이므로,
Theorem 4.3.3에 의해 $R/I \cong \mathbb{R}$.

---


#### Example 6
$R$을 정수 계수의 quaternion이라 하자. 즉,

$$
R = \{ a_0 + a_1 i + a_2 j + a_3 k \mid a_0, a_1, a_2, a_3 \in \mathbb{Z} \}
$$

로 정의한다. 고정된 소수 $p$에 대해, $I_p$를 적절히 정의하면 $I_p$는 $R$의 **ideal**이며,

$$
R/I_p \cong H(\mathbb{Z}_p)
$$

여기서 $H(\mathbb{Z}_p)$는 $\mathbb{Z}_p$ 위에서 정의된 quaternion ring이다.
(자세한 사항은 Section 1의 문제 36과 그 앞의 단락을 참조.)

---


#### Example 7
$R$이 다음과 같다고 하자.
$$
R = \left\{ \begin{pmatrix} a & b \\ 0 & a \end{pmatrix} \mid a, b \in \mathbb{R} \right\}
$$

   이는 $\mathbb{R}$ 위 $2 \times 2$ 행렬들 중 특정한 형태의 행렬로 구성된 **subring**이다.

다음 집합을 정의하자:

$$
I = \left\{ \begin{pmatrix} 0 & b \\ 0 & 0 \end{pmatrix} \mid b \in \mathbb{R} \right\}
$$

이것은 $R$의 **additive subgroup**이며, 다음 계산을 통해 **ideal**임을 확인할 수 있다:

$$
\begin{pmatrix} x & y \\ 0 & x \end{pmatrix} 
\begin{pmatrix} 0 & b \\ 0 & 0 \end{pmatrix} 
= \begin{pmatrix} 0 & xb \\ 0 & 0 \end{pmatrix} \in I
$$

$$
\begin{pmatrix} 0 & b \\ 0 & 0 \end{pmatrix}
\begin{pmatrix} x & y \\ 0 & x \end{pmatrix}
= \begin{pmatrix} 0 & bx \\ 0 & 0 \end{pmatrix} \in I
$$

따라서 $I$는 $R$의 **ideal**이다.

이제 $R/I$는 다음과 같은 형태의 **coset**으로 이루어진다:

$$
\begin{pmatrix} a & b \\ 0 & a \end{pmatrix} 
= \begin{pmatrix} a & 0 \\ 0 & a \end{pmatrix}
+ \begin{pmatrix} 0 & b \\ 0 & 0 \end{pmatrix}
$$

$$
\Rightarrow
\begin{pmatrix} a & b \\ 0 & a \end{pmatrix} + I
= \begin{pmatrix} a & 0 \\ 0 & a \end{pmatrix} + I
$$

따라서 $R/I$의 모든 원소는 실수 $a$에 대응된다. 즉,

$$
\begin{pmatrix} a & b \\ 0 & a \end{pmatrix} + I \mapsto a
$$

는 $\mathbb{R}$로의 **isomorphism**을 정의한다.

다른 방식으로 접근하면 다음과 같다:
사상 $\varphi : R \to \mathbb{R}$를 다음과 같이 정의하자:

$$
\varphi\left(\begin{pmatrix} a & b \\ 0 & a \end{pmatrix}\right) = a
$$

두 원소를 더하거나 곱할 때,

* 덧셈:

$$
\begin{pmatrix} a & b \\ 0 & a \end{pmatrix}
+ \begin{pmatrix} c & d \\ 0 & c \end{pmatrix}
= \begin{pmatrix} a + c & b + d \\ 0 & a + c \end{pmatrix}
$$

$$
\Rightarrow \varphi(\text{합}) = a + c
= \varphi(...) + \varphi(...)
$$

* 곱셈:

$$
\begin{pmatrix} a & b \\ 0 & a \end{pmatrix}
\begin{pmatrix} c & d \\ 0 & c \end{pmatrix}
= \begin{pmatrix} ac & ad + bc \\ 0 & ac \end{pmatrix}
$$

$$
\Rightarrow \varphi(\text{곱}) = ac = \varphi(...) \cdot \varphi(...)
$$

이므로 $\varphi$는 **homomorphism**이다. 또한,

$$
\ker \varphi = I
\Rightarrow R/I \cong \mathbb{R}
$$

---


#### Example 8
$R$이 다음과 같다고 하자.
$$
R = \left\{ \begin{pmatrix} a & -b \\ b & a \end{pmatrix} \mid a, b \in \mathbb{R} \right\}
$$
   사상 $\psi: R \to \mathbb{C}$를 다음과 같이 정의하자:

$$
\psi\left(\begin{pmatrix} a & -b \\ b & a \end{pmatrix}\right) = a + bi
$$

이 사상은 $R$에서 $\mathbb{C}$로의 **isomorphism**이며,
따라서 $R \cong \mathbb{C}$

---


#### Example 9
$R$을 단위원을 갖는 **commutative ring**이라 하고, $a \in R$라 하자.

$$
(a) = \{ ra \mid r \in R \}
$$

는 $R$의 **ideal**이다. 실제로 $u = xa$, $v = ya \in (a)$라 하면:

$$
u \pm v = xa \pm ya = (x \pm y)a \in (a)
$$

또한 $r \in R$, $u = xa \in (a)$일 때:

$$
ru = r(xa) = (rx)a \in (a)
$$

따라서 $(a)$는 $R$의 **ideal**이다.

만약 $R$이 **commutative**하지 않다면, 위 정의의 집합은 **ideal**이 아닐 수도 있다. 그러나 최소한 **left ideal**임은 확실하다.

<!-- TODO() -->