# baekjoon_10809



```
https://www.acmicpc.net/problem/10809
```



```
n = input()
al = 'abcdefghijklmnopqrstuvwxyz'
di = {}

for i in range(len(al)):
  di[al[i]] = -1

for char in n:
  if char in di:
    di[char] = n.index(char)

values = di.values()

for value in values:
  print(value, end=" ")
```

