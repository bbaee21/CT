# baekjoon_1546



```
https://www.acmicpc.net/problem/1546
```



```
T = int(input())
arr = list(map(int, input().split()))
max_scr = max(arr)

for i in range(T):
  arr[i] = arr[i] / max_scr * 100

aver = sum(arr) / len(arr)

print(aver)
```

