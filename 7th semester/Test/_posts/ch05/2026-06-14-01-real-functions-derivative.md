# 📘 Chapter 5 — Real Function Derivative 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 미분의 가장 기본적인 출발점이다.

- difference quotient로 derivative를 정의한다.
- differentiable이면 continuous라는 사실을 증명한다.
- 합, 곱, 몫의 미분법을 정리한다.
- chain rule을 증명한다.
- 미분 가능하지만 도함수가 연속일 필요는 없다는 예시를 본다.

즉 이 절은 “미분이 무엇이고, 어떻게 계산하며, 어디서 조심해야 하는가”를 한 번에 세운다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 5.1

$[a,b]$에 정의된 real-valued function $f$와 $x\in[a,b]$에 대해
$$
\phi(t)=\frac{f(t)-f(x)}{t-x}
\qquad (a<t<b,\ t\ne x)
$$
를 만들고,
$$
f'(x)=\lim_{t\to x}\phi(t)
$$
가 존재하면 이를 $f$의 derivative라고 한다.

이 limit가 존재하면 $f$는 $x$에서 differentiable하다고 한다. endpoint에서는 one-sided derivative를 생각할 수 있다.

### ▪ Theorem 5.2

$f$가 $x\in[a,b]$에서 differentiable이면 $f$는 $x$에서 continuous이다.

### ▪ Proof

$$
f(t)-f(x)=\frac{f(t)-f(x)}{t-x}(t-x).
$$
$t\to x$일 때 첫 인수는 $f'(x)$로, 둘째 인수는 0으로 가므로 전체가 0으로 간다. 따라서 $f(t)\to f(x)$, 즉 연속이다.

### ▪ Theorem 5.3

$f,g$가 $x$에서 differentiable이면

1. $(f+g)'(x)=f'(x)+g'(x)$
2. $(fg)'(x)=f'(x)g(x)+f(x)g'(x)$
3. $g(x)\ne0$이면
   $$
   \left(\frac fg\right)'(x)=\frac{g(x)f'(x)-g'(x)f(x)}{g(x)^2}.
   $$

### ▪ Proof

(1)은 limit law로 바로 나온다. (2)는
$$
h(t)-h(x)=f(t)(g(t)-g(x))+g(x)(f(t)-f(x))
$$
를 $t-x$로 나누고 $t\to x$를 보내면 된다. (3)도 quotient difference를 전개한 뒤 같은 방식으로 처리한다.

### ▪ Example 5.4

- constant의 derivative는 0
- identity function의 derivative는 1
- 반복 적용으로 $x^n$의 미분법 $nx^{n-1}$
- 따라서 polynomial과 denominator가 0이 아닌 rational function은 differentiable

### ▪ Theorem 5.5 — Chain rule

$f$가 $[a,b]$에서 continuous이고 $x$에서 differentiable, $g$가 $f(x)$에서 differentiable이라 하자. $h(t)=g(f(t))$이면
$$
h'(x)=g'(f(x))f'(x).
$$

### ▪ Proof

$y=f(x)$라 두고
$$
f(t)-f(x)=(t-x)[f'(x)+u(t)],
$$
$$
g(s)-g(y)=(s-y)[g'(y)+v(s)]
$$
로 쓴다. 여기서 $u(t)\to0$, $v(s)\to0$. 이제 $s=f(t)$를 대입하면
$$
h(t)-h(x)=(t-x)[f'(x)+u(t)][g'(y)+v(s)].
$$
따라서
$$
\frac{h(t)-h(x)}{t-x}=[f'(x)+u(t)][g'(y)+v(s)]
$$
이고, $t\to x$이면 $s=f(t)\to y$이므로 우변은 $g'(y)f'(x)$로 간다.

### ▪ Examples 5.6

1. $f(x)=x\sin(1/x)$ for $x\ne0$, $f(0)=0$: $x\ne0$에서는 미분 가능하지만 0에서는 derivative가 존재하지 않는다.
2. $f(x)=x^2\sin(1/x)$ for $x\ne0$, $f(0)=0$: 모든 점에서 differentiable이지만 $f'$는 0에서 continuous가 아니다.

---

## 🟢 3. 개념 해설 + 엄밀성

derivative는 “순간변화율”이라는 직관으로 설명되지만, Rudin에서는 끝까지 quotient의 limit로 다룬다. 중요한 것은 differentiability가 continuity보다 훨씬 강하다는 점, 그리고 chain rule이 composite structure를 풀어 주는 핵심 도구라는 점이다.

또 예제 5.6은 “미분 가능 ⇒ 도함수 연속”이 거짓이라는 사실을 초반에 분명히 박아 준다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- derivative의 존재를 정의로 직접 판정할 때
- algebraic differentiation rules로 계산할 때
- composite function의 derivative를 구할 때
- 0 근처 특이한 함수의 differentiability를 판정할 때

### 📌 문제 풀이 패턴
1. 정의형 quotient 직접 계산
2. product/quotient rule 적용
3. chain rule로 composite 해체
4. 0 근처에서는 정의로 되돌아가기

---

## 🔴 5. 대표 문제 & 풀이 전략

### 직접 연결 exercise

- Exercise 1, 2, 3: derivative와 mean value theorem 초입 응용
- Exercise 11, 12: higher derivative 존재 여부와 quotient/definition 기술

이 절을 제대로 이해하면 “정의로 직접 증명할지, 정리로 밀고 갈지” 판단이 쉬워진다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 5.1 포함
- [x] Theorems 5.2, 5.3 포함
- [x] Theorem 5.5 포함
- [x] Examples 5.6 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 differentiability는 continuity를 함의하는가?
- chain rule 증명에서 왜 $f$의 continuity가 필요한가?
- Example 5.6(b)가 무엇을 반례로 보여 주는가?
