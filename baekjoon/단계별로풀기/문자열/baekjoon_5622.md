# baekjoon_5622



```
https://www.acmicpc.net/problem/5622
```



```
char = input()

phone_num = {
  '1' : '',
  '2' : ['A', 'B', 'C'],
  '3' : ['D', 'E', 'F'],
  '4' : ['G', 'H', 'I'],
  '5' : ['J', 'K', 'L'],
  '6' : ['M', 'N', 'O'],
  '7' : ['P', 'Q', 'R', 'S'],
  '8' : ['T', 'U', 'V'],
  '9' : ['W', 'X', 'Y', 'Z'],
  '0' : ''
}
res = 0

for i in char:
  for key, value in phone_num.items():
    if i in value:
      res += (int(key) + 1)
print(res)
```

