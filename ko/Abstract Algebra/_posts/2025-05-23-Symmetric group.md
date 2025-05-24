---
title: "THE SYMMETRIC GROUP"
excerpt: "책 기준 3장 내용"
tags: math mathematics abstract algebra 
header:
  teaser: https://media.wiley.com/product_data/coverImage300/92/04713687/0471368792.jpg
---

# 3 THE SYMMETRIC GROUP

## 3.1 Preliminaries

Chapter 2에서 추상적인 group에 대해 증명한 정리를 다시 상기해보자. 이 결과는 **Cayley’s Theorem** (Theorem 2.5.1)으로 알려져 있으며, 임의의 group \$G\$는 어떤 적절한 집합 \$S\$에 대한 $A(S)$의 subgroup과 **isomorphic**하다는 것을 말한다. 여기서 \$A(S)\$는 \$S\$ 자신의 모든 1-1 사상들로 이루어진 집합이다. 실제로 이 정리의 증명에서 우리는 집합 \$S\$로 단지 집합으로 간주한 group \$G\$ 자체를 사용하였다.

역사적으로 group은 이러한 방식으로 처음 등장했다. 추상적인 group 개념이 정의되기 오래전인 18세기 말과 19세기 초, Lagrange, Abel, Galois 등의 작업에서는 permutation에 대한 결과들이 먼저 등장한다. 그러나 group의 추상 개념은 19세기 중반에 Cayley에 의해 어느 정도 정식화되었다.

isomorphic한 group은 동일한 구조를 가지므로, Cayley’s Theorem은 \$A(S)\$의 group들이 보편적인 성격을 지님을 시사한다. 만약 임의의 집합 \$S\$에 대해 \$A(S)\$의 모든 subgroup의 구조를 알 수 있다면, 우리는 모든 group의 구조를 알 수 있게 된다. 그러나 이는 기대하기엔 너무 과도한 목표다. 그럼에도 불구하고, 임의의 group \$G\$를 어떤 \$A(S)\$에 isomorphic하게 포함시키는 이 embedding을 활용할 수는 있다. 이렇게 하면 추상적인 \$G\$를 \$S\$ 위의 잘 정의된 사상들의 집합으로 바꾸어 보다 구체적인 대상으로 만든다는 장점이 있다.

우리는 임의의 집합 \$S\$에 대한 \$A(S)\$의 subgroup들에 대해서는 다루지 않을 것이다. 집합 \$S\$가 무한하면 \$A(S)\$는 매우 복잡하고 난해해진다. 심지어 \$S\$가 유한하더라도 \$A(S)\$의 전체 구조를 파악하는 것은 거의 불가능하다.

이 장에서는 \$S\$가 유한 집합일 때의 \$A(S)\$만 고려한다. \$S\$의 원소 수가 \$n\$이면, \$A(S)\$를 **symmetric group of degree \$n$** 이라 부르고 \$S\_n\$으로 표기한다. \$S\_n\$의 원소들을 **permutation**이라 부르며, 우리는 그것들을 소문자 그리스 문자로 표기할 것이다.

두 원소 \$u, r \in A(S)\$의 곱을 \$(ur)(s) = u(r(s))\$로 정의했기 때문에, 우리는 \$S\_n\$의 원소들을 적절한 기호로 나타낼 때 오른쪽에서 왼쪽으로 곱하는 방식으로 계산할 것이다. 다른 대수학 교재를 보면 permutation을 왼쪽에서 오른쪽으로 곱하기도 하므로, 독자는 어떤 방향으로 곱하는지를 항상 확인해야 한다. 우리의 정의에 일관되게 따르기 위해 우리는 **오른쪽에서 왼쪽으로 곱한다**.

Cayley’s Theorem에 따르면, 유한 group \$G\$의 order가 \$n\$이면 \$G\$는 \$S\_n\$의 subgroup과 isomorphic하다. 또한 \$S\_n\$의 원소 수는 \$n!\$이다. 일반적으로 우리는 \$G\$가 \$S\_n\$의 subgroup이라고 말한다. \$n\$이 크지 않아도 \$n!\$은 매우 커지므로, \$G\$는 \$S\_n\$ 안의 아주 작은 부분만 차지한다. 가능한 한 작은 \$n\$에 대해 \$G\$를 \$S\_n\$에 포함시키는 것이 바람직하다. 특정한 유한 group의 경우 이는 특히 만족스럽게 이루어질 수 있다.

