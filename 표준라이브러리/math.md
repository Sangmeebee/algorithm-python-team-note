# math

- math : 수학적 기능 제공

  - 팩토리얼, 제곱근, 최대공약수(GCD), 삼각함수 관련 함수, pi와 같은 상수

  - **최대 공약수(gcd)**

    - 최대 공약수를 구해야 할 때는 math 라이브러리의 gcd() 함수를 이용

    - ~~~python
      import math
      
      #최소 공배수(LCM)를 구하는 함수
      def lcm(a, b) :
        return a*b // math.gcd(a, b)
      
      a = 21
      b = 14
      
      print(math.gcd(a, b)) #최대공약수(GCD)
      print(lcm(21, 14)) #최소공배수(LCM)
      
      #7
      #42
      ~~~

      