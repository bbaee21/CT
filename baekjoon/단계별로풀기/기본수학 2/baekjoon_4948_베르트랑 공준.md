# baekjoon_4948_베르트랑 공준



```
https://www.acmicpc.net/problem/4948
```



```
def sosu(n):
    if n == 1:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True							

num_list = list(range(2, 246912))		
res = []								

for i in num_list:						
    if sosu(i):							
        res.append(i)					

n = int(input())

while True:
    cnt = 0					
    if n == 0 :
            break
    for i in res:			
        if n < i <= 2 * n:		
            cnt += 1		
    print(cnt)
    n = int(input())
```

