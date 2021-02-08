# bisect

bisect : 이진 탐색 기능을 제공

- **bisect_left**, **bisect_right** : 이진탐색으로 해당하는 데이터의 왼쪽, 오른쪽 인덱스의 값을 출력

  ~~~python
  from bisect import bisect_left, bisect_right
  
  a = [1, 2, 4, 4, 8]
  x = 4
  
  print(bisect_left(a, x))
  print(bisect_right(a, x))
  ~~~

  

- 특정 범위의 데이터 수 계산

  ~~~python
  from bisect import bisect_left, bisect_right
  def count_by_range(a, left_value, right_value) :
    return bisect_right(a, right_value) - bisect_left(a, left_value)
  ~~~

  