\$S\$가 \$n\$개의 원소를 갖는 유한 집합일 때, \$S = {x\_1, x\_2, \dots, x\_n}\$라 하자. permutation \$u \in S\_n = A(S)\$가 주어지면, 각 \$k = 1,2,\dots,n\$에 대해 \$u(x\_k) \in S\$이므로 \$u(x\_k) = x\_{i\_k}\$이고 \$1 \le i\_k \le n\$이다. \$u\$는 1-1이므로 \$j \ne k\$일 때 \$u(x\_j) \ne u(x\_k)\$이다. 따라서 \$i\_1, i\_2, \dots, i\_n\$은 \$1\$부터 \$n\$까지의 수들을 어떤 순서로 재배열한 것이다.

결국 \$u\$의 작용은 단지 \$x\_j\$의 첨자에 대한 작용으로 결정되므로, 기호 \$x\$ 자체는 과잉이다. 우리는 편의상 \$S = {1, 2, \dots, n}\$이라 가정할 수 있다.

이제 \$A(S)\$의 두 원소 \$u, r\$의 곱에 대해 다시 생각해보자. 우리는 \$(ur)(s) = u(r(s))\$으로 정의하였다. Chapter 1 Section 4에서 \$A(S)\$는 group의 네 가지 공리를 만족함을 보였고, 이는 우리가 abstract group을 정의할 때 모델로 삼았던 것이다. 따라서 \$S\_n\$은 mapping의 곱에 대해 group이 된다.

permutation \$u \in S\_n\$을 나타내기 위한 간편한 표기법이 필요하다. 가장 명확한 방식 중 하나는 \$u\$가 \$S\$의 각 원소에 대해 무엇을 하는지를 표로 나타내는 것이다. 이전에는 예를 들어 \$u: x\_1 \mapsto x\_2,\ x\_2 \mapsto x\_3,\ x\_3 \mapsto x\_1\$과 같이 표현했지만, 이 방식은 번거롭고 공간을 많이 차지한다. 우리는 이를 더 간결하게 만들 수 있다.

예를 들어, \$u \in S\_3\$를 다음과 같이 표기한다:

$$
u = \begin{pmatrix}
1 & 2 & 3 \\
3 & 1 & 2
\end{pmatrix}
$$

이 기호에서 두 번째 줄의 숫자는 그 위에 있는 숫자의 image이다. 첫 줄은 보통 \$1, 2, \dots, n\$의 순서이지만, 첫 줄의 순서를 바꾸어도 대응되는 두 번째 줄이 정확히 따라오면 동일한 permutation이다. 예를 들어:

$$
u = \begin{pmatrix}
1 & 2 & 3 \\
3 & 1 & 2
\end{pmatrix}
= \begin{pmatrix}
2 & 3 & 1 \\
1 & 2 & 3
\end{pmatrix}
= \begin{pmatrix}
3 & 1 & 2 \\
2 & 3 & 1
\end{pmatrix}
$$

만약 우리가 \$u = \begin{pmatrix}1 & 2 & 3 \ 3 & 1 & 2 \end{pmatrix}\$을 알고 있다면, \$u^{-1}\$은 어떻게 구할 수 있을까? 쉽게 말해 위 기호를 뒤집기만 하면 된다. 즉:

$$
u^{-1} = \begin{pmatrix}
3 & 1 & 2 \\
1 & 2 & 3
\end{pmatrix}
$$

항등원 \$e\$는 모든 원소를 그대로 두는 permutation이며, 다음과 같이 표현된다:

$$
e = \begin{pmatrix}
1 & 2 & 3 \\
1 & 2 & 3
\end{pmatrix}
$$

permutation의 곱은 어떤 방식으로 이 기호들로 표현되는가? \$ur\$은 “먼저 \$r\$을 적용하고 그 결과에 \$u\$를 적용”하는 것을 의미한다. \$r\$의 첫 줄에서 \$k\$를 보고, 두 번째 줄에서 \$i\_k\$를 확인한 후, \$u\$의 첫 줄에서 \$i\_k\$를 찾고 그에 해당하는 두 번째 줄의 값을 확인한다. 이 값이 \$ur\$가 \$k\$에 대해 가지는 값이다. 이 과정을 \$k = 1,2,\dots,n\$에 대해 반복하면 \$ur\$의 표현을 얻을 수 있다.

예를 들어 \$u, r \in S\_5\$가 다음과 같을 때:

$$
u = \begin{pmatrix}
1 & 2 & 3 & 4 & 5 \\
5 & 2 & 1 & 3 & 4
\end{pmatrix}, \quad
r = \begin{pmatrix}
1 & 2 & 3 & 4 & 5 \\
4 & 5 & 1 & 2 & 3
\end{pmatrix}
$$

