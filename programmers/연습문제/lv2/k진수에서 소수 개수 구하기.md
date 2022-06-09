# k진수에서 소수 개수 구하기



```
https://programmers.co.kr/learn/courses/30/lessons/92335?language=python3
```



```
def trans(n, r):
    base = ''
    while n > 0:
        n, mod = divmod(n, r)
        base += str(mod)
    return base[::-1]

def check_prime(n):
    if n == 1:
        return False
    elif n == 2:
        return True
    
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True


def solution(n, k):
    n = trans(n, k)
    ls = str(n).split("0")
    ls = list(filter(lambda x: x != '', ls))
    ls = list(map(lambda x: check_prime(int(x)), ls))
    
    answer = ls.count(True)
    return answer
```

