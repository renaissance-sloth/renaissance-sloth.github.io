# 📘 Chapter 7 — Discussion of Main Problem 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 Chapter 7 전체의 질문을 던진다.

> 함수열이나 함수급수의 limit를 취할 때, continuity / differentiability / integrability 같은 좋은 성질이 보존되는가?

Rudin은 먼저 pointwise convergence를 정의한 뒤, limit process를 함부로 교환하면 무엇이 깨지는지 여러 반례로 보여 준다. 이 절은 “왜 uniform convergence가 필요한가”를 동기부여하는 절이다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 7.1

집합 $E$ 위 함수열 $\{f_n\}$에 대해 각 $x\in E$에서 숫자열 $f_n(x)$가 수렴하면
$$
f(x)=\lim_{n\to\infty}f_n(x)
\qquad (x\in E)
$$
로 정의되는 함수 $f$를 limit function이라 한다. 이때 $f_n\to f$ pointwise on $E$라고 한다.

함수급수 $\sum f_n(x)$가 각 $x$에서 수렴하면
$$
f(x)=\sum_{n=1}^{\infty} f_n(x)
$$
를 그 sum이라 한다.

### ▪ Main problem

연속함수열의 pointwise limit가 continuous인가? 미분 가능한 함수열의 limit는 differentiable인가? 적분과 limit를 바꿔도 되는가? 즉
$$
\lim_{t\to x}\lim_{n\to\infty}f_n(t)
\stackrel{?}=\lim_{n\to\infty}\lim_{t\to x}f_n(t)
$$
같은 교환이 가능한가가 핵심 질문이다.

### ▪ Examples 7.2–7.6

1. **double sequence example**: 반복 limit의 순서를 바꾸면 값이 달라질 수 있다.
2. **continuous functions with discontinuous sum**: pointwise convergent series of continuous functions may have discontinuous sum.
3. **everywhere discontinuous limit**: rational/irrational type limit function이 생길 수 있다.
4. **derivatives do not pass to limit**: $f_n\to0$인데 $f_n'$는 $0$으로 가지지 않을 수 있다.
5. **integral and limit fail to commute**: pointwise limit와 integral의 교환이 실패할 수 있다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 핵심은 “pointwise convergence는 너무 약하다”는 것이다. 각 점에서 따로따로 수렴하는 것만으로는 함수 전체의 좋은 성질이 유지되지 않는다. 반례들이 Chapter 7 전체를 정당화한다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- pointwise convergence와 uniform convergence를 구분해야 할 때
- 반례를 통해 왜 stronger hypothesis가 필요한지 설명할 때
- continuity/differentiability/integration interchange 문제를 이해할 때

### 📌 문제 풀이 패턴
1. pointwise limit 먼저 계산
2. 좋은 성질이 실제로 보존되는지 separately 검사
3. 실패하면 counterexample structure를 분석

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 3, 5, 7은 이 절의 반례 구조를 직접 반영한다.
- 이후 uniform convergence 절의 정리들은 모두 “이 절에서 망가진 것을 어떻게 복구할까?”에 대한 답이다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 7.1 포함
- [x] main problem 설명 포함
- [x] Examples 7.2–7.6 요지 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- pointwise convergence와 uniform convergence의 차이를 말해 보라.
- 왜 continuous function의 limit가 discontinuous가 될 수 있는가?
- 왜 integral과 limit를 바꾸는 데 추가 조건이 필요한가?
