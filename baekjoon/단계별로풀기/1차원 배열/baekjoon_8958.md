# baekjoon_8958



```
https://www.acmicpc.net/problem/8958
```



```
T = int(input())

for _ in range(T):
  score = list(input())

  res = 0
  cnt = 1

  for i in score:
    if i == 'O':
      res += cnt
      cnt += 1
    else:
      cnt = 1
  print(res)
```

