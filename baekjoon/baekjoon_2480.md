# baekjoon_2480



```
https://www.acmicpc.net/problem/2480
```



```
fir, sec, thir = map(int, input().split())


if fir == sec == thir:
  print(10000 + fir * 1000)
elif fir == sec or sec == thir:
  print(1000 + sec * 100)
elif fir == thir:
  print(1000 + thir * 100)
else:
  print(max(fir, sec, thir) * 100)
```

