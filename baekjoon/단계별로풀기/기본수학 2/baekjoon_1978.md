# baekjoon_1978



```
https://www.acmicpc.net/problem/1978
```



```
T = int(input())

arr = list(map(int, input().split()))

res = 0
for i in range(T):
  not_sosu = 0
  if arr[i] > 1:
    for j in range(2, arr[i]):
      if arr[i] % j == 0:
        not_sosu += 1
    if not_sosu == 0:
      res += 1
print(res)
```

