# baekjoon_11022



```
https://www.acmicpc.net/problem/11022
```



```
import sys

n = int(input())

res = 0

for i in range(1, n + 1):
  A, B = map(int, sys.stdin.readline().split())
  res = A + B
  print('Case #{}: {} + {} = {}'.format(i, A, B, res))
```

