# baekjoon_2525



```
https://www.acmicpc.net/problem/2525
```



```
H, M = map(int, input().split())

time = int(input())

if M + time >= 60:
  if (M + time) % 60 == 0:
    if H + (M + time) // 60 >= 24:
      H -= 24
    print(H + ((M + time) // 60), 0)
  else:
    H += (M + time) // 60
    M = (M + time) % 60
    if H >= 24:
      H -= 24
    print(H, M)
else:
  print(H, M + time)
```

