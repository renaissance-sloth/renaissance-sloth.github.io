---
title: "이전에 들어봤을 법한 것들"
excerpt: "책 기준 1장 내용"
tags: math mathematics abstract algebra 
header:
  teaser: https://media.wiley.com/product_data/coverImage300/92/04713687/0471368792.jpg
---

# set theory (집합론)
본격적으로 시작하기 전에 표기법을 정하자. 매번 같은 말을 길게 반복하면 서로 불편하기 때문이다.

S를 objects(객체)의 collection(모음집)이라고 하자. 

S의 objects는 S의 **element**(원소)라고 부르자.

주어진 S의 element a에 대해 $a \in S$라고 쓰고 `a is an element of S`라 읽을 것이다.

반대로, a가 S에 들어있지 않다면, $a \notin S$라고 쓸 것이다.

예시: S를 양의 정수 $(1, 2, 3, \ldots, n, \ldots)$라고 하면,
$165 \in S$, $-13 \notin S$의 결과를 얻을 수 있다.
{: .notice}

두 개의 집합 S, T에 대해 하나가 다른 하나의 부분이면, 우리는 S를 T의 **subset**(부분집합)이라고 한다.

쓸 때는 $S \subset T$로 쓰고, 읽을 때는 `S is contained in T`(S가 T에 포함되었다.)로 읽는다.

만일 $s \in S$가 $s \in T$를 보장한다면, $S \subset T$임을 알 수 있다.
{: .notice--info}

같은 말을 $T \supset S$로 쓰고, `T contains S`(T가 S를 포함한다.)로 읽을 수도 있다.

예시: T를 양의 정수, S를 양의 짝수라고 하면,
$S \subset T$의 결과를 얻을 수 있다.
{: .notice}

정의에 따라 생각해보면, 자기 자신은 항상 자신의 부분집합이다.

