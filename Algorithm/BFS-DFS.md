# BFS and DFS

## DFS(Depth-First Search)
- 루트 노드 또는 임의의 노드에서 다음 브랜치로 넘어가기 전에 해당 브랜치를 모두 탐색하는 방법
- 스택 or 재귀함수를 이용해 구현
- 모든 경로를 방문해야 할 경우에 적합함
- 시간 복잡도(정점의 수 : N, 간선의 수 : E)
    - 인접 행렬 : `O(V^2)`
    - 인접 리스트 : `O(V+E)`

## BFS(Breadth-First Search)
- 루트 노드 또는 임의의 노드에서 인접한 노드부터 먼저 탐색하는 방법
- 큐를 이용해 구현
- 최소 비용이 우선일 때 적합함
- 시간 복잡도(정점의 수 : N, 간선의 수 : E)
    - 인접 행렬 : `O(V^2)`
    - 인접 리스트 : `O(V+E)`