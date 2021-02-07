# BFS

- 너비 우선 탐색 : 시작노드에서 가까운 노드부터 우선적으로 탐색

- 특정 조건에서 최단 경로를 구할 때 사용하는 알고리즘

- 큐 자료구조 이용

- 동작 과정

  - 탐색 **시작 노드**를 **큐에 삽입**하고 **방문 처리** 한다.

  - 큐에서 노드를 꺼낸 뒤에 해당 노드의 인접 노드 중에서 방문하지 않은 노드를 모두 큐에 삽입하고 방문 처리

  - 2번의 과정을 수행할 수 없을 때까지 반복

  

  <img src="/Users/sangmee/Library/Application Support/typora-user-images/스크린샷 2021-02-07 오후 5.41.10.png" alt="스크린샷 2021-02-07 오후 5.41.10" style="zoom:50%;" />

  

  ~~~python
from collections import deque
  def bfs(graph, start, visited) :
    queue = deque([start])
    visited[start] = True
    while queue :
      v = queue.popleft()
      print(v, end=' ')
      for i in graph[v] :
        if not visited[i] :
          queue.append(i)
          visited[i] = True
        	
  graph = [[], [2, 3, 8], [1, 7], [1, 4, 5], [3, 5], [3, 4], [7], [2, 6, 8], [1, 7]]
  visited = [False]*9
  bfs(graph, 1, visited)
  ~~~