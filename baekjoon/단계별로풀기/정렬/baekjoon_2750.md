# baekjoon_2750



```
https://www.acmicpc.net/problem/2750
```



```
N = int(input())
M = set()

for i in range(M):
	M.add(int(input()))

M = list(M)
M.sort()

for j in range(len(M)):
	print(M[j])
```

