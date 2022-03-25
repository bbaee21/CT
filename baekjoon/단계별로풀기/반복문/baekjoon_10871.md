# baekjoon_10871



```
https://www.acmicpc.net/problem/10871
```



```
import sys

N, X = map(int, sys.stdin.readline().split())

arr = list(map(int, sys.stdin.readline().split()))

for i in range(N):
  if arr[i] < X:
    print(arr[i])
  else:
    pass
```

