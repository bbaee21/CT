# baekjoon_2292



```
https://www.acmicpc.net/problem/2292
```



```
n = int(input())

start = 1
cnt = 1
while n > start:
  start += 6 * cnt
  cnt += 1
print(cnt)
```

