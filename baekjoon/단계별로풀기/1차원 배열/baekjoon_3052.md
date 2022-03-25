# baekjoon_3052



```
https://www.acmicpc.net/problem/3052
```



```

temp = []
for i in range(10):
  n = int(input())
  rem = n % 42
  temp.append(rem)

set_temp = set(temp)

print(len(set_temp))
```

