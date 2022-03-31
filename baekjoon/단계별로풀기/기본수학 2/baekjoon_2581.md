# baekjoon_2581



```
https://www.acmicpc.net/problem/2581
```



```
N = int(input())
M = int(input())

plus_sosu = []

for i in range(N, M + 1):
  not_sosu = 0
  if i > 1:
    for j in range(2, i):
      if i % j == 0:
        not_sosu += 1
        break
    if not_sosu == 0:
      plus_sosu.append(i)

if len(plus_sosu) > 0:
  print(sum(plus_sosu))
  print(min(plus_sosu))
else:
  print(-1)
```

