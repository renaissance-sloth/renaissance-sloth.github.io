# 📘 Chapter 7 — The Stone–Weierstrass Theorem 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 함수근사의 정점이다.

- Weierstrass polynomial approximation theorem
- algebra, uniform closure, point-separating family 개념
- Stone–Weierstrass theorem의 real version
- self-adjoint complex version

즉 “어떤 함수족이 모든 연속함수를 균등근사할 수 있는가?”에 대한 구조적 답을 준다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 7.26 — Weierstrass theorem

$[a,b]$의 모든 continuous complex function은 polynomial sequence에 의해 uniformly approximated될 수 있다. real-valued function이면 real polynomial로 가능하다.

### ▪ Proof idea

본문은 kernel
$$
Q_n(x)=c_n(1-x^2)^n
$$
를 사용해 convolution-type polynomial
$$
P_n(x)=\int_{-1}^1 f(x+t)Q_n(t)dt
$$
를 만들고, 이것이 uniformly $f$로 가는 것을 보인다.

### ▪ Corollary 7.27

$|x|$는 compact interval 위에서 polynomial들로 uniformly approximate된다.

### ▪ Definition 7.28

함수족 $\mathscr A$가 algebra라는 것은 addition, multiplication, scalar multiplication에 대해 닫혀 있다는 뜻이다. uniformly closed의 개념과 uniform closure도 정의한다.

### ▪ Theorem 7.29

bounded function algebra의 uniform closure는 uniformly closed algebra이다.

### ▪ Definition 7.30

$\mathscr A$가 points를 separate한다는 것은 서로 다른 두 점을 구별하는 함수가 항상 존재한다는 뜻이다. 또 no point of vanishing은 각 점에서 0이 아닌 값을 가지는 함수가 하나쯤 있다는 뜻이다.

### ▪ Theorem 7.31

point-separating, nowhere-vanishing algebra는 두 점에서 임의로 지정한 두 값을 동시에 맞추는 함수를 포함한다.

### ▪ Theorem 7.32 — Stone–Weierstrass (real case)

$K$ compact, $\mathscr A$ real continuous functions의 algebra, $\mathscr A$가 points를 separate하고 no point of vanishing이면, $\mathscr A$의 uniform closure는 $K$ 위의 모든 real continuous functions이다.

### ▪ Proof structure

1. uniform closure는 절댓값에 대해 닫힘
2. 따라서 max/min에 대해 닫힘
3. 한 점에서 함수값을 맞추면서 아래에서 근사하는 함수 $g_x$ 구성
4. compactness로 finite subcover를 뽑아 전체에서 $\varepsilon$-근사하는 함수 구성

### ▪ Theorem 7.33 — Complex version

complex continuous functions의 self-adjoint algebra $\mathscr A$가 compact set $K$에서 points를 separate하고 nowhere vanishing이면, $\mathscr A$는 $\mathscr C(K)$에서 dense이다.

---

## 🟢 3. 개념 해설 + 엄밀성

Stone–Weierstrass는 “대수적 구조 + 점 분리 능력 + compactness”만 있으면 모든 연속함수를 균등근사할 수 있다고 말한다. 이는 단순한 polynomial theorem을 아주 강력한 구조정리로 일반화한 것이다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 특정 함수족이 dense인지 보일 때
- polynomial/trigonometric polynomial approximation을 정당화할 때
- later Fourier analysis, approximation theory의 기초로 쓸 때

### 📌 문제 풀이 패턴
1. algebra 확인
2. points separate 확인
3. nowhere vanishing 확인
4. Stone–Weierstrass 적용

---

## 🔴 5. 대표 문제 & 풀이 전략

- Chapter 8 Fourier series approximation과도 연결된다.
- Exercise 15, 16과 직접 연결되지는 않지만 Chapter 7의 철학적 climax를 제공한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorems 7.26, 7.27 포함
- [x] Definitions 7.28, 7.30 포함
- [x] Theorems 7.29, 7.31, 7.32, 7.33 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- algebra와 uniform closure의 뜻을 설명하라.
- point separation이 왜 핵심 조건인가?
- Stone–Weierstrass가 Weierstrass theorem을 어떻게 일반화하는가?
