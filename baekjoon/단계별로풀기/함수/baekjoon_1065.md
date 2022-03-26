# baekjoon_1065



```
https://www.acmicpc.net/problem/1065
```



```
n = int(input())
res = 0

for i in range(1, n + 1):
  ls = list(map(int, str(i)))

  if i < 100:
    res += 1
  elif (ls[0] - ls[1]) == (ls[1] - ls[2]):
    res += 1

print(res)
```

