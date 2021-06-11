# baekjoon_1193





```
* 실패 코드

T = int(input())

temp_T = 0
cnt = 0

while True:
    cnt += 1
    T -= cnt

    if cnt > T:
        T += cnt
        cnt += 1
        break


if cnt % 2 == 0:
    print(f'{cnt-T}/{T}')
else:
    print(f'{T-cnt}/{T}')
```



```
* 통과

T = int(input())

temp_T = 0
cnt = 1

while T > cnt:
    T -= cnt
    cnt += 1

if cnt % 2 == 0:
    a = T
    b = cnt - T + 1
else:
    a = cnt - T + 1
    b = T

print(f'{a}/{b}')
```

