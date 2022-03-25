# baekjoon_1110



```
https://www.acmicpc.net/problem/1110
```



```
n = int(input())
nx_n = n

cnt = 0

while True:
  a = nx_n // 10
  b = nx_n % 10
  nx_n = b * 10 + ((a + b) % 10)

  cnt += 1

  if nx_n == n:
    break
print(cnt)
```

