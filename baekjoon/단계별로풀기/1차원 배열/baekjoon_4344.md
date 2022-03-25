# baekjoon_4344



```
https://www.acmicpc.net/problem/4344
```



```
T = int(input())

for _ in range(T):
  cnt = 0
  score = list(map(int, input().split()))
  std = score.pop(0)

  aver = sum(score) / std

  for scr in score:
    if scr > aver:
      cnt += 1
  res = (cnt / std) * 100

  print('{0:.3f}%'.format(res))
```

