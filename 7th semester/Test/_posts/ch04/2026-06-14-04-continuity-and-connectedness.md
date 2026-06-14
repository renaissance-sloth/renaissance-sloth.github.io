# 📘 Chapter 4 — Continuity and Connectedness 통합 강의

---

## 📍 1. 전체 구조 (Big Picture)

이 절의 핵심은 연속함수가 **connectedness를 보존한다**는 사실이다.

- connected set의 continuous image가 connected임을 보인다.
- 그 결과로 interval 위 continuous real function의 **intermediate value theorem**을 얻는다.
- 마지막으로 intermediate value property만으로 continuity가 따라오지는 않는다는 점을 짚는다.

즉 이 절은 “연속함수는 중간값을 건너뛰지 않는다”는 유명한 직관을 엄밀하게 만들어 준다.

---

## 🔵 2. 원문 기반 정리 (완전 반영)

### ▪ Theorem 4.22

$f:X\to Y$가 continuous mapping이고, $E\subset X$가 connected subset이면 $f(E)$는 connected이다.

### ▪ Proof

반대로 $f(E)=A\cup B$가 nonempty separated sets $A,B\subset Y$로 분리된다고 하자. 그러면
$$
G=E\cap f^{-1}(A),
\qquad
H=E\cap f^{-1}(B)
$$
로 두면 $E=G\cup H$이고 둘 다 empty가 아니다.

또 $f$의 continuity 때문에 inverse image of closed set은 closed이므로, $G$와 $H$의 closures는 서로 만나지 않게 된다. 따라서 $G,H$는 separated이고, 이는 $E$가 connected라는 가정과 모순이다. 따라서 $f(E)$는 connected이다.

### ▪ Theorem 4.23 — Intermediate Value Theorem

$[a,b]$ 위의 continuous real function $f$가 있고
$$
f(a)<c<f(b)
$$
라 하자. 그러면 어떤 $x\in(a,b)$가 존재하여
$$
f(x)=c.
$$

물론 $f(a)>f(b)$인 경우도 마찬가지이다.

### ▪ Proof

Theorem 2.47에 의해 interval $[a,b]$는 connected이다. 따라서 Theorem 4.22로부터 $f([a,b])\subset\mathbb R$도 connected이다. 그런데 실수축의 connected set은 interval이므로, $f(a)$와 $f(b)$ 사이의 모든 값, 특히 $c$를 포함해야 한다. 따라서 어떤 $x\in[a,b]$에 대해 $f(x)=c$이다. strict inequality 때문에 실제로 $x\in(a,b)$.

### ▪ Remark 4.24

중간값 성질의 converse, 즉 intermediate value property를 가지면 자동으로 continuous일 것처럼 보일 수 있지만, 이는 거짓이다. 뒤의 Example 4.27(d)류 현상이 이를 경고한다.

---

## 🟢 3. 개념 해설 + 엄밀성

connectedness는 “두 조각으로 깔끔하게 분리되지 않는 성질”이다. Theorem 4.22는 연속함수가 그런 “붙어 있음”을 깨뜨리지 못한다는 말이다.

Intermediate Value Theorem은 사실 특별한 실함수 정리가 아니라, **connectedness preservation의 1차원 버전**이다. Rudin이 이 정리를 connectedness에서 뽑아내는 이유가 바로 여기에 있다.

---

## 🟡 4. 핵심 사용법 (문제 풀이 연결)

### 📌 언제 사용하는가
- 함수가 특정 값을 반드시 한 번은 지나야 함을 보일 때
- 방정식 $f(x)=c$의 해 존재를 보일 때
- connectedness를 image 쪽으로 전달할 때

### 📌 문제 풀이 패턴
1. domain이 interval/connected인지 확인
2. function continuity 확인
3. image가 connected라는 결론 사용
4. 실수축에서는 connected = interval임을 써서 중간값 결론 도출

---

## 🔴 5. 대표 문제 & 풀이 전략

### 대표 사용법: existence proof

예를 들어 $f(a)<0<f(b)$이면 Intermediate Value Theorem으로 $f(x)=0$인 $x$의 존재를 즉시 얻는다. 해 존재를 보이는 가장 고전적인 패턴이다.

### Chapter 4 exercise 연결

- Exercise 19는 intermediate value property를 역방향으로 활용하는 문제다.
- Exercise 23, 24의 convexity 문제에서도 interval 구조와 연속성이 반복해서 작동한다.

---

## ⚫ 6. 섹션 체크리스트

- [x] Theorem 4.22 포함
- [x] Theorem 4.23 포함
- [x] Remark 4.24 포함
- [x] connectedness와 intermediate value 연결 설명 포함
- [ ] PDF 원문과 문장 단위 추가 대조 완료

---

## ⚪ 7. 이해 확인 & 훈련 문제

- 왜 continuous image of connected is connected 인가?
- Intermediate Value Theorem이 connectedness의 결과라는 말은 무슨 뜻인가?
- 중간값 성질이 continuity를 바로 뜻하지 않는 이유는 무엇인가?
