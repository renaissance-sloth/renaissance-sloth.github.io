# 📘 Chapter 5 — Derivatives of Higher Order 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 derivative를 한 번 더, 또 한 번 더 취하는 higher-order derivative의 언어를 도입한다. 뒤의 Taylor theorem과 Exercise 11, 12가 바로 여기에 기대고 있다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 5.14

$f$가 interval에서 derivative $f'$를 가지고, $f'$가 다시 differentiable이면 그 derivative를 $f''$라 쓴다. 이렇게 계속해서
$$
f,f',f'',f^{(3)},\dots,f^{(n)}
$$
를 정의한다. $f^{(n)}$를 $n$-th derivative 또는 derivative of order $n$이라고 한다.

$f^{(n)}(x)$가 존재하려면 단지 한 점에서만이 아니라 그 주변에서 lower-order derivatives가 먼저 존재해야 한다는 점을 강조한다.

---

## 🟢 3. 개념 해설 + 엄밀성

higher derivative는 단순히 notation이 아니라 regularity hierarchy다.

- $f'$ exists: 접선 기울기 존재
- $f''$ exists: 기울기 변화율 존재
- higher derivatives: local polynomial approximation의 정밀도 상승

한 점에서만 derivative를 묻는 것과 달리, higher derivative는 주변 정보까지 요구한다는 점이 중요하다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- Taylor expansion을 준비할 때
- convexity와 second derivative를 연결할 때
- second difference quotient를 해석할 때

### 📌 문제 풀이 패턴
1. lower-order derivative부터 차례대로 존재 확인
2. 0 근처 특이점은 definition으로 직접 점검
3. higher derivative existence와 continuity를 분리해서 생각

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 11: second derivative와 symmetric difference quotient
- Exercise 12: $|x|^3$의 higher derivative 존재 여부
- Exercise 14: convexity와 $f'$, $f''$ 관계

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 5.14 포함
- [x] higher derivative 존재 조건 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- $f''(x)$가 존재한다는 말은 정확히 무엇을 뜻하는가?
- 왜 higher derivative는 주변 정보가 필요한가?
- $|x|^3$에서 어디까지 미분 가능한지 스스로 점검해 보라.
