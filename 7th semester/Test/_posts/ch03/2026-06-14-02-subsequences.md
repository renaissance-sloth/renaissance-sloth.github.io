# 📘 Chapter 3 — Subsequences 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절의 핵심 질문은 이것이다.

> 원래 수열 전체는 수렴하지 않더라도, 그 안에서 적당히 골라낸 부분수열은 수렴할 수 있는가?

이 절의 흐름은 다음과 같다.

- 먼저 **subsequence**와 **subsequential limit**를 정의한다.
- 그 다음 compact space에서는 반드시 수렴 부분수열이 존재한다는 사실을 증명한다.
- 특히 $\mathbb R^k$에서는 **bounded sequence이면 convergent subsequence를 가진다**는 아주 중요한 결론을 얻는다.
- 마지막으로 subsequential limit들의 집합이 closed라는 사실을 보인다.

이 절은 뒤에서 나오는 Cauchy sequence, limsup/liminf, 함수열의 compactness 논의의 출발점이다. 특히 “전체는 안 잡히더라도 부분은 잡힌다”는 감각이 이후 해석학 전체에서 반복된다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Definition 3.5 — Subsequence

sequence $\{p_n\}$가 주어졌다고 하자. 양의 정수열
$$
n_1<n_2<n_3<\cdots
$$
을 택하면, 그에 대응하는 sequence
$$
\{p_{n_k}\}
$$
를 $\{p_n\}$의 **subsequence**라고 한다.

만약 $\{p_{n_k}\}$가 수렴하면, 그 극한을 $\{p_n\}$의 **subsequential limit**라고 한다.

### ▪ Remark

$\{p_n\}$이 $p$로 수렴할 필요충분조건은, $\{p_n\}$의 모든 subsequence가 역시 $p$로 수렴하는 것이다.

이 사실은 직관적으로 매우 중요하다. 전체 수열이 진짜로 $p$로 가고 있다면, 중간중간 몇 항을 빼버려도 여전히 $p$로 가야 한다. 반대로 어떤 subsequence 하나라도 다른 곳으로 가버리면 전체는 $p$로 수렴할 수 없다.

### ▪ Theorem 3.6

1. $\{p_n\}$이 compact metric space $X$의 sequence이면, $\{p_n\}$의 어떤 subsequence는 $X$의 한 점으로 수렴한다.
2. $\mathbb R^k$의 모든 bounded sequence는 convergent subsequence를 포함한다.

### ▪ Proof

**(1)** $E$를 $\{p_n\}$의 range라고 하자.

- 만약 $E$가 유한집합이면, 비둘기집 원리와 같은 생각으로 어떤 점 $p\in E$가 무한히 자주 나타난다. 따라서
  $$
  p_{n_1}=p_{n_2}=\cdots=p
  $$
  인 subsequence를 만들 수 있고, 이 subsequence는 자명하게 $p$로 수렴한다.

- 만약 $E$가 무한집합이면, compactness에 의해 $E$는 limit point $p\in X$를 가진다. 이제 귀납적으로
  $$
  d(p,p_{n_i})<1/i
  $$
  를 만족하도록 $n_1<n_2<\cdots$를 고를 수 있다. 그러면
  $$
  p_{n_i}\to p.
  $$

따라서 compact metric space의 모든 sequence는 convergent subsequence를 가진다.

**(2)** 이것은 (1)에서 바로 나온다. 이유는 $\mathbb R^k$의 bounded subset은 compact closure 안에 들어가기 때문이다.

### ▪ Theorem 3.7

metric space $X$에서 sequence $\{p_n\}$의 모든 subsequential limit들의 집합은 $X$의 closed subset을 이룬다.

### ▪ Proof

subsequential limit 전체의 집합을 $E^*$라 하고, $q$를 $E^*$의 limit point라 하자. 목표는 $q\in E^*$를 보이는 것이다.

$p_{n_1}\neq q$가 되도록 $n_1$을 택하고,
$$
\delta=d(q,p_{n_1})
$$
로 두자. 이제 귀납적으로 $n_1,\dots,n_{i-1}$이 정해졌다고 하자.

