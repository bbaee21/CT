# baekjoon_1929

> 소수구하기
>
> M이상 N이하의 소수를 모두 출력하는 프로그램을 작성하시오.





* 실패코드
  * 에라토스네테스의 체 개념만 확인하고, 바로 적용함
  * 실패

```
primes = []
a = [False, False] + [True] * (e - 1)

for i in range(2, e + 1):

    if a[i]:
        primes.append(i)
        for j in range(2 * i, e + 1, i):
            a[j] = False

print(primes)
```



* 성공 코드

```
def Prime(s, e):
    if e < 2:
        return []

    # 0, 1은 제외니까 false 박아주고 시작한다.
    era = [False, False] + [True] * (e - 1)

    # 2부터 시작해서 소수 구하기 쉽게,
    # 소수 구할 때 2 부터 구하는 숫자 / 2 까지 나눴을 때, 나누어지는 숫자가 없으면 소수다.
    # 그래서 루트 해당 숫자 까지 살펴 보면 된다.
    for i in range(2, int(e ** 0.5) + 1):
        if era[i]:
            # 해당 숫자의 배수인 것들 다 false로 변경
            era[i * 2 :: i] = [False] * ((e - i) // i)


    # 2 안나오게..? / s-> 시작점 숫자보다 작은건 안나오게
    return [i for i, v in enumerate(era) if v and i >= s]

s, e = map(int, input().split())
P = Prime(s, e)

for p in P:
    print(p)
```

