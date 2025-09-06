---
title: "현대대수 주요개념 총정리"
excerpt: 
tags: math abstract-algebra concept
header:
  teaser: https://drive.google.com/thumbnail?id=1uhNc8ro4rr31LsFmXllQU5ADHh9scufz&sz=w1000
---

주요 개념을 총정리해 드리겠습니다. 내용은 집합론, 군론, 환론, 체론 순으로 구성되어 있습니다.

---

### **문제 해결을 위한 핵심 개념 총정리**

#### **1. 기초 개념 (Fundamental Concepts)**

**1.1. 집합론 (Set Theory)**
*   **집합 (Set)**: 객체들의 모임.
*   **원소 (Element)**: 집합 내의 객체. `a ∈ S`는 'a가 S의 원소이다'를 의미.
*   **부분집합 (Subset)**: `S ⊆ T`는 S의 모든 원소가 T에 속함을 의미. `T ⊇ S`와 같음.
*   **공집합 (Null/Empty Set)**: 원소가 없는 집합. `∅`로 표기하며, 모든 집합의 부분집합임.
*   **합집합 (Union)**: `A ∪ B`는 A 또는 B에 속하는 모든 원소의 집합.
*   **교집합 (Intersection)**: `A ∩ B`는 A와 B 모두에 속하는 원소의 집합.
*   **차집합 (Difference)**: `A - B`는 A에는 속하지만 B에는 속하지 않는 원소의 집합.
*   **여집합 (Complement)**: `S - A`를 S에 대한 A의 여집합이라 하며 `A'`로 표기.
*   **카르테시안 곱 (Cartesian Product)**: `A × B = {(a, b) | a ∈ A, b ∈ B}` (순서쌍의 집합).
*   **집합의 등식 증명**: `S = T`를 증명하려면 `S ⊆ T`와 `T ⊆ S`를 모두 보여야 함.
*   **드 모르간 법칙 (De Morgan Rules)**:
    *   `(A ∩ B)' = A' ∪ B'`
    *   `(A ∪ B)' = A' ∩ B'`
*   **원소의 개수 (m(C))**:
    *   `m(A ∪ B) = m(A) + m(B) - m(A ∩ B)`
    *   `m(A × B) = m(A)m(B)`
    *   `n`개의 원소를 가진 집합의 부분집합의 개수는 `2^n`개.

**1.2. 사상 (Mappings/Functions)**
*   **함수/사상 (Function/Mapping)**: 두 집합 `S`, `T`에 대해 `f: S → T`는 S의 각 원소 `s`에 T의 유일한 원소 `t`를 할당하는 규칙. `t`를 `s`의 `f`에 의한 **상 (Image)**이라 하고 `t = f(s)`로 씀.
*   **상 집합 (Image of a set)**: `f(S) = {f(s) ∈ T | s ∈ S}`.
*   **항등 함수 (Identity Function)**: `i: S → S`로 `i(s) = s`로 정의.
*   **상등 (Equality of Mappings)**: `f = g`는 `f(s) = g(s)`가 모든 `s ∈ S`에 대해 성립할 때.
*   **전사 (Onto/Surjective)**: `f: S → T`가 T의 모든 원소 `t`가 S의 어떤 `s`의 상이 될 때. 즉, `f(S) = T`.
*   **단사 (One-to-one/Injective)**: `f: S → T`가 `s₁ ≠ s₂`일 때 `f(s₁) ≠ f(s₂)`일 때. 즉, `f(s₁) = f(s₂)`이면 `s₁ = s₂`.
*   **역상 (Inverse Image)**: `f⁻¹(A) = {s ∈ S | f(s) ∈ A}`.
*   **전단사 (One-to-one correspondence/Bijection)**: `f`가 단사이면서 전사일 때.
*   **합성 (Composition)**: `g: S → T`와 `f: T → U`일 때, `f ∘ g: S → U`는 `(f ∘ g)(s) = f(g(s))`로 정의.
    *   **결합 법칙 (Associative Law)**: `h ∘ (g ∘ f) = (h ∘ g) ∘ f` [Lemma 1.3.1].
    *   **단사성 보존**: `g`, `f`가 단사이면 `f ∘ g`도 단사 [Lemma 1.3.2].
    *   **전사성 보존**: `g`, `f`가 전사이면 `f ∘ g`도 전사 [Remark after Lemma 1.3.2].
    *   **전단사성 보존**: `g`, `f`가 전단사이면 `f ∘ g`도 전단사 [Lemma 1.3.3].
*   **역함수 (Inverse of a Bijection)**: `f: S → T`가 전단사이면 `f⁻¹: T → S`도 전단사이고 `f ∘ f⁻¹ = i_T`, `f⁻¹ ∘ f = i_S` [Lemma 1.3.4].

