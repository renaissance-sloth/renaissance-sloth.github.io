# 📘 Chapter 7 — Equicontinuous Families of Functions 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 함수열의 compactness 비슷한 성질을 얻기 위한 조건을 다룬다.

- pointwise bounded / uniformly bounded 정의
- pointwise convergent subsequence를 뽑는 diagonal process
- equicontinuity 정의
- equicontinuity + pointwise boundedness + compactness로 uniformly convergent subsequence를 얻는다

이 절은 Arzelà–Ascoli의 원형이다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 7.19

함수열 $\{f_n\}$이 $E$에서 pointwise bounded라는 것은 각 $x\in E$마다 숫자열 $f_n(x)$이 bounded라는 뜻이다. uniformly bounded라는 것은 하나의 상수 $M$로
$$
|f_n(x)|<M
\qquad (x\in E,\ n\ge1)
$$
가 성립하는 것이다.

### ▪ Examples 7.20, 7.21

- uniformly bounded continuous functions의 sequence라도 pointwise convergent subsequence가 없을 수 있다.
- uniformly bounded sequence라도 uniformly convergent subsequence가 없을 수 있다.

### ▪ Definition 7.22 — Equicontinuity

함수족 $\mathscr F$가 $E$에서 equicontinuous라는 것은, 모든 $\varepsilon>0$에 대해 어떤 $\delta>0$가 존재하여
$$
d(x,y)<\delta
\implies
|f(x)-f(y)|<\varepsilon
$$
가 모든 $f\in\mathscr F$와 모든 $x,y\in E$에 대해 동시에 성립하는 것이다.

### ▪ Theorem 7.23

$E$가 countable이고 $\{f_n\}$이 pointwise bounded이면, 모든 $x\in E$에서 convergent한 subsequence를 하나 뽑을 수 있다.

### ▪ Proof idea

점들을 $x_1,x_2,\dots$로 나열하고, 첫 점에서 수렴하는 subsequence를 뽑고, 그 subsequence 안에서 두 번째 점에서 수렴하는 subsequence를 다시 뽑는 diagonal process를 수행한다.

### ▪ Theorem 7.24

$K$ compact, $f_n\in\mathscr C(K)$, 그리고 $f_n\to f$ uniformly이면 $\{f_n\}$은 equicontinuous이다.

### ▪ Theorem 7.25

$K$ compact, $f_n\in\mathscr C(K)$, $\{f_n\}$ pointwise bounded, equicontinuous라 하자. 그러면

1. $\{f_n\}$은 uniformly bounded이고
2. $\{f_n\}$은 uniformly convergent subsequence를 가진다.

### ▪ Proof idea

compactness로 유한한 $\delta$-net을 잡고, 그 점들에서의 boundedness를 whole space boundedness로 퍼뜨린다. dense countable subset에서 diagonal process로 pointwise convergent subsequence를 뽑고, equicontinuity를 이용해 이를 uniform convergence로 업그레이드한다.

---

## 🟢 3. 개념 해설 + 엄밀성

equicontinuity는 “모든 함수가 같은 $\delta$로 연속적이다”라는 uniform version of continuity다. 함수열 compactness의 핵심은 pointwise control만으로는 부족하고, oscillation control이 함께 필요하다는 데 있다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- subsequence extraction이 필요할 때
- pointwise convergence를 uniform convergence로 강화하고 싶을 때
- compact domain에서 함수열 compactness를 다룰 때

### 📌 문제 풀이 패턴
1. dense countable subset 선택
2. diagonal subsequence 추출
3. equicontinuity로 whole compact set에 퍼뜨림

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 15, 16, 18은 이 절과 매우 직접 연결된다.
- 특히 Exercise 16은 사실상 Theorem 7.25의 압축된 버전처럼 읽힌다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definitions 7.19, 7.22 포함
- [x] Theorems 7.23–7.25 포함
- [x] examples 요지 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- pointwise bounded와 uniformly bounded의 차이는 무엇인가?
- diagonal process는 어떻게 작동하는가?
- equicontinuity가 없으면 왜 uniform subsequence를 기대하기 어려운가?
