# 📘 Chapter 3 — Upper and Lower Limits 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절은 “수열이 수렴하지 않을 때도 끝부분의 거동을 어떻게 정량화할 것인가?”를 다룬다.

- 먼저 $+\infty$, $-\infty$로 간다는 뜻을 정의한다.
- 그다음 모든 **subsequential limit**를 한데 모아, 그 집합의 supremum/infimum을
  $$
  \limsup s_n,\qquad \liminf s_n
  $$
  로 정의한다.
- 이후 $\limsup$와 $\liminf$의 핵심 성질을 정리한다.

핵심 메시지는 다음이다.

> 수렴하지 않는 수열도 “가장 위에서 반복해서 접근하는 값”과 “가장 아래에서 반복해서 접근하는 값”을 가질 수 있다.

이 절을 이해하면 oscillation, subsequence argument, series의 root/ratio test의 논리까지 훨씬 자연스럽게 읽힌다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 3.15

실수수열 $\{s_n\}$에 대해 다음을 정의한다.

- 모든 실수 $M$에 대해, 어떤 $N$이 존재하여 $n\ge N$이면
  $$
  s_n\ge M
  $$
  이면
  $$
  s_n\to +\infty.
  $$

- 모든 실수 $M$에 대해, 어떤 $N$이 존재하여 $n\ge N$이면
  $$
  s_n\le M
  $$
  이면
  $$
  s_n\to -\infty.
  $$

여기서 $\to$ 기호를 사용하지만, Definition 3.1의 “수렴” 정의 자체를 바꾸는 것은 아니다. 단지 특정한 발산 형태를 추가 표기하는 것이다.

### ▪ Definition 3.16

실수수열 $\{s_n\}$의 어떤 subsequence가 extended real line에서 $x$로 수렴하면, 그런 숫자 $x$들의 집합을 $E$라고 하자. 즉 $E$는 모든 subsequential limit들과, 필요하면 $+\infty, -\infty$도 포함한다.

이제
$$
s^*=\sup E,
\qquad
s_*=\inf E
$$
로 두고,
$$
\limsup_{n\to\infty}s_n=s^*,
\qquad
\liminf_{n\to\infty}s_n=s_*
$$
로 정의한다.

### ▪ Theorem 3.17

$\{s_n\}$을 실수수열이라 하고, 위 정의에서의 $E$와 $s^*$를 생각하자. 그러면 $s^*$는 다음 두 성질을 가진다.

1. $s^*\in E$.
2. $x>s^*$이면, 어떤 $N$이 존재하여 $n\ge N$이면
   $$
   s_n<x.
   $$

또한 $s^*$는 이 두 성질을 갖는 유일한 수이다.

물론 $s_*$에 대해서도 대칭적인 결과가 성립한다.

### ▪ Proof

세 경우로 나누어 생각한다.

**(i) $s^*=+\infty$**  
그러면 $E$가 위로 bounded가 아니므로, subsequential limit들이 arbitrarily large하다. 따라서 어떤 subsequence는 $+\infty$로 가고, hence $+\infty\in E$.

**(ii) $s^*$가 유한한 실수**  
이 경우 $E$는 위로 bounded이고, Theorem 3.7에 의해 subsequential limit 집합은 closed이다. 따라서 집합 $E$의 supremum은 다시 $E$ 안에 속한다. 즉 $s^*\in E$.

**(iii) $s^*=-\infty$**  
그러면 $E$는 $-\infty$ 하나만 가진다. 즉 어떤 실수 $M$보다 큰 값으로 가는 subsequence가 존재할 수 없다. 따라서 결국 모든 충분히 큰 $n$에 대해 $s_n\le M$, 즉 $s_n\to-\infty$. 따라서 역시 $s^*\in E$.

이제 (2)를 보이자. 만약 $x>s^*$인데도 $s_n\ge x$인 항이 무한히 많다면, 그 항들만 뽑아 어떤 subsequence를 만들 수 있다. 그러면 그 subsequence는 어떤 subsequential limit $y\ge x>s^*$를 만들어야 하므로 $s^*=\sup E$와 모순이다. 따라서 충분히 뒤로 가면 항상 $s_n<x$이다.

유일성은 간단하다. 만약 $p<q$이고 둘 다 (1), (2)를 만족한다고 하자. 중간값 $x$를 잡아 $p<x<q$라 하자. 그러면 $p$의 성질 (2)에 의해 충분히 큰 $n$에 대해 $s_n<x$이다. 그런데 그러면 $q$는 성질 (1), 즉 $q$로 가는 subsequence가 존재한다는 것을 만족할 수 없다. 모순. 따라서 유일하다.

### ▪ Examples 3.18

