# baekjoon_11021



```
https://www.acmicpc.net/problem/11021
```



```
import sys

n = int(input())

res = 0

for i in range(1, n + 1):
  A, B = map(int, sys.stdin.readline().split())
  res = A + B
  print('Case #' + str(i) + ':', res)
```

