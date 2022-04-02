# baekjoon_17427



```
https://www.acmicpc.net/problem/17427
```



```
N = int(input())
res = 0
for i in range(1, N + 1):
  res += (N // i) * i
  
print(res)
```

