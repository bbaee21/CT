# baekjoon_2941



```
https://www.acmicpc.net/problem/2941
```



```
char = input()

ls = ['c=', 'c-', 'dz=', 'd-', 'lj', 'nj', 's=', 'z=']

res = 0

for i in range(len(ls)):
  char = char.replace(ls[i], 'c')
print(len(char))
```

