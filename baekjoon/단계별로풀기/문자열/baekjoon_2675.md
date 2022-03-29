# baekjoon_2675



```
https://www.acmicpc.net/problem/2675
```



```
T = int(input())
for _ in range(T):
  cnt, arr = input().split()
  char = ''
  for i in arr:
    char += int(cnt) * i
  print(char)
```

