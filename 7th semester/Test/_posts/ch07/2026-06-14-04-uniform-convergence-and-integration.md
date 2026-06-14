# 📘 Chapter 7 — Uniform Convergence and Integration 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 uniform convergence가 적분과 limit를 안전하게 교환하게 해 준다는 사실을 정리한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 7.16

$\alpha$ increasing on $[a,b]$, 각 $f_n\in\mathscr R(\alpha)$, 그리고 $f_n\to f$ uniformly on $[a,b]$라 하자. 그러면 $f\in\mathscr R(\alpha)$이고
$$
\int_a^b f\,d\alpha = \lim_{n\to\infty}\int_a^b f_n\,d\alpha.
$$

따라서 uniformly convergent series는 term-by-term integration이 가능하다.

### ▪ Proof idea

$\varepsilon_n=\sup |f_n-f|\to0$를 두면
$$
f_n-\varepsilon_n\le f\le f_n+\varepsilon_n.
$$
이것을 upper/lower integrals와 integral estimate에 넣으면 integrability와 limit 교환이 동시에 나온다.

---

## 🟢 3. 개념 해설 + 엄밀성

pointwise convergence는 integral과 limit를 바꾸기에 너무 약했지만, uniform convergence는 전체 구간에서 오차를 한 번에 제어하므로 적분 후 오차도 쉽게 제어된다. 적분은 평균적 연산이라 uniform control과 잘 맞는다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- limit와 적분을 교환하고 싶을 때
- 함수급수를 항별 적분하고 싶을 때
- improper integral의 dominated/uniform approximation의 첫 단계로 쓸 때

### 📌 문제 풀이 패턴
1. uniform error $\varepsilon_n$ 도입
2. 적분 estimate로 차이를 바로 눌러줌
3. series면 partial sums에 Theorem 7.16 적용

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 12는 이 절의 improper integral version처럼 읽으면 된다.
- Exercise 5도 왜 absolute convergence alone으로는 uniform convergence가 안 되는지 비교하는 좋은 예다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 7.16 포함
- [x] term-by-term integration 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 uniform convergence는 적분과 limit 교환을 가능하게 하는가?
- partial sums에 Theorem 7.16을 적용하면 어떤 결론이 나오는가?
- pointwise convergence만으로는 왜 부족한가?