\$ur\$은 다음과 같이 계산된다:

$$
ur = \begin{pmatrix}
1 & 2 & 3 & 4 & 5 \\
3 & 4 & 5 & 2 & 1
\end{pmatrix}
$$

이 방식도 간결하지만, 첫 줄이 항상 \$1, 2, \dots, n\$이라는 점을 감안하면 이 줄은 생략할 수 있다. 다음 절에서는 더 간결한 cycle 표기법을 소개할 것이다.

---

## 3.2 Cycles

이제 permutation을 나타내는 또 다른 방식, 즉 **cycle notation**을 소개하자. 이 표기법은 특히 permutation이 많은 경우에 더 간단하고 효율적이다.

각 permutation \$u\$가 \$S = {1, 2, \dots, n}\$의 원소들을 다른 원소들로 보낸다고 하자. 우리가 할 일은 각 원소 \$i\$가 어디로 가는지를 따라가며, 순환 구조를 파악하는 것이다.

\$u\$의 작용이 다음과 같다고 하자:

$$
u(i_1) = i_2, \quad u(i_2) = i_3, \quad \dots, \quad u(i_{r-1}) = i_r, \quad u(i_r) = i_1
$$

이 경우 \$u\$는 \$i\_1 \mapsto i\_2 \mapsto \cdots \mapsto i\_r \mapsto i\_1\$과 같은 순환 구조를 가진다. 우리는 이를 간단히 다음과 같이 표기한다:

$(i_1\ i_2\ \dots\ i_r)$

이것을 **cycle**이라 부른다. \$r = 1\$인 경우 \$(i\_1)\$은 \$i\_1\$을 고정시키는 항등 사상이므로 일반적으로 생략한다. \$r = 2\$이면 \$(i\_1\ i\_2)\$는 두 원소를 서로 교환하는 permutation으로, 이를 **transposition**이라 한다.

예를 들어 permutation \$u \in S\_5\$가 다음과 같다고 하자:

$$
u = \begin{pmatrix}
1 & 2 & 3 & 4 & 5 \\
4 & 5 & 3 & 1 & 2
\end{pmatrix}
$$

이때:

* \$u(1) = 4\$, \$u(4) = 1\$이므로 cycle \$(1\ 4)\$
* \$u(2) = 5\$, \$u(5) = 2\$이므로 cycle \$(2\ 5)\$
* \$u(3) = 3\$이므로 고정 → 생략 가능

따라서 \$u = (1\ 4)(2\ 5)\$로 나타낼 수 있다. 이 두 cycle은 서로 영향을 주지 않으므로 이를 **disjoint cycles**이라 부른다. disjoint cycles들은 commute한다. 즉:

$(a\ b)(c\ d) = (c\ d)(a\ b)$

이제 permutation이 여러 개의 disjoint cycles로 유일하게 표현된다는 사실을 다음과 같은 Theorem으로 제시한다.

---

### **Theorem 3.2.1**

모든 permutation \$u \in S\_n\$은 **disjoint cycles**의 곱으로 유일하게 표현된다. 단, cycle의 순서는 중요하지 않다.

**설명:** 이 정리는 permutation을 분해할 때 어떤 원소부터 시작하든 최종적으로 얻어지는 cycle의 구조는 동일하다는 것을 보장한다. 단지 cycle의 나열 순서만 다를 수 있을 뿐이다.

---

이제 cycle의 **order**에 대해 살펴보자.

### **Definition.**

Cycle \$(a\_1\ a\_2\ \dots\ a\_r)\$의 **order**는 \$r\$이다. 이는 해당 cycle을 \$r\$번 곱하면 항등 permutation이 되며, \$r\$보다 작은 양의 정수 \$k\$에 대해서는 \$k\$번 곱해도 항등원이 되지 않는다는 것을 의미한다.

즉:

$$
(a_1\ a_2\ \dots\ a_r)^r = \text{id}
$$

---

### **Theorem 3.2.2**

서로 disjoint한 cycles의 곱으로 표현된 permutation \$u\$의 order는 각 cycle의 order의 **최소공배수 (lcm)** 이다.

즉, \$u = c\_1 c\_2 \dots c\_k\$이고 \$c\_i\$의 order가 \$r\_i\$일 때:

$$
\text{ord}(u) = \operatorname{lcm}(r_1, r_2, \dots, r_k)
$$

