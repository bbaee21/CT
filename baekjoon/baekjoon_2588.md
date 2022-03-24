# baekjoon_2588



```
https://www.acmicpc.net/problem/2588
```



```

a = input()
b = input()

answer = 0

one = 0
two = 0
thr = 0

for i in range(len(a)):
  for j in range(len(b)):
    if i == 0:
      if j == 0:
        thr += (int(a[i]) * 100) * int(b[j])
      elif j == 1:
        two += (int(a[i]) * 100) * int(b[j])
      else:
        one += (int(a[i]) * 100) * int(b[j])
    elif i == 1:
      if j == 0:
        thr += (int(a[i]) * 10) * int(b[j])
      elif j == 1:
        two += (int(a[i]) * 10) * int(b[j])
      else:
        one += (int(a[i]) * 10) * int(b[j])
    else:
      if j == 0:
        thr += int(a[i]) * int(b[j])
      elif j == 1:
        two += int(a[i]) * int(b[j])
      else:
        one += int(a[i]) * int(b[j])

answer += one + (two * 10) + (thr * 100)
print(one)
print(two)
print(thr)
print(answer)
```

