# 📘 Chapter 4 — Infinite Limits and Limits at Infinity 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 limit 개념을 extended real line까지 확장한다.

- $+\infty$, $-\infty$의 neighborhood를 정의한다.
- 함수가 무한대로 간다, 혹은 무한대에서 어떤 limit를 가진다는 말을 통일적으로 정의한다.
- limit algebra도 가능한 범위에서는 그대로 유지된다.

이 절은 뒤에서 improper integral, asymptotic behavior, singularity analysis에 바로 연결된다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 4.32

모든 실수 $c$에 대해
$$
(c,+\infty)
$$
를 $+\infty$의 neighborhood라 하고,
$$
(-\infty,c)
$$
를 $-\infty$의 neighborhood라 한다.

### ▪ Definition 4.33

$f$가 $E\subset\mathbb R$에 정의된 real function이라 하자. $A$와 $x$를 extended real number system의 원소라 하자. 이때
$$
f(t)\to A\quad\text{as }t\to x
$$
라는 것은, $A$의 every neighborhood $U$에 대해 $x$의 어떤 neighborhood $V$가 존재하여, $V\cap E$가 empty가 아니고, 모든
$$
t\in V\cap E,\quad t\ne x
$$
에 대해
$$
f(t)\in U
$$
가 성립하는 것을 말한다.

$A$와 $x$가 ordinary real numbers인 경우 이것은 Definition 4.1과 일치한다.

### ▪ Theorem 4.34

$f(t)\to A$, $g(t)\to B$ as $t\to x$라 하자. 그러면 정의되는 경우에

1. $f(t)\to A'$이면 $A'=A$
2. $(f+g)(t)\to A+B$
3. $(fg)(t)\to AB$
4. $(f/g)(t)\to A/B$

단, $\infty-\infty$, $0\cdot\infty$, $\infty/\infty$, $A/0$ 같은 정의되지 않은 형식은 제외한다.

### ▪ Proof idea

이것은 ordinary finite-limit algebra의 extended-real analogue이다. 본문 말대로 proof는 essentially 새로운 내용을 주지 않는다. 다만 연산이 정의되지 않는 경우를 조심해야 한다.

---

## 🟢 3. 개념 해설 + 엄밀성

이 절의 중요한 철학은 “무한대도 neighborhood language로 다룰 수 있다”는 점이다. 그러면 finite limit, infinite limit, limits at infinity를 하나의 통일된 틀 안에서 서술할 수 있다.

예를 들어
$$
f(t)\to +\infty\quad (t\to x)
$$
는 “충분히 $x$ 가까이 가면 함수값이 임의로 큰 오른쪽 반직선 안에 들어간다”는 말일 뿐이다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- vertical asymptote / horizontal asymptote를 다룰 때
- improper integrals와 연결되는 극한을 해석할 때
- extended real arithmetic로 function behavior를 통일해 쓰고 싶을 때

### 📌 문제 풀이 패턴
1. target $A$가 finite인지 infinite인지 확인
2. 그에 맞는 neighborhood를 잡음
3. 입력 쪽 $x$ neighborhood를 제어
4. 연산은 Theorem 4.34에서 정의되는 경우만 사용

---

## 🔴 5. 대표 문제 & 풀이 전략

이 절은 Chapter 4 exercise 중 직접 지정된 문항과 1:1 대응되진 않지만, 이후 improper integral과 asymptotic analysis를 읽을 때 필수 배경이다. 특히 “무한대에서의 limit”를 ordinary limit와 같은 문법으로 다루는 감각이 중요하다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 4.32 포함
- [x] Definition 4.33 포함
- [x] Theorem 4.34 포함
- [x] extended real viewpoint 설명 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- $+\infty$의 neighborhood를 왜 $(c,+\infty)$로 정의하는가?
- infinite limit를 ordinary limit와 같은 틀로 다루는 장점은 무엇인가?
- Theorem 4.34에서 왜 $\infty-\infty$ 같은 형식을 제외해야 하는가?