---

예를 들어 \$u = (1\ 4)(2\ 5)\$는 두 개의 transposition으로 이루어진 permutation이다. 각 cycle의 order는 2이므로:

$$
\text{ord}(u) = \operatorname{lcm}(2, 2) = 2
$$

---

cycle notation의 또 다른 장점은 곱셈 연산을 시각적으로 더 쉽게 이해할 수 있다는 것이다. 예를 들어, \$(1\ 2\ 3)(3\ 4)\$와 같은 곱이 주어졌을 때, \$3\$이 두 cycle에 모두 등장하므로 이들은 **not disjoint**하며 순서에 따라 곱의 결과가 달라진다.

이와 달리 disjoint cycle들은 commute하므로 계산이 훨씬 단순하다.

또한, 어떤 permutation이 **odd permutation**인지 **even permutation**인지를 cycle 분해를 통해 판별할 수 있다. 이 내용은 다음 절에서 다룬다.

---

## 3.3 Even and Odd Permutations

모든 permutation은 2-cycle, 즉 **transposition**들의 곱으로 표현될 수 있다. 예를 들어, cycle $(1\ 2\ 3)$은 두 개의 transposition으로 다음과 같이 쓸 수 있다:

$$
(1\ 2\ 3) = (1\ 3)(1\ 2)
$$

이 표현은 permutation의 행동이 "먼저 1을 2로, 그다음 2를 3으로, 그리고 3을 다시 1로" 돌아가는 것을 반영한다.

transposition $(a\ b)$는 단지 두 원소 $a$, $b$를 교환하는 permutation이며, 그 이외의 원소는 고정된다. 우리는 다음 정리를 통해 permutation이 항상 transposition들의 곱으로 표현될 수 있다는 것을 공식화한다.

---

### **Theorem 3.3.1**

모든 permutation은 transposition들의 곱으로 표현될 수 있다.

---

그러나 동일한 permutation이라도 여러 가지 방법으로 transposition들의 곱으로 표현될 수 있다. 예를 들어, permutation $u = (1\ 2\ 3)$는 아래처럼 두 가지 방법으로 쓸 수 있다:

$$
u = (1\ 3)(1\ 2) = (2\ 3)(1\ 3)
$$

이러한 표현이 중복되는 것처럼 보이지만, 흥미로운 점은 다음과 같다: 어떤 permutation이 짝수 개의 transposition으로 표현될 수 있다면, 어떤 다른 표현이든 **반드시** 짝수 개의 transposition만을 포함한다. 이는 permutation의 본질적인 성질이며, 다음 정리에 의해 보장된다.

---

### **Theorem 3.3.2**

임의의 permutation이 두 가지 방법으로 transposition들의 곱으로 표현되었다고 하자. 만약 하나가 짝수 개의 transposition으로 구성되었다면, 다른 표현도 반드시 짝수 개이다. 마찬가지로, 하나가 홀수 개이면 다른 표현도 반드시 홀수 개이다.

이 정리는 transposition의 개수의 \*\*짝수/홀수성(parity)\*\*이 permutation의 **고유한 불변량**임을 뜻한다.

---

### **Definition.**

transposition의 곱으로 표현될 때 짝수 개의 transposition을 필요로 하는 permutation을 **even permutation**, 홀수 개를 필요로 하는 permutation을 **odd permutation**이라 한다.

---

따라서 permutation의 짝수/홀수성은 well-defined이며, 이를 바탕으로 다음과 같은 중요한 subgroup을 정의할 수 있다.

---

### **Definition.**

$S_n$의 모든 even permutation들로 구성된 집합을 $A_n$이라 하며, 이는 \*\*alternating group of degree $n$\*\*이라 불린다.

---

$A_n$은 $S_n$의 subgroup임은 물론이고, 사실상 **normal subgroup**이다. 그 이유는 다음과 같다:

1. $A_n$은 짝수 개의 transposition으로 표현되는 permutation들로 구성된다.
2. permutation $u \in A_n$, $g \in S_n$일 때, $gug^{-1}$은 역시 짝수 개의 transposition으로 표현된다.
3. 따라서 $g A_n g^{-1} \subseteq A_n$, 즉 $A_n \trianglelefteq S_n$

또한 $A_n$의 원소 수는 정확히 $S_n$의 절반이다:

$$
|A_n| = \frac{n!}{2}
$$

이것은 permutation의 반은 even이고, 반은 odd임을 의미한다.

---

**예제.** $S_3$의 원소는 총 6개이며, 이 중 even permutation은 다음과 같다:

