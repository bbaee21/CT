# baekjoon_2869

> 달팽이는 올라가고 싶다.



* 처음 실패 코드

```
A, B, V = map(int, input().split())

sun = 0
h = 0

while True:
    sun += 1
    h += A
    if h == A:
        print(sun)
        break
    h -= B
```

* while로 시간초과 예상



* 성공코드

```
import math

A, B, V = map(int, input().split())

c = V - A
move = A - B

print(math.ceil(c / move) + 1)
```

* math import 해서 반올림 한다.
* 