$q$가 $E^*$의 limit point이므로,
$$
d(x,q)<2^{-i}\delta
$$
를 만족하는 $x\in E^*$를 택할 수 있다. 그런데 $x\in E^*$라는 것은 어떤 subsequence가 $x$로 수렴한다는 뜻이므로, 그 subsequence의 충분히 뒤쪽 항 중에서
$$
d(x,p_{n_i})<2^{-i}\delta
$$
를 만족하는 $n_i>n_{i-1}$를 택할 수 있다. 그러면 triangle inequality로
$$
d(q,p_{n_i})\le d(q,x)+d(x,p_{n_i})<2^{-i}\delta+2^{-i}\delta=2^{1-i}\delta.
$$

따라서
$$
p_{n_i}\to q.
$$
즉 $q\in E^*$. 따라서 $E^*$는 closed이다.

---

## 🟢 3. 개념 해설 + 엄밀성

### 왜 subsequence를 도입하는가

어떤 수열이 수렴하지 않는다고 해서 아무 정보가 없는 것은 아니다. 예를 들어
$$
(-1)^n
$$
은 전체로는 발산하지만, 짝수 부분수열은 1로, 홀수 부분수열은 -1로 수렴한다.

즉 subsequence는 “발산하는 수열이 어디로 흔들리는지”를 드러내는 도구다.

### compactness가 왜 등장하는가

compactness는 해석학에서 “무한한 것에서도 limit를 뽑아낼 수 있는 성질”로 자주 나타난다. 여기서는 그 첫 형태가 바로

> compact space의 모든 sequence는 convergent subsequence를 가진다.

라는 명제다.

이 정리는 나중에 함수열의 Arzelà–Ascoli류 논리, 최적화, measure/functional analysis의 compactness argument의 원형이 된다.

### subsequential limit 집합이 closed라는 말의 의미

부분극한들이 여기저기 흩어져 있어도, 그 부분극한들의 극한점도 결국 다시 부분극한이 된다는 뜻이다. 즉 “부분극한 집합은 닫혀 있다.” 이건 limsup/liminf를 다룰 때 매우 자연스럽다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가

- bounded sequence에서 수렴 부분수열을 뽑고 싶을 때
- 어떤 수열이 발산함을 보이기 위해 서로 다른 subsequential limit를 찾을 때
- compactness를 실제 계산 가능한 형태로 바꿔 쓰고 싶을 때
- limsup, liminf, cluster point 문제를 풀 때

### 📌 문제 풀이 패턴

1. **유한 range 패턴**  
   어떤 값이 무한히 많이 나오면 constant subsequence를 뽑는다.

2. **limit point 근처로 점점 조이기 패턴**  
   $1,1/2,1/3,\dots$처럼 반지름을 줄여가며 subsequence를 만든다.

3. **두 개의 다른 부분극한 찾기 패턴**  
   전체 수열의 발산을 보여줄 때 자주 쓴다.

4. **closedness 패턴**  
   subsequential limit 집합의 limit point를 다시 subsequence로 잡아 넣는다.

---

## 🔴 5. 대표 문제 & 풀이 전략

### 이 절과 직접 연결되는 대표 질문

1. bounded sequence가 왜 꼭 수렴하지는 않는가?  
   → 예: $(-1)^n$. 하지만 subsequence는 수렴시킬 수 있다.

2. 전체 수열이 수렴하지 않음을 어떻게 보이는가?  
   → 서로 다른 두 subsequential limit를 찾으면 된다.

3. compactness가 왜 useful한가?  
   → 무한한 sequence에서 limit를 뽑아낼 수 있기 때문이다.

### Chapter 3 과제와 연결

- Exercise 14: subsequence와 평균수열 비교에서 “원래 수열이 흔들려도 평균은 수렴할 수 있다”는 점을 이해할 때 도움이 된다.
- Exercise 20: Cauchy sequence의 subsequence가 수렴하면 전체가 수렴한다는 논리에서 subsequence가 본격적으로 사용된다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Definition 3.5 포함
- [x] Theorem 3.6 포함
- [x] Theorem 3.7 포함
- [x] 핵심 remark 포함
- [x] 문제 풀이 연결 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

### 개념 확인 질문

1. subsequence와 원래 sequence의 차이는 무엇인가?
2. 왜 compactness가 convergent subsequence의 존재를 보장하는가?
3. subsequential limit 집합이 closed라는 사실은 어떤 점에서 자연스러운가?

### 간단한 훈련 문제

1. $(-1)^n$의 subsequential limit를 모두 구하라.
2. $\sin n$이 bounded임을 이용해 convergent subsequence를 가진다고 설명하라.
3. 어떤 sequence가 두 개의 서로 다른 subsequential limit를 가지면 수렴할 수 없음을 보이라.
