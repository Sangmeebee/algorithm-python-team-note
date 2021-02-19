# Collections

- collections : 덱, 카운터 등의 유용한 자료구조 표함

  - **Counter** : 등장 횟수를 세는 기능

    - 리스트와 같은 반복 가능한 객체가 주어졌을 때 내부에 원소가 몇 번씩 등장했는지 알려줌

    - ~~~python
      from collections import Counter
      counter = Counter(['red', 'blue', 'red', 'greed', 'blue', 'blue'])
      print(counter['blue'])
      print(counter['green'])
      print(dict(counter))
      #3
      #0
      #{'red': 2, 'blue': 3, 'greed': 1}
      
      modes = counter.most_common()
      print(modes)
      #[('blue', 3), ('red', 2), ('greed', 1)]
      ~~~

      