1. 모든 유리수를 다 포함하는 sequence를 생각하면, 모든 실수가 subsequential limit가 되므로
   $$
   \limsup s_n=+\infty,
   \qquad
   \liminf s_n=-\infty.
   $$

2. $s_n=(-1)^n/[1+(1/n)]$이면,
   $$
   \limsup s_n=1,
   \qquad
   \liminf s_n=-1.
   $$

3. 실수수열 $\{s_n\}$이 $s$로 수렴할 필요충분조건은
   $$
   \limsup s_n=\liminf s_n=s.
   $$

### ▪ Theorem 3.19

어떤 고정된 $N$에 대해 $n\ge N$이면 $s_n\le t_n$라 하자. 그러면
$$
\liminf s_n\le \liminf t_n,
\qquad
\limsup s_n\le \limsup t_n.
$$

### ▪ Proof

뒤쪽 꼬리에서 항상 $s_n\le t_n$이므로, subsequential limits도 ordering을 깨뜨릴 수 없다. 따라서 하한극한과 상한극한에도 같은 순서가 전달된다. 증명 자체는 거의 정의를 바로 쓰면 끝나는 수준이다.

---

## 🟢 3. 개념 해설 + 엄밀성

### $\limsup$은 무엇을 잡는가

$\limsup s_n$은 “수열이 무한히 자주 가까이 가는 값들 중 가장 위쪽 값”이다. 그래서 실제로 꼭 subsequential limit여야 하고, 그보다 큰 수는 eventually upper bound가 되어야 한다.

즉 Theorem 3.17의 두 조건

1. 실제로 도달 가능해야 함
2. 그보다 큰 값은 결국 위쪽 경계가 되어야 함

이 바로 $\limsup$의 본질이다.

### 왜 extended real line을 쓰는가

예를 들어 $s_n=n$이면 ordinary real limit는 없지만,
$$
\limsup s_n=+\infty
$$
라고 적을 수 있다. 이 표기가 있으면 “발산”도 구조 있게 서술할 수 있다.

### 수렴과의 관계

수열이 진짜 수렴하면 위아래 흔들림이 사라져서
$$
\limsup s_n=\liminf s_n.
$$
반대로 이 둘이 같으면 subsequential behavior가 하나로 압축되므로 결국 수렴한다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- oscillating sequence의 극한 거동을 설명할 때
- root test, ratio test에서 $\limsup$를 사용할 때
- convergence/nonconvergence를 subsequence로 판정할 때
- comparison 논리에서 tail ordering을 limit superior/inferior로 넘길 때

### 📌 문제 풀이 패턴

1. **서로 다른 두 subsequence 찾기**  
   $\limsup\neq\liminf$이면 비수렴의 강력한 증거다.

2. **꼬리 부등식 전달 패턴**  
   eventually $s_n\le t_n$이면 limsup/liminf에도 inequality가 간다.

3. **실제 subsequence 구성 패턴**  
   $\limsup$값 근처의 항을 계속 골라 subsequence를 만든다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### 대표 예시 1: $(-1)^n$

이 수열은 수렴하지 않지만,
$$
\limsup (-1)^n=1,
\qquad
\liminf (-1)^n=-1.
$$
즉 위아래 흔들림이 정확히 기록된다.

### 대표 예시 2: 단조수열과 결합

단조증가 수열이면 사실 $\limsup$와 $\sup$의 tail 개념이 거의 같아진다. 따라서 monotone convergence 정리와 연결할 때 매우 자연스럽다.

### Chapter 3 이후 내용과 연결

- Root test에서
  $$
  \alpha=\limsup \sqrt[n]{|a_n|}
  $$
  를 정의해 판정한다.
- Ratio/root 비교 정리에서도 $\limsup$가 중심 역할을 한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 3.15 포함
- [x] Definition 3.16 포함
- [x] Theorem 3.17 포함
- [x] Examples 3.18 포함
- [x] Theorem 3.19 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

### 개념 확인 질문

1. $\limsup s_n$이 실제 subsequential limit여야 하는 이유는 무엇인가?
2. $\limsup$와 $\liminf$가 같다는 것이 왜 수렴을 뜻하는가?
3. 왜 eventually inequality가 limsup inequality로 이어지는가?

### 간단한 훈련 문제

1. $s_n=(-1)^n+1/n$에 대해 $\limsup s_n$, $\liminf s_n$를 구하라.
2. $s_n=n$에 대해 $\limsup s_n$, $\liminf s_n$를 extended real sense에서 구하라.
3. $s_n\le t_n$ eventually이면 $\limsup s_n\le\limsup t_n$를 정의로 다시 증명해 보라.
