# baekjoon_1157



```
https://www.acmicpc.net/problem/1157
```



```
char = input().lower()
ls_char = list(set(char))
max_value = []

for i in ls_char:
  cnt = char.count(i)
  max_value.append(cnt)

if max_value.count(max(max_value)) > 1:
  print('?')
else:
  max_idx = max_value.index(max(max_value))
  print(ls_char[max_idx].upper())
```

