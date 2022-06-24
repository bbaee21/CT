# baekjoon_9020



```
https://www.acmicpc.net/problem/9020
```



```
실패
```

```
def sosu(n):
    if n == 1:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

for _ in range(int(input())):
    num = int(input())

    a, b = num // 2, num // 2
    while a > 0:
        if sosu(a) and sosu(b):
            print(a, b)
        else:
            a -= 1
            b += 1
```



```
성공
```

```
def sosu(x):
  if x == 1:
    return False
  for i in range(2, int(x ** 0.5) + 1):
    if x % i == 0:
      return False
  return True


N = int(input())

while N:
  num = int(input())

  s_num_1 = num // 2
  s_num_2 = s_num_1

  for _ in range(s_num_1):
    if sosu(s_num_1) and sosu(s_num_2):
      print(s_num_1, s_num_2)
      break
    else:
      s_num_1 -= 1
      s_num_2 += 1
  N -= 1
```
