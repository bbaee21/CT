# baekjoon_2884



```
https://www.acmicpc.net/problem/2884
```



```
H, M = map(int, input().split())

time = 45

if M >= 45:
  print(H, (M - time))
else:
  if H != 0:
    print(H - 1, 60 - abs(time - M))
  else:
    print(23, 60 - abs(time - M))
```

