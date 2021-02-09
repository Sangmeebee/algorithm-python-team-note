# heapq

- heapq : 힙 자료구조를 제공
  
  - 우선순위 큐 기능을 구현하기 위해 사용 (다익스트라(최단경로) 알고리즘)
  - 최소 힙으로 구현 되어 있음 (우선 순위가 낮은 순서)
  - **최소 힙**
  
  ~~~python
  import heapq
  
  def heapsort(iterable) :
    h = []
    result = []
    
    for v in iterable :
      heapq.heappush(h, v)
    for i in range(len(h)) :
      result.append(heapq.heappop(h))
    return result
      
  result = heapsort([1, 3, 5, 7, 9, 2, 4, 6, 8])
  print(result)
  ~~~
  
  - **최대 힙**
  
  ~~~python
  import heapq
  
  def heapsort(iterable) :
    
    h = []
    result = []
    
    for v in iterable :
      heapq.heappush(h, -v)
    for _ in range(len(h)) :
      result.append(-heapq.heappop(h))
    return result
  
  result = heapsort([1, 3, 5, 7, 9, 2, 4, 6, 8])
  print(result)
  ~~~
  
  

