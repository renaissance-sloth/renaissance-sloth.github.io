# 📘 Chapter 5 — Differentiation of Vector-Valued Functions 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 지금까지의 scalar differentiation을 complex-valued 및 $\mathbb R^k$-valued function으로 넓힌다.

- componentwise differentiation이 가능함을 본다.
- scalar 경우의 product-type rules 일부가 유지됨을 본다.
- mean value theorem과 L'Hospital rule은 그대로 가지 않음을 예제로 확인한다.
- 대신 vector-valued에서도 참인 약한 형태의 estimate를 얻는다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Remarks 5.16

- complex-valued function에는 Definition 5.1이 그대로 적용된다.
- $f=f_1+if_2$이면
  $$
  f'(x)=f_1'(x)+if_2'(x).
  $$
- $f:[a,b]\to\mathbb R^k$일 때도
  $$
  \lim_{t\to x}\left|\frac{f(t)-f(x)}{t-x}-f'(x)\right|=0
  $$
  로 derivative를 정의한다.
- componentwise로
  $$
  f'=(f_1',\dots,f_k')
  $$
  가 된다.

### ▪ Examples 5.17, 5.18

- complex-valued function에서는 ordinary mean value theorem이 그대로 성립하지 않는다.
- complex-valued function에서는 L'Hospital's rule도 실패할 수 있다.

### ▪ Theorem 5.19

$f:[a,b]\to\mathbb R^k$가 continuous이고 $(a,b)$에서 differentiable이면, 어떤 $x\in(a,b)$가 존재하여
$$
|f(b)-f(a)|\le (b-a)|f'(x)|.
$$

### ▪ Proof

$z=f(b)-f(a)$라 두고
$$
\phi(t)=z\cdot f(t)
$$
를 정의하면 real-valued function이 된다. mean value theorem을 $\phi$에 적용하면
$$
\phi(b)-\phi(a)=(b-a)\phi'(x)=(b-a)z\cdot f'(x)
$$
이고, 한편
$$
\phi(b)-\phi(a)=z\cdot z=|z|^2.
$$
Schwarz inequality로
$$
|z|^2\le (b-a)|z||f'(x)|
$$
이므로
$$
|z|\le (b-a)|f'(x)|.
$$

---

## 🟢 3. 개념 해설 + 엄밀성

벡터값 함수는 componentwise로 꽤 많은 것이 유지된다. 하지만 “실수축의 순서구조”에 의존하는 mean value theorem류는 그대로 남지 않는다. 그래서 Rudin은 counterexample을 먼저 보여 준 뒤, 대신 살아남는 estimate형 정리를 제시한다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- complex/$\mathbb R^k$-valued path의 derivative를 계산할 때
- componentwise regularity를 쓸 때
- vector-valued function에 대한 mean-value-type bound가 필요할 때

### 📌 문제 풀이 패턴
1. component로 쪼개기
2. scalar theorem이 그대로 가는지 여부 점검
3. 안 가면 estimate형 정리로 대체

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 10은 complex-valued 함수에서 limit 비율을 다루므로 이 절의 경고가 중요하다.
- Exercise 20은 Taylor inequality의 vector-valued analogue를 묻는다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Remarks 5.16 포함
- [x] Examples 5.17, 5.18 포함
- [x] Theorem 5.19 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- vector-valued derivative가 componentwise derivative와 어떻게 연결되는가?
- 왜 ordinary MVT가 complex-valued case에서 실패하는가?
- Theorem 5.19는 ordinary MVT의 어떤 약한 대체물인가?
