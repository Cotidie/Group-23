## Link
[파티](https://www.acmicpc.net/problem/1238)

## Topic
- Shortest Path (Dijkstra)

## Approach
 파티가 열리는 마을에서 다른 마을까지 최단경로를 구하고, 그중 가장 큰 값을 출력한다. 한 점으로부터 임의의 점까지의 최단경로이므로 다익스트라 알고리즘을 사용한다.

 1. 인접한 마을 중 가장 가까운 마을을 찾기 위한 우선순위 큐와 전용 자료형을 준비한다.
    - `pq`: 인접한 마을 중 가장 짧은 경로를 선택할 우선순위 큐
    - `Pair`: 현재 마을 번호와 경로 비용을 담는 자료형
 2. 시작 마을로부터 가장 가까운 마을을 고르고 최단거리를 확정한다.
    - 이미 확정된 값이 있으면 그대로 둔다. (계산한 값이 더 적은 경우)
    - 우선순위 큐에 인접한 마을까지의 경로를 넣는다.
 3. 우선순위 큐에서 가장 짧은 경로를 꺼내 최단거리를 확정한다.
    - 꺼낸 값이 기존 값보다 크다면 이미 확정된 마을이다.
 4. 2~3을 큐가 빌 때까지 반복한다.

## Trials
- 도로는 단방향이므로 모든 학생에 대해 다익스트라를 돌려야 한다. 가는 길과 오는 길이 다르다.
- 도시로부터 한 번 돌리고, 도시를 제외한 곳으로부터 한 번씩 더 돌려 합산한다.
  - 전자는 집에 가는 길, 후자는 도시로 가는 길이다.