* $e = \text{id}$
* $(1\ 2\ 3)$
* $(1\ 3\ 2)$

나머지 3개, 즉 $(1\ 2), (1\ 3), (2\ 3)$은 odd permutation이다. 따라서 $A_3 = \{e, (1\ 2\ 3), (1\ 3\ 2)\}$

---

alternating group $A_n$은 $n \geq 5$일 때 단순 group이 되며, group 이론 및 Galois 이론에서 매우 중요한 역할을 한다. $A_5$는 첫 번째로 등장하는 **nonabelian simple group**이다.

---

다음 절에서는 $S_n$과 $A_n$의 구조와 관련된 더 깊은 주제들을 다룰 것이다.

---

## 3.4 The Sign of a Permutation

앞 절에서 보았듯이, 모든 permutation은 transposition들의 곱으로 표현될 수 있으며, 그 표현에 포함된 transposition의 수가 짝수인지 홀수인지에 따라 **even permutation** 또는 **odd permutation**으로 분류된다.

이제 우리는 각 permutation에 이 정보를 수치로 부여하는 사상, 즉 **sign function**을 정의한다.

---

### **Definition.**

permutation $u \in S_n$에 대해, $u$를 transposition들의 곱으로 표현한 뒤 그 개수를 $r$이라 하자. 그러면 다음과 같이 정의된 함수

$$
\operatorname{sgn}(u) = (-1)^r
$$

를 $u$의 **sign**이라 부르며, $\operatorname{sgn} : S_n \rightarrow \{1, -1\}$이다.

* $\operatorname{sgn}(u) = 1$ ⇔ $u$는 even permutation
* $\operatorname{sgn}(u) = -1$ ⇔ $u$는 odd permutation

---

이제 이 sign 함수가 **homomorphism**이 되는지를 살펴보자. 그 목적을 위해 아래 정리를 소개한다.

---

### **Theorem 3.4.1**

sign 함수 $\operatorname{sgn} : S_n \rightarrow \{1, -1\}$는 group homomorphism이며, 다음을 만족한다:

* $\operatorname{sgn}(uv) = \operatorname{sgn}(u) \cdot \operatorname{sgn}(v)$
* $\operatorname{ker}(\operatorname{sgn}) = A_n$

---

**증명 스케치:**

1. $u$와 $v$가 각각 $r, s$개의 transposition으로 표현되었다고 하자.
   그러면 $uv$는 적어도 $r+s$개의 transposition으로 표현될 수 있으며,

   $$
   \operatorname{sgn}(uv) = (-1)^{r+s} = (-1)^r \cdot (-1)^s = \operatorname{sgn}(u) \cdot \operatorname{sgn}(v)
   $$

2. $\operatorname{sgn}(u) = 1$이면 $u \in A_n$, 즉 even permutation이다.
   반대로 $u \in A_n$이면 $\operatorname{sgn}(u) = 1$

∴ $\operatorname{ker}(\operatorname{sgn}) = A_n$

---

이 sign 함수는 매우 중요한 성질들을 가지고 있으며, determinant 함수의 정의나 alternating tensor의 부호 등 다양한 수학 분야에서 핵심적으로 등장한다.

이제 permutation의 또 다른 표현 방법인 **matrix 표현**을 간단히 살펴보자.

---

### **Permutation Matrices**

permutation $u \in S_n$에 대해, $u$의 작용을 $n \times n$ 행렬로 나타낼 수 있다. 이 행렬은 각 행과 열에 정확히 하나의 $1$이 있고 나머지는 모두 $0$이다. 이때 $1$의 위치는 $u$가 각 정수를 어디로 보내는지를 나타낸다.

예를 들어 $u = (1\ 3\ 2) \in S_3$라면, permutation matrix는 다음과 같다:

$$
P_u =
\begin{pmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & 1 & 0
\end{pmatrix}
$$

이 행렬은 다음과 같은 성질을 가진다:

* $P_u \cdot P_v = P_{uv}$
* $\det(P_u) = \operatorname{sgn}(u)$

이 마지막 항목은 매우 중요하다. permutation의 sign이 바로 대응되는 permutation matrix의 determinant라는 사실은 **선형대수학에서 determinant의 기초 정의**와 직접적으로 연결된다.

---

다음 절에서는 permutation의 parity를 구하는 또 다른 방법—즉, **inversion의 수**를 세는 방법—을 소개할 것이다.

— 계속하려면 “continue”를 입력하세요 —

<!-- TODO() -->