# baekjoon_4673



```
https://www.acmicpc.net/problem/4673
```



```

ori_set = set(range(1, 10001))
sangsung = set()
for i in range(1, 10001):
  for j in str(i):
    i += int(j)
  sangsung.add(i)

res = sorted(ori_set - sangsung)

for k in res:
  print(k)

```

