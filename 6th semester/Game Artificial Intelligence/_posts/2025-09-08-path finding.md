---
title: "경로 탐색"
excerpt: "'게임 인공지능' 과목의 경로 탐색 설명입니다."
tags: syllabus ai game
header:
  teaser: https://drive.google.com/thumbnail?id=1yaExL1j9qfjyfHwmDdTBnSHI3c-RnL0G&sz=w1000
---

# 길 찾기 (Pathfinding)

*   **문제:** 캐릭터/유닛이 A 지점에서 B 지점으로 이동할 경로를 찾는 것
*   **게임에서 가장 일반적인 AI 요구사항 중 하나입니다.**
*   특히 유닛이 많은 RTS 게임에서 중요합니다.

## 가장 간단한 시나리오 (Simplest scenario)

*   단일 캐릭터
*   비실시간
*   격자
*   정적 세계
*   **해결책: A\***

## 복잡한 시나리오 (Complex scenario)

*   여러 캐릭터 (경로가 겹침)
*   실시간
*   연속 지도
*   동적 세계

# BFS와 A\* 시각적 비교 (Visual comparison BFS vs A\*)

*   [길찾기 알고리즘 비교](http://qiao.github.io/PathFinding.js/visual/)
*   [실제 지도에서 경로 찾기](https://www.kevanahlquist.com/osm_pathfinding/)

# 예시 (Example)

*   "시작"에서 "목표"에 도달하세요.
*   유닛은 상, 하, 좌, 우로 이동할 수 있습니다.

# 예시: 너비 우선 탐색 (Breadth First Search)

*   OPEN = [시작]
*   CLOSED = []

*   **탐색 알고리즘은 목표를 찾을 때까지 탐색 공간의 노드를 탐색합니다.**
*   다른 알고리즘은 다른 순서로 노드를 탐색합니다.
*   **각 시점에서 두 가지 노드 목록이 있습니다.**
    *   탐색된 노드 (CLOSED)
    *   탐색할 후보 노드 (OPEN)

*   **노드가 탐색(확장)될 때, 모든 후속 노드(자식)가 OPEN 목록에 추가됩니다.**

*   **너비 우선 탐색은 OPEN 목록에 추가된 순서대로 노드를 탐색합니다.**
    *   '시작'에 더 가까운 노드가 항상 더 멀리 있는 노드보다 먼저 탐색됩니다.

## 너비 우선 탐색 (Breadth First Search) 알고리즘

```
OPEN = [시작]
CLOSED = []
WHILE OPEN이 비어있지 않은 동안:
    N = OPEN.removeFirst()
    IF goal(N) THEN path to N을 반환 (RETURN)
    CLOSED.add(N)
    FOR N의 모든 자식 C가 CLOSED 또는 OPEN에 없는 경우:
        C.parent = N
        OPEN.add(C)
    ENDFOR
ENDWHILE
```

*   **길 찾기에서 최단 경로를 찾습니다.**
*   **하지만...**
    *   **높은 계산 비용:** 지도의 너무 많은 셀을 탐색합니다.
    *   시간 비용: 확장된 노드의 수
    *   메모리 비용: 확장된 노드의 수

# A\*

*   **휴리스틱 탐색 알고리즘:**
    *   **주어진 시작 노드와 목표 사이의 최단 경로를 찾습니다.**
    *   탐색을 안내하기 위해 휴리스틱을 사용합니다.
    *   **휴리스틱: h(n) -> n에서 목표까지의 거리 추정치**

*   **완전성:** 해결책이 있다면, A\*는 해결책을 찾습니다.

*   **최적성:** **휴리스틱이 허용 가능(admissible)하다면, A\*는 최적의 경로를 찾습니다.**
    *   **허용 가능한 휴리스틱은 목표까지의 거리를 절대로 과대평가하지 않습니다.**
    *   **길 찾기에서 유클리드(Euclidean) 및 해밍(Hamming) 거리는 허용 가능한 휴리스틱입니다.**

# 예시: A\*

*   OPEN = [시작]
*   CLOSED = []
*   사용된 휴리스틱: 맨해튼 거리 (Manhattan Distance)

*   **각 노드에 "추정 비용" f를 할당합니다.**
    *   **f(n) = g(n) + h(n)**
        *   g(n): 시작에서 n까지의 실제 비용
        *   h(n): 휴리스틱 (n에서 목표까지의 추정 비용)

*   **가장 낮은 추정 비용을 가진 노드를 먼저 확장합니다.** 

## A\* 알고리즘

```
시작.g = 0;
시작.h = heuristic(시작)
OPEN = [시작];
CLOSED = [];
WHILE OPEN이 비어있지 않은 동안:
    N = OPEN.removeLowestF()
    IF goal(N) THEN path to N을 반환 (RETURN)
    CLOSED.add(N)
    FOR N의 모든 자식 M이 CLOSED 또는 OPEN에 없는 경우:
        M.parent = N
        M.g = N.g + 1;
        M.h = heuristic(M)
        OPEN.add(M)
    ENDFOR
ENDWHILE
```

*   **최적:** **허용 가능한 휴리스틱을 사용하여 길 찾기에서 최단 경로를 찾습니다.**
*   **너비 우선 탐색보다 빠릅니다.**
    *   지도의 더 적은 셀을 탐색합니다 (동일한 최악의 시나리오라도).
*   시간 비용: 확장된 노드의 수
*   메모리 비용: 확장된 노드의 수

*   **휴리스틱은 알고리즘의 탐색을 목표 쪽으로 편향시킵니다.**

*   **너비 우선 탐색:** 편향 없음
*   **A\***: 목표 쪽으로 편향됨

# 지도 표현 (Representation of Map)

*   [A\* 설명](https://www.redblobgames.com/pathfinding/a-star/introduction.html)