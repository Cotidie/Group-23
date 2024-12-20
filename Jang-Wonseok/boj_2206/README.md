## Link
[벽 부수고 이동하기](https://www.acmicpc.net/problem/2206)

## Topic
- BFS

## Approach

 가중치가 없는 곳에서 최단거리를 찾으려면 BFS를 이용해야 한다. 단, 벽을 부수지 않은 경우와 벽을 부순 경우 모두 한 곳에 도달할 수 있으므로 visited 배열을 따로 구성해야 한다.

1. BFS를 수행할 큐와 전용 자료형, 방문 여부를 체크할 배열을 준비한다.
    - `Travel`: 현재 위치, 거리, 벽 부수기 여부를 담는 자료형
    - `visited[N][M][2]`: 벽 부수기 여부에 따라 따로 방문 여부를 체크할 배열
2. (1, 1)에서부터 BFS를 수행한다.
    - 벽을 만났을 때 벽을 부순 후 큐에 넣는다.
3. 가장 처음 (N, M)에 도달했을 때 그 거리를 반환한다.
    - 만약 BFS가 종료되었다면 (N, M)에 도달하지 못한 경우이다.
   
## Note
- 아직 벽을 부수지 않았다면 방문 여부를 모두 체크해도 되지 않을까?