# baekjoon_1316



```
https://www.acmicpc.net/problem/1316
```



```
T = int(input())

res = 0 
for _ in range(T):
  char = input()
  continue_num = 0

  for idx in range(len(char) - 1):
    if char[idx] != char[idx + 1]:
      new_char = char[idx + 1:]
      if new_char.count(char[idx]) > 0:
        continue_num += 1
  if continue_num == 0:
    res += 1
print(res)
```

