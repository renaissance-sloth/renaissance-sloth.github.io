# 📘 Chapter 6 — Rectifiable Curves 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 앞의 벡터 적분을 기하에 적용한다. 연속 곡선의 길이를 polygonal approximation의 supremum으로 정의하고, continuously differentiable curve의 길이가
$$
\int_a^b |\gamma'(t)|dt
$$
라는 친숙한 공식으로 계산된다는 것을 증명한다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 6.26

$[a,b]\to\mathbb R^k$의 continuous mapping $\gamma$를 curve라고 한다. one-to-one이면 arc, $\gamma(a)=\gamma(b)$면 closed curve라고 한다.

partition $P=\{x_0,\dots,x_n\}$에 대해
$$
\Lambda(P,\gamma)=\sum_{i=1}^n |\gamma(x_i)-\gamma(x_{i-1})|
$$
를 정의하고,
$$
\Lambda(\gamma)=\sup_P \Lambda(P,\gamma)
$$
를 curve의 length로 정의한다. 이 supremum이 finite이면 rectifiable이라 한다.

### ▪ Theorem 6.27

$\gamma'$가 $[a,b]$에서 continuous이면 $\gamma$는 rectifiable이고
$$
\Lambda(\gamma)=\int_a^b |\gamma'(t)|dt.
$$

### ▪ Proof

한쪽 부등식은
$$
\gamma(x_i)-\gamma(x_{i-1})=\int_{x_{i-1}}^{x_i}\gamma'(t)dt
$$
와 Theorem 6.25로부터
$$
|\gamma(x_i)-\gamma(x_{i-1})|
\le \int_{x_{i-1}}^{x_i}|\gamma'(t)|dt
$$
를 얻고 모두 더하면 된다. 따라서
$$
\Lambda(\gamma)\le \int_a^b |\gamma'(t)|dt.
$$

반대 부등식은 $\gamma'$의 uniform continuity를 이용해 partition을 충분히 잘게 쪼개면 각 작은 구간에서 $|\gamma'|$의 적분이 chord length에 가깝도록 만든다. 합쳐서
$$
\int_a^b |\gamma'(t)|dt\le \Lambda(\gamma)+2\varepsilon(b-a)
$$
를 얻고 $\varepsilon\to0$를 보내면 된다.

---

## 🟢 3. 개념 해설 + 엄밀성

curve length를 바로 정의하지 않고 polygonal approximation의 supremum으로 정의하는 이유는 일반 continuous curve에는 속도 개념이 항상 주어지지 않기 때문이다. 하지만 derivative가 continuous하면 속도 $|\gamma'|$를 적분해 길이를 계산할 수 있다. 이 정리가 두 정의를 연결해 준다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 매끄러운 곡선의 길이를 계산할 때
- reparameterization invariance를 볼 때
- curve geometry를 적분으로 바꿀 때

### 📌 문제 풀이 패턴
1. polygonal length 정의
2. 벡터 FTC와 norm inequality로 upper bound
3. derivative의 uniform continuity로 reverse estimate

---

## 🔴 5. 대표 문제 & 풀이 전략

- Exercise 19는 곡선의 reparameterization이 arc/closed/rectifiable 성질과 길이를 보존함을 묻는다. 이 절의 정의와 정리를 정확히 써야 한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 6.26 포함
- [x] Theorem 6.27 포함
- [x] 길이 공식 설명 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- curve length를 왜 supremum으로 정의하는가?
- continuously differentiable curve에서 길이가 $\int|\gamma'|$가 되는 이유를 설명하라.
- 왜 uniform continuity가 reverse inequality에서 중요한가?
