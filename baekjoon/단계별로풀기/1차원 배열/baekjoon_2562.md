# baekjoon_2562



```
https://www.acmicpc.net/problem/2562
```



```
arr = []
for _ in range(9):
  n = int(input())
  arr.append(n)

print(max(arr))
print(arr.index(max(arr)) + 1)
```