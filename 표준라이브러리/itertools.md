## 순열과 조합

- 모든 경우의 수를 고려해야 할 때 

- itertools : 반복되는 형태의 데이터를 처리

  - 순열과 조합 라이브러리는 코딩 테스트에 자주 사용 (완전 탐색 문제)

- **순열** : 서로 다른 n개에서 서로 다른 r개를 선택하여 일렬로 나열

  - {'A', 'B', 'C'}에서 세 개를 선택하여 나열하는 경우 : 'ABC', 'ACB', 'BAC', 'BCA', 'CAB', 'CBA'

  - ~~~python
    from itertools import permutations
    data = ['A', 'B', 'C']
    result = list(permutations(data, 3))
    print(result)
    #[('A', 'B', 'C'), ('A', 'C', 'B'), ('B', 'A', 'C'), ('B', 'C', 'A'), ('C', 'A', 'B'), ('C', 'B', 'A')]
    ~~~

  - 중복 순열

    - ~~~python
      from itertools import product
      data = ['A', 'B', 'C']
      result = list(product(data, repeat=2))
      print(result)
      #[('A', 'A'), ('A', 'B'), ('A', 'C'), ('B', 'A'), ('B', 'B'), ('B', 'C'), ('C', 'A'), ('C', 'B'), ('C', 'C')]
      ~~~

      

- **조합** : 서로 다른 n개에서 **순서에 상관 없이** 서로 다른 r개를 선택하는 것

  - {'A', 'B', 'C'}에서 순서를 고려하지 않고 두 개를 뽑는 경우 : 'AB', 'AC', 'BC'

  - ~~~python
    from itertools import combinations
    data = ['A', 'B', 'C']
    result = list(combinations(data, 2))
    print(result)
    #[('A', 'B'), ('A', 'C'), ('B', 'C')]
    ~~~

  - 중복조합

    - ~~~python
      from itertools import combinations_with_replacement
      data = ['A', 'B', 'C']
      result = list(combinations_with_replacement(data, 2))
      print(result)
      # [('A', 'A'), ('A', 'B'), ('A', 'C'), ('B', 'B'), ('B', 'C'), ('C', 'C')]
      ~~~