**1.3. 정수 (The Integers)**
*   **정돈 원리 (Well-Ordering Principle)**: 음이 아닌 정수의 모든 공집합이 아닌 부분집합은 가장 작은 원소를 가짐.
*   **유클리드 알고리즘 (Euclid's Algorithm)**: `m, n`이 정수이고 `n > 0`일 때, `m = qn + r`인 정수 `q, r`이 존재하며 `0 ≤ r < n`. [Theorem 1.5.1]
*   **나눗셈 (Divisibility)**: `m | n`은 `n = cm`인 정수 `c`가 존재할 때.
*   **최대공약수 (Greatest Common Divisor, GCD)**: `a, b` (모두 0은 아님)의 GCD `c`는 `c > 0`, `c | a`, `c | b`이고 `d | a`, `d | b`인 모든 `d`에 대해 `d | c`일 때. `(a, b)`로 표기.
    *   **존재 및 형태**: `c = (a, b)`는 존재하고 유일하며, `c = m₀a + n₀b`인 정수 `m₀, n₀`가 존재 [Theorem 1.5.3].
*   **서로소 (Relatively Prime)**: `(a, b) = 1`일 때 `a, b`는 서로소.
    *   **성질**: `a, b`가 서로소일 필요충분조건은 `1 = ma + nb`인 정수 `m, n`이 존재 [Theorem 1.5.4].
    *   **약분 정리**: `(a, b) = 1`이고 `a | bc`이면 `a | c` [Theorem 1.5.5].
    *   **확장된 약분 정리**: `b, c`가 `a`와 각각 서로소이면 `bc`도 `a`와 서로소 [Corollary to Theorem 1.5.5].
*   **소수 (Prime Number)**: `p > 1`인 정수 `p`로, 어떤 정수 `a`에 대해 `p | a`이거나 `p`와 `a`가 서로소일 때.
    *   **소수의 성질**: `p`가 소수이고 `p | (a₁a₂...a_n)`이면 `p | a_i`인 `i`가 존재 [Theorem 1.5.6].
*   **산술의 기본 정리 (Fundamental Theorem of Arithmetic)**:
    *   `n > 1`이면 `n`은 소수이거나 소수들의 곱 [Theorem 1.5.7].
    *   `n > 1`이면 `n`은 `n = p₁^a₁ p₂^a₂ ... p_k^a_k` (`p₁ < p₂ < ... < p_k`는 소수, `a_i > 0`) 형태로 유일하게 쓸 수 있음 [Theorem 1.5.8].

**1.4. 수학적 귀납법 (Mathematical Induction)**
*   **원리**: `P(n)`이 양의 정수에 대한 명제일 때, `P(1)`이 참이고 `P(k)`가 참일 때 `P(k+1)`도 참이면, 모든 양의 정수 `n`에 대해 `P(n)`은 참이다 [Theorem 1.6.1].

**1.5. 복소수 (Complex Numbers)**
*   **복소수 (Complex Number)**: `a + bi` 형태의 수. `i² = -1`.
*   **복소 켤레 (Complex Conjugate)**: `z = a + bi`일 때 `z̄ = a - bi`.
    *   **성질**: `z̄ = z`, `z + w = z̄ + w̄`, `zw = z̄w̄`, `(z/w) = z̄/w̄` [Lemma 1.7.1].
*   **절대값 (Absolute Value)**: `|z| = √(a² + b²)`.
    *   **성질**: `|uv| = |u||v|` [Lemma 1.7.3].
*   **삼각 부등식 (Triangle Inequality)**: `|z + w| ≤ |z| + |w|` [Theorem 1.7.5].
*   **극 형식 (Polar Form)**: `z = r(cosθ + i sinθ)`.
*   **드 무아브르 정리 (De Moivre's Theorem)**: `(cosθ + i sinθ)^n = cos(nθ) + i sin(nθ)`. (정수 `n`에 대해 성립하며, 유리수 `r`에 대해서도 성립).
*   **`n`차 단위근 (n'th Roots of Unity)**: `ω_n = cos(2π/n) + i sin(2π/n)`.

#### **2. 군 이론 (Group Theory)**

**2.1. 군의 정의와 예시 (Definitions and Examples of Groups)**
*   **군 (Group)**: 비어있지 않은 집합 `G`와 이항 연산 `*`에 대해 다음 네 가지 공리(군의 공리)를 만족할 때.
    *   `(a) 닫혀있음 (Closure)`: `a, b ∈ G`이면 `a * b ∈ G`.
    *   `(b) 결합 법칙 (Associativity)`: `a * (b * c) = (a * b) * c`.
    *   `(c) 항등원 (Identity Element)`: `a * e = e * a = a`인 특정한 원소 `e ∈ G`가 존재.
    *   `(d) 역원 (Inverse Element)`: 각 `a ∈ G`에 대해 `a * b = b * a = e`인 원소 `b ∈ G` (`a⁻¹`로 표기)가 존재.
*   **아벨 군 (Abelian Group)**: `a * b = b * a`가 모든 `a, b ∈ G`에 대해 성립하는 군.
*   **유한 군 (Finite Group)**: 원소의 개수가 유한한 군. 원소의 개수를 **위수 (Order)** `|G|`라 함.
*   **대칭군 (Symmetric Group, S_n)**: `n`개의 원소를 가진 집합 `S`의 모든 1-1 사상들의 집합 `A(S)`. `|S_n| = n!` [Lemma 1.4.2].
*   **지수 표기법**: `a^n = a * a * ... * a` (n번), `a⁻ⁿ = (a⁻¹)ⁿ`, `a⁰ = e`.

**2.2. 군의 기본 성질 (Some Simple Remarks)**
*   **항등원의 유일성**: 군의 항등원은 유일.
*   **역원의 유일성**: 군의 각 원소의 역원은 유일.
*   **역원의 역원**: `(a⁻¹)⁻¹ = a` [Lemma 2.2.1(c)].
*   **곱의 역원**: `(ab)⁻¹ = b⁻¹a⁻¹` [Lemma 2.2.1(d)].
*   **소거 법칙 (Cancellation Law)**:
    *   `ab = ac`이면 `b = c`.
    *   `ba = ca`이면 `b = c` [Lemma 2.2.2].

**2.3. 부분군 (Subgroups)**
*   **부분군 (Subgroup)**: 군 `G`의 비어있지 않은 부분집합 `H`가 `G`의 연산에 대해 스스로 군을 이룰 때.
*   **부분군 판정법 (Subgroup Test)**: 비어있지 않은 부분집합 `A ⊆ G`가 다음 두 조건을 만족하면 `A`는 `G`의 부분군이다.
    *   `A`는 `G`의 연산에 대해 닫혀있음 (`a, b ∈ A`이면 `ab ∈ A`).
    *   `a ∈ A`이면 `a⁻¹ ∈ A`. [Lemma 2.3.1]
*   **유한 부분군 판정법 (Finite Subgroup Test)**: 유한하고 비어있지 않은 부분집합 `H ⊆ G`가 `G`의 연산에 대해 닫혀있으면 `H`는 `G`의 부분군이다 [Lemma 2.3.2].
*   **주기 부분군 (Cyclic Subgroup)**: `a ∈ G`에 의해 생성된 `{a^i | i는 모든 정수}` 형태의 부분군. `<a>`로 표기.
*   **중심화 부분군 (Centralizer)**: `C(a) = {g ∈ G | ga = ag}`. `a`와 가환인 `G`의 모든 원소들의 집합.
*   **중심 (Center)**: `Z(G) = {z ∈ G | zx = xz`가 모든 `x ∈ G`에 대해 성립}`. `G`의 모든 원소와 가환인 원소들의 집합.

**2.4. 동치 관계와 라그랑주 정리 (Equivalence Relations and Lagrange's Theorem)**
*   **동치 관계 (Equivalence Relation)**: 집합 `S` 위의 관계 `~`가 다음 세 조건을 만족할 때:
    *   `(a) 반사성 (Reflexivity)`: `a ~ a`.
    *   `(b) 대칭성 (Symmetry)`: `a ~ b`이면 `b ~ a`.
    *   `(c) 추이성 (Transitivity)`: `a ~ b`이고 `b ~ c`이면 `a ~ c`.
*   **동치류 (Equivalence Class)**: `[a] = {b ∈ S | b ~ a}`.
*   **몫류 (Coset)**:
    *   `H`가 `G`의 부분군이고 `a, b ∈ G`일 때, `ab⁻¹ ∈ H`로 정의된 동치 관계의 동치류 `[b]`는 `Hb = {hb | h ∈ H}` 형태의 **우(右)몫류 (Right Coset)**.
    *   `a⁻¹b ∈ H`로 정의된 동치 관계의 동치류 `[a]`는 `aH = {ah | h ∈ H}` 형태의 **좌(左)몫류 (Left Coset)** [176, Problem 5].
*   **켤레류 (Conjugacy Class)**: `a ~ b`를 `b = x⁻¹ax`인 `x ∈ G`가 존재할 때로 정의한 동치 관계의 동치류 `[a] = {x⁻¹ax | x ∈ G}`. `cl(a)`로 표기.
*   **라그랑주 정리 (Lagrange's Theorem)**: `G`가 유한군이고 `H`가 `G`의 부분군이면, `H`의 위수 `|H|`는 `G`의 위수 `|G|`를 나눈다 [Theorem 2.4.2].
*   **원소의 위수 (Order of an element)**: `a ∈ G`의 위수 `o(a)`는 `a^m = e`를 만족하는 가장 작은 양의 정수 `m`.
    *   **성질**: 유한군 `G`의 원소 `a`의 위수 `o(a)`는 `|G|`를 나눈다 [Theorem 2.4.4].
    *   **페르마의 작은 정리 일반화**: `G`가 위수 `n`인 유한군이면 `a^n = e`가 모든 `a ∈ G`에 대해 성립 [Theorem 2.4.5].
*   **합동류 (Congruence Classes Modulo n)**: 정수 `Z`와 `n > 1`인 고정된 정수에 대해 `a ≡ b mod n` (즉 `n | (a - b)`)으로 정의된 동치 관계의 동치류 `[a]`.
    *   `Z_n = {,, ..., [n-1]}`는 덧셈 `[a] + [b] = [a + b]`에 대해 주기군을 이룬다 [Theorem 2.4.6].
    *   `U_n = {[a] ∈ Z_n | (a, n) = 1}`은 곱셈 `[a][b] = [ab]`에 대해 군을 이룬다 [169, Theorem 2.4.7]. `|U_n| = φ(n)` (`φ(n)`은 오일러 파이 함수).
    *   **오일러 정리 (Euler's Theorem)**: `a`가 `n`과 서로소인 정수이면 `a^(φ(n)) ≡ 1 mod n` [Theorem 2.4.8].
    *   **페르마의 작은 정리 (Fermat's Little Theorem)**: `p`가 소수이고 `p <binary data, 1 bytes><binary data, 1 bytes> a`이면 `a^(p-1) ≡ 1 mod p`. 또한, 임의의 정수 `b`에 대해 `b^p ≡ b mod p` [Corollary to Theorem 2.4.8].

**2.5. 준동형사상과 정규 부분군 (Homomorphisms and Normal Subgroups)**
*   **준동형사상 (Homomorphism)**: 두 군 `G`, `G'`에 대해 `φ: G → G'`가 `φ(ab) = φ(a)φ(b)`를 모든 `a, b ∈ G`에 대해 만족할 때. (연산을 보존).
    *   **성질**: `φ(e) = e'` (항등원을 항등원으로 보냄), `φ(a⁻¹) = φ(a)⁻¹` (역원을 역원으로 보냄) [Lemma 2.5.2].
    *   **상 (Image)**: `φ(G) = {φ(a) | a ∈ G}`는 `G'`의 부분군 [Lemma 2.5.3].
*   **단사 준동형사상 (Monomorphism)**: `φ`가 단사일 때.
*   **동형사상 (Isomorphism)**: `φ`가 단사이면서 전사일 때. `G ≅ G'`로 표기.
*   **자기동형사상 (Automorphism)**: `G`에서 `G` 자신으로의 동형사상.
*   **켤레 자기동형사상 (Inner Automorphism)**: `a ∈ G`에 의해 유도된 `σ_a(x) = a⁻¹xa` 형태의 자기동형사상.
*   **핵 (Kernel)**: 준동형사상 `φ: G → G'`에 대해 `Ker φ = {a ∈ G | φ(a) = e'}`.
    *   **성질**: `Ker φ`는 `G`의 부분군이며, `a⁻¹(Ker φ)a ⊆ Ker φ` [Theorem 2.5.5].
    *   **단사성 판정**: `φ`가 단사일 필요충분조건은 `Ker φ = {e}` [Corollary to Theorem 2.5.5].
*   **정규 부분군 (Normal Subgroup)**: `G`의 부분군 `N`이 `a⁻¹Na ⊆ N`를 모든 `a ∈ G`에 대해 만족할 때. `N ◁ G`로 표기.
    *   **동치 조건**: `N ◁ G`일 필요충분조건은 `a⁻¹Na = N`이 모든 `a ∈ G`에 대해 성립. 이는 모든 좌(左)몫류가 우(右)몫류와 같음 (`aN = Na`)과 동치 [Theorem 2.5.6].
    *   **핵과의 관계**: 모든 준동형사상의 핵은 정규 부분군이다. (역으로 모든 정규 부분군은 어떤 준동형사상의 핵이 된다).

**2.6. 몫군 (Factor Groups/Quotient Groups)**
*   **몫군 (Factor Group)**: `N ◁ G`일 때, 몫류 `Na`들을 원소로 갖는 집합 `G/N = {Na | a ∈ G}`는 `(Na)(Nb) = Nab`로 정의된 연산에 대해 군을 이룬다 [Theorem 2.6.1].
    *   **자연 준동형사상 (Natural Homomorphism)**: `φ: G → G/N`를 `φ(a) = Na`로 정의하면 `φ`는 전사 준동형사상이며 `Ker φ = N` [Theorem 2.6.2].
    *   **위수**: `G`가 유한군일 때 `|G/N| = |G|/|N|` [Theorem 2.6.3].

**2.7. 준동형 정리 (Homomorphism Theorems)**
*   **제1 준동형 정리 (First Homomorphism Theorem)**: `φ: G → G'`가 `G`에서 `G'`로의 전사 준동형사상이고 `K`가 `φ`의 핵이면 `G' ≅ G/K` [Theorem 2.7.1].
*   **대응 정리 (Correspondence Theorem)**: `φ: G → G'`가 `G`에서 `G'`로의 전사 준동형사상이고 `K`가 `φ`의 핵일 때, `G'`의 부분군 `H'`와 `K`를 포함하는 `G`의 부분군 `H` 사이에 일대일 대응이 존재하며 `H/K ≅ H'` [Theorem 2.7.2]. `H' ◁ G'`이면 `H ◁ G`이다.
*   **제2 준동형 정리 (Second Homomorphism Theorem)**: `H`가 `G`의 부분군이고 `N`이 `G`의 정규 부분군이면 `HN = {hn | h ∈ H, n ∈ N}`은 `G`의 부분군이고 `N ◁ HN`이며 `(HN)/N ≅ H/(H ∩ N)` [Theorem 2.7.3].
*   **제3 준동형 정리 (Third Homomorphism Theorem)**: `φ: G → G'`가 `G`에서 `G'`로의 전사 준동형사상이고 `K`가 `φ`의 핵일 때, `N' ◁ G'`이고 `N = {a ∈ G | φ(a) ∈ N'}`이면 `G/N ≅ G'/N'`. 이는 `G/N ≅ (G/K)/(N/K)`와 동치 [Theorem 2.7.4].

**2.8. 코시 정리와 실로우 정리의 예비 지식 (Cauchy's Theorem and Sylow's Theorem Preliminaries)**
*   **궤도 (Orbit)**: `f ∈ A(S)`일 때, `s ∈ S`의 궤도 `O(s) = {f^j(s) | j는 모든 정수}`.
*   **코시 정리 (Cauchy's Theorem)**: `p`가 소수이고 `p`가 유한군 `G`의 위수 `|G|`를 나누면, `G`는 위수가 `p`인 원소를 가진다 [Theorem 2.8.2].
*   **위수 `pq`인 군의 성질**:
    *   `G`의 위수가 `pq`(`p, q`는 소수, `p > q`)이고 `a`가 위수 `p`인 원소이면, `<a>`는 `G`의 정규 부분군이다 [Lemma 2.8.3].
    *   `q`가 `p-1`을 나누지 않으면, `G`는 순환군이다 [Theorem 2.8.5].
*   **서로소 위수의 가환 원소의 곱**: `a ∈ G`의 위수가 `m`이고 `b ∈ G`의 위수가 `n`이며 `m`과 `n`이 서로소이고 `ab = ba`이면, `ab`의 위수는 `mn`이다 [Lemma 2.8.4].

**2.9. 직접곱 (Direct Products)**
*   **외부 직접곱 (External Direct Product)**: 군 `G₁, ..., G_n`의 외부 직접곱 `G₁ × G₂ × ... × G_n`는 원소들을 `n`-튜플 `(a₁, ..., a_n)`으로 갖고, 연산은 각 성분별로 정의.
*   **내부 직접곱 (Internal Direct Product)**: `G`가 정규 부분군 `N₁, ..., N_n`의 내부 직접곱이라는 것은 `G`의 모든 원소 `a`가 `a = a₁a₂...a_n` (`a_i ∈ N_i`) 형태로 유일하게 표현될 때.
*   **가환성 조건**: `M, N`이 `G`의 정규 부분군이고 `M ∩ N = {e}`이면, `m ∈ M`, `n ∈ N`에 대해 `mn = nm` [Lemma 2.9.2].
*   **정리**: `G = N₁ × N₂ × ... × N_n` (외부)은 `G`가 `N₁, ..., N_n`의 내부 직접곱일 필요충분조건으로 `ψ((a₁, ..., a_n)) = a₁...a_n`인 동형사상이 존재한다 [Theorem 2.9.4].
*   **두 부분군의 직접곱 조건**: `G`가 `N₁`와 `N₂`의 내부 직접곱일 필요충분조건은 `G = N₁N₂`이고 `N₁ ∩ N₂ = {e}` [Corollary to Theorem 2.9.4].

**2.10. 유한 아벨 군 (Finite Abelian Groups)**
*   **기본 정리 (Fundamental Theorem on Finite Abelian Groups)**: 모든 유한 아벨 군은 순환군들의 직접곱이다 [Theorem 2.10.3].

**2.11. 켤레와 실로우 정리 (Conjugacy and Sylow's Theorem)**
*   **켤레류 (Conjugacy Class)**: `cl(a) = {x⁻¹ax | x ∈ G}`.
*   **중심화 부분군 (Centralizer)**: `C(a) = {x ∈ G | xa = ax}`는 `G`의 부분군 [Lemma 2.11.1].
*   **켤레류의 크기**: 유한군 `G`에서 `cl(a)`의 원소 개수는 `|G|/|C(a)| = i_G(C(a))`와 같다 [Theorem 2.11.2].
*   **켤레 방정식 (Class Equation)**: `|G| = Σ i_G(C(a))` (합은 각 켤레류에서 하나씩 원소를 택하여 계산) [Theorem 2.11.3].
*   **`p`군 (`p`-group)의 중심**: `p`가 소수이고 `|G| = p^n`이면 `G`의 중심 `Z(G)`은 자명하지 않다 (`e`가 아닌 원소를 포함한다) [Theorem 2.11.4].
*   **위수 `p²`인 군**: `p`가 소수이고 `|G| = p²`이면 `G`는 아벨 군이다 [Theorem 2.11.5].
*   **`p`-군의 정규 부분군**: `p`가 소수이고 `|G| = p^n`이면 `G`는 위수가 `p^(n-1)`인 정규 부분군을 포함한다 [Theorem 2.11.6].
*   **실로우 제1 정리 (Sylow's First Theorem)**: `G`의 위수가 `p^n m` (`p`는 소수, `p <binary data, 1 bytes><binary data, 1 bytes> m`)일 때, `G`는 위수가 `p^n`인 부분군 (`p`-실로우 부분군)을 가진다 [Theorem 2.11.7].

#### **3. 환 이론 (Ring Theory)**

**3.1. 환의 정의와 예시 (Definitions and Examples)**
*   **환 (Ring)**: 비어있지 않은 집합 `R`에 덧셈 `+`와 곱셈 `·` 두 연산이 정의되어 다음 공리들을 만족할 때:
    *   `(a)-(e)`: `(R, +)`는 아벨 군. (덧셈에 대한 닫힘, 교환, 결합, 항등원 0, 역원 -a).
    *   `(f)`: `(R, ·)`는 닫혀있음.
    *   `(g)`: `(R, ·)`는 결합 법칙 성립. (결합적 환).
    *   `(h)`: 분배 법칙 성립: `a·(b+c) = a·b+a·c` 및 `(b+c)·a = b·a+c·a`.
*   **단위원을 갖는 환 (Ring with unit)**: 곱셈에 대한 항등원 `1`이 존재하며 `1 ≠ 0`.
*   **가환환 (Commutative Ring)**: `a·b = b·a`가 성립.
*   **영인자 (Zero-divisor)**: `a ≠ 0`이고 `ab = 0`인 `b ≠ 0`가 존재할 때 `a`를 영인자라 함.
*   **정역 (Integral Domain)**: 단위원을 갖는 가환환에서 영인자가 없을 때.
*   **나눗셈 환 (Division Ring)**: 단위원을 갖는 환에서 모든 `a ≠ 0`가 곱셈 역원 `a⁻¹`를 가질 때.
*   **체 (Field)**: 가환 나눗셈 환. (즉, 곱셈에 대해 0을 제외한 원소들이 아벨 군을 이룸).
*   **부분환 (Subring)**: 환 `R`의 부분집합 `S`가 `R`의 연산을 그대로 사용하여 환을 이룰 때. `S`가 비어있지 않고 `ab ∈ S`, `a ± b ∈ S`이면 부분환이다.

**3.2. 환의 기본 성질 (Some Simple Results)**
*   **곱셈과 0**: `a0 = 0a = 0` [Lemma 4.2.1(a)].
*   **음수 곱셈**: `a(-b) = (-a)b = -(ab)`, `(-a)(-b) = ab` [Lemma 4.2.1(b, c)].
*   **`(-1)a = -a`**: 단위원 `1`이 존재할 때 [Lemma 4.2.1(d)].
*   **이항식의 제곱**: `(a+b)² = a² + b² + ab + ba` [Lemma 4.2.2].
*   **부울 환 (Boolean Ring)**: 모든 `x ∈ R`에 대해 `x² = x`인 환.
    *   **성질**: 부울 환은 가환환이다 [Lemma 4.2.4].

**3.3. 아이디얼, 준동형사상, 몫환 (Ideals, Homomorphisms, and Quotient Rings)**
*   **환 준동형사상 (Ring Homomorphism)**: 두 환 `R`, `R'`에 대해 `φ: R → R'`가 다음을 만족할 때:
    *   `φ(a + b) = φ(a) + φ(b)`
    *   `φ(ab) = φ(a)φ(b)`
*   **아이디얼 (Ideal)**: `R`의 비어있지 않은 부분집합 `I`가 다음을 만족할 때:
    *   `(a) 덧셈에 대한 `R`의 부분군.
    *   `(b) `r ∈ R`, `a ∈ I`이면 `ra ∈ I`이고 `ar ∈ I` (곱셈에 대해 닫혀있음). (양쪽 아이디얼).
*   **환 준동형사상의 핵 (Kernel of Ring Homomorphism)**: `Ker φ = {x ∈ R | φ(x) = 0}`는 `R`의 아이디얼 [Lemma 4.3.1].
*   **몫환 (Quotient Ring)**: `K`가 `R`의 아이디얼일 때, 덧셈군 `R/K`는 `(a + K)(b + K) = ab + K`로 정의된 곱셈에 대해 환을 이룬다. `φ: R → R/K`를 `φ(a) = a + K`로 정의하면 `φ`는 `R`에서 `R/K`로의 전사 준동형사상이며 `Ker φ = K` [Theorem 4.3.2].
*   **환 동형 정리 (Ring Homomorphism Theorems)**: 군의 준동형 정리와 유사하게 성립.
    *   **제1 동형 정리 (First Isomorphism Theorem)**: `φ: R → R'`가 `R`에서 `R'`로의 전사 준동형사상이고 `K`가 `φ`의 핵이면 `R' ≅ R/K` [Theorem 4.3.3].
    *   **대응 정리 (Correspondence Theorem)**: `φ: R → R'`가 `R`에서 `R'`로의 전사 준동형사상이고 `K`가 `φ`의 핵일 때, `R'`의 아이디얼 `I'`와 `K`를 포함하는 `R`의 아이디얼 `I` 사이에 일대일 대응이 존재하며 `I/K ≅ I'` [Theorem 4.3.4].
    *   **제2 동형 정리 (Second Isomorphism Theorem)**: `A`가 환 `R`의 부분환이고 `I`가 `R`의 아이디얼이면 `A + I`는 `R`의 부분환이고 `I`는 `A + I`의 아이디얼이며 `(A + I)/I ≅ A/(A ∩ I)` [Theorem 4.3.5].
    *   **제3 동형 정리 (Third Isomorphism Theorem)**: `φ: R → R'`가 `R`에서 `R'`로의 전사 준동형사상이고 `K`가 `φ`의 핵일 때, `I'`가 `R'`의 아이디얼이고 `I = {a ∈ R | φ(a) ∈ I'}`이면 `R/I ≅ R'/I'`. 이는 `R/I ≅ (R/K)/(I/K)`와 동치 [Theorem 4.3.6].
*   **주 아이디얼 (Principal Ideal)**: 가환환 `R`에서 `a ∈ R`에 의해 생성된 아이디얼 `(a) = {xa | x ∈ R}`.

**3.4. 극대 아이디얼 (Maximal Ideals)**
*   **정의**: 환 `R`의 진(眞)아이디얼 `M`이 `M`을 포함하는 `R`의 유일한 아이디얼이 `M` 자신과 `R`뿐일 때 `M`을 극대 아이디얼이라 한다.
*   **성질**: `R`이 단위원을 갖는 가환환이고 `M`이 `R`의 아이디얼일 때:
    *   `R/M`이 체일 필요충분조건은 `M`이 극대 아이디얼이다 [Theorem 4.4.2, 4.4.3].
    *   `R`의 아이디얼이 `(0)`과 `R` 자신뿐이면 `R`은 체이다 [Lemma 4.4.1].

**3.5. 다항식 환 (Polynomial Rings)**
*   **다항식 환 (Polynomial Ring, F[x])**: 체 `F` 위의 `x`에 대한 모든 다항식의 집합.
    *   **성질**: `F[x]`는 단위원을 갖는 가환환이다 [Lemma 4.5.1].
*   **차수 (Degree, deg p(x))**: 다항식의 최고 차수 항의 지수.
    *   **곱셈 차수**: `deg(p(x)q(x)) = deg p(x) + deg q(x)` (p,q가 0이 아닐 때) [Lemma 4.5.2].
*   **정역**: `F[x]`는 정역이다 [Lemma 4.5.4].
*   **나눗셈 알고리즘 (Division Algorithm)**: `f(x), g(x) ∈ F[x]` (`g(x) ≠ 0`)일 때 `f(x) = q(x)g(x) + r(x)`인 `q(x), r(x) ∈ F[x]`가 존재하며 `r(x) = 0`이거나 `deg r(x) < deg g(x)` [Theorem 4.5.5].
*   **주 아이디얼 정역 (Principal Ideal Domain, PID)**: `F[x]`의 모든 아이디얼 `I`는 `I = (g(x))` (`g(x)`는 `I`에서 최소 차수를 갖는 다항식) 형태이다. 즉, `F[x]`는 PID이다 [Theorem 4.5.6].
    *   **모닉 다항식 (Monic Polynomial)**: 최고차항의 계수가 1인 다항식. (아이디얼의 모닉 생성원은 유일).
*   **최대공약수 (GCD)**: `f(x), g(x) ∈ F[x]`의 최대공약수 `d(x)`는 모닉 다항식이며 `d(x) | f(x)`, `d(x) | g(x)`이고, `h(x)`가 `f(x), g(x)`를 모두 나누면 `h(x) | d(x)`이다.
    *   **존재 및 형태**: `d(x) = a(x)f(x) + b(x)g(x)`인 `a(x), b(x) ∈ F[x]`가 존재 [Theorem 4.5.7].
*   **서로소 다항식 (Relatively Prime Polynomials)**: 최대공약수가 1인 다항식.
    *   **성질**: `f(x), g(x)`가 서로소일 필요충분조건은 `a(x)f(x) + b(x)g(x) = 1`인 `a(x), b(x) ∈ F[x]`가 존재 [Theorem 4.5.9].
*   **기약 다항식 (Irreducible Polynomial)**: `p(x) ∈ F[x]`가 양의 차수를 가지며, `f(x) ∈ F[x]`가 `p(x)`로 나누어지거나 `p(x)`와 `f(x)`가 서로소일 때. (즉, 양의 차수를 갖는 두 다항식의 곱으로 인수분해될 수 없는 다항식).
    *   **아이디얼과의 관계**: `(p(x))`가 `F[x]`의 극대 아이디얼일 필요충분조건은 `p(x)`가 `F[x]`에서 기약이다 [Theorem 4.5.11].
*   **유일 인수분해 정리 (Unique Factorization Theorem for Polynomials)**: 양의 차수를 갖는 모든 `f(x) ∈ F[x]`는 기약이거나 기약 다항식들의 곱으로 표현되며, 이 인수분해는 순서와 단위(leading coefficient)를 제외하면 유일하다 [Theorem 4.5.12].
*   **가우스 보조 정리 (Gauss' Lemma)**: `f(x) ∈ Z[x]`가 모닉 다항식이고 `f(x) = a(x)b(x)` (`a(x), b(x) ∈ Q[x]`)이면, `f(x) = a₁(x)b₁(x)`인 모닉 다항식 `a₁(x), b₁(x) ∈ Z[x]`가 존재하며 `deg a₁(x) = deg a(x)`, `deg b₁(x) = deg b(x)` [Theorem 4.6.3].
*   **아이젠슈타인 판정법 (Eisenstein Criterion)**: `f(x) = x^n + a₁x^(n-1) + ... + a_n`이 정수 계수를 갖는 상수 아닌 다항식일 때, 어떤 소수 `p`가 `a₁, a₂, ..., a_n`을 나누고 `p² <binary data, 1 bytes><binary data, 1 bytes> a_n`이면 `f(x)`는 `Q[x]`에서 기약이다 [Theorem 4.6.4].

**3.6. 정역의 몫체 (Field of Quotients of an Integral Domain)**
*   **정의 및 구성**: 정역 `D`가 주어지면, `D`의 원소 `a, b ≠ 0`에 대한 모든 분수 `a/b`로 구성된 체 `F`가 존재한다. 이 `F`를 `D`의 몫체라 한다 [Theorem 4.7.1].

#### **4. 체 이론 (Field Theory)**

**4.1. 체의 특성 (Characteristic of a Field)**
*   **특성 (Characteristic)**: 체 `F`의 특성 `p ≠ 0`는 `px = 0` (`p`는 양의 정수)를 모든 `x ∈ F`에 대해 만족하고, `p`보다 작은 양의 정수는 이 성질을 갖지 않을 때의 `p`를 의미. 이런 `p`가 없으면 특성은 `0`.
*   **성질**: 체 (또는 정역)의 특성은 `0`이거나 소수이다 [Theorem 5.1.1, Corollary].

**4.2. 벡터 공간 (Vector Spaces)**
*   **벡터 공간 (Vector Space)**: 체 `F` 위의 아벨 군 `V`에 대해, 각 `α ∈ F`와 `v ∈ V`에 대해 `αv ∈ V`가 정의되며 특정 공리들을 만족할 때. (예: `Fⁿ`, `F[x]`).
*   **부분 공간 (Subspace)**: 벡터 공간 `V`의 비어있지 않은 부분집합 `W`가 `W` 자체로 `F` 위의 벡터 공간을 이룰 때.
*   **선형 결합 (Linear Combination)**: `v = α₁v₁ + ... + α_nv_n` 형태.
*   **유한 차원 벡터 공간 (Finite Dimensional Vector Space)**: `V = <v₁, ..., v_n>`인 유한한 원소 집합으로 생성될 수 있을 때.
*   **선형 독립/종속 (Linearly Independent/Dependent)**: `α₁v₁ + ... + α_nv_n = 0`일 때 모든 `α_i = 0`이면 선형 독립. 아니면 선형 종속.
*   **기저 (Basis)**: `F` 위의 벡터 공간 `V`의 기저는 `V`를 생성하고 `F` 위에서 선형 독립인 원소들로 구성된 집합.
*   **차원 (Dimension, dim_F(V))**: 기저의 원소 개수 [Theorem 5.2.5].
    *   **성질**: `dim_F(V) = n`일 때 `m > n`이면 `V`의 임의의 `m`개 원소는 선형 종속이다 [Theorem 5.2.6].
    *   **성질**: `dim_F(V) = n`일 때 `V`의 임의의 `n`개 선형 독립 원소는 `V`의 기저를 이룬다 [Theorem 5.2.7].

**4.3. 체 확장 (Field Extensions)**
*   **체 확장 (Field Extension)**: `K`가 `F`를 부분체로 가질 때 `K`는 `F`의 확장체. `F ⊆ K`.
*   **유한 확장 (Finite Extension)**: `F` 위의 벡터 공간으로 볼 때 `dim_F(K)`가 유한할 때. `[K:F]`로 표기하고 `F` 위의 `K`의 **차수 (Degree)**라 함.
*   **차수의 곱셈 법칙 (Degree Multiplicativity)**: `L ⊇ K ⊇ F`인 세 체에 대해 `[L:F] = [L:K][K:F]` [Theorem 5.3.1].
    *   **코롤라이**: `[L:F]`가 유한이면 `[K:F]`도 유한이며 `[K:F]`는 `[L:F]`를 나눈다.
*   **대수적 원소 (Algebraic Element)**: `α ∈ K`가 `F` 위에서 `p(α) = 0`인 `p(x) ≠ 0 ∈ F[x]`를 만족할 때 `α`는 `F` 위에서 대수적.
    *   **성질**: `K`가 `F`의 유한 확장체이면, `K`의 모든 원소는 `F` 위에서 대수적이다 [Theorem 5.3.2].
*   **초월적 원소 (Transcendental Element)**: `F` 위에서 대수적이 아닌 `K`의 원소.
*   **대수적 수 (Algebraic Number)**: `Q` 위에서 대수적인 복소수. (대수적 수의 집합은 `C`의 부분체를 이룬다) [Theorem 5.4.2].
*   **최소 다항식 (Minimal Polynomial)**: `α`가 `F` 위에서 대수적일 때 `α`를 근으로 가지는 `F[x]`의 모닉 다항식 중 차수가 가장 낮은 다항식.
    *   **성질**: 최소 다항식은 `F[x]`에서 기약이다 [Lemma 5.3.4].
    *   **확장 차수**: `α`의 최소 다항식의 차수가 `n`이면 `[F(α):F] = n`. `F(α)`는 `F`와 `α`를 모두 포함하는 `K`의 가장 작은 부분체.
    *   **동형**: `F[x]/(p(x)) ≅ F(α)` (`p(x)`는 `α`의 최소 다항식).

**4.4. 작도 가능성 (Constructibility)**
*   **작도 가능 길이 (Constructible Length)**: 주어진 길이 `1`로부터 자와 컴퍼스만을 유한 번 사용하여 작도 가능한 음이 아닌 실수 길이.
*   **작도 가능 수 (Constructible Number)**: 절대값이 작도 가능 길이인 실수.
    *   **성질**: 작도 가능 수의 집합은 실수의 체의 부분체를 이룬다 [Theorem 5.5.1].
    *   **작도 가능성 판정 조건 (Criterion for Constructibility)**: 실수 `α`가 작도 가능하려면 `[Q(α):Q]`가 `2`의 거듭제곱이어야 한다. (즉, `α`의 `Q` 위에서의 최소 다항식의 차수가 `2`의 거듭제곱이어야 한다) [Theorem 5.5.2].
*   **큐브 배증 문제 (Duplicating the Cube)**: 체적 `1`의 큐브를 배증하는 것은 불가능하다. (즉, `b³ = 2`인 `b`를 작도하는 것은 불가능하다. `x³ - 2`는 `Q` 위에서 차수 3의 기약 다항식이므로) [Theorem 5.5.3].
*   **각의 삼등분 문제 (Trisecting an Angle)**: `60°`를 자와 컴퍼스로 삼등분하는 것은 불가능하다. (즉, `cos 20°`가 작도 불가능하다. `cos 20°`의 최소 다항식은 차수 3의 다항식이므로) [Theorem 5.5.4].

**4.5. 다항식의 근 (Roots of Polynomials)**
*   **근 (Root)**: `α ∈ K`가 `f(x) ∈ F[x]`의 근이라는 것은 `f(α) = 0`일 때.
*   **인수 정리 (Factor Theorem)**: `α ∈ L`가 `f(x) ∈ F[x]`의 근이면 `f(x)`는 `L[x]`에서 `(x - α)q(x)`로 인수분해된다 [Lemma 5.6.1].
*   **유한 체에서의 다항식 분해**: `q`개의 원소를 갖는 유한 체 `F`에서 `x^q - x`는 `x(x - α₁)...(x - α_{q-1})`로 인수분해된다. 여기서 `α₁, ..., α_{q-1}`는 `F`의 `0`이 아닌 원소들이다 [Theorem 5.6.4].
    *   **윌슨 정리 (Wilson's Theorem)**: `p`가 소수이면 `(p-1)! ≡ -1 mod p` [Corollary to Theorem 5.6.4].
*   **근을 포함하는 확장체 구성**: 체 `F`와 양의 차수 `n`을 갖는 `f(x) ∈ F[x]`가 주어지면, `f(x)`가 근을 갖는 `F`의 유한 확장체 `K`가 존재하며 `[K:F] ≤ n`이다 [Theorem 5.6.5].
*   **분해체 (Splitting Field)**: `n`차 다항식 `f(x) ∈ F[x]`가 주어지면, `f(x)`가 `n`개의 근을 갖는 (즉, 선형 인수로 분해되는) `F`의 확장체 `K`가 존재하며 `[K:F] ≤ n!`이다 [Theorem 5.6.6].

---

이 요약본은 주어진 자료의 모든 중요한 정의, 정리, 코롤라이를 망라하며, 각 개념이 어떤 문맥에서 사용되는지에 대한 간략한 설명을 포함합니다. 이 개념들을 숙지하시면 관련된 문제들을 해결하는 데 큰 도움이 될 것입니다.