# Tower Breakers



```
https://www.hackerrank.com/challenges/one-week-preparation-kit-tower-breakers-1/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-three&h_r=next-challenge&h_v=zen
```



```
def towerBreakers(n, m):
    # Write your code here
    if n % 2 == 1 and m != 1:
        return 1
    return 2
```



```
타워 빼기 게임
최종 1, 움직일 수 없는 상황이면 진다.

n -> 타워의 수, m -> 타워에서 이동가능한 수
1
플레이어 1은 타워의 수가 짝수면 이길 수 없다.
n(타워) = 2, m(이동가능) = 4
플레이어 1 -> 타워1 2칸 --> 이동가능 2
플레이어 2 -> 타워2 2칸 --> 이동가능 2
----------------------
플레이어 1 -> 타워1 1칸 --> 이동가능 1 (이동불가)
플레이어 2 -> 타워2 1칸 --> 이동가능 1 (이동불가)
----------------------
플레이어 1은 이동할 수 없기 때문에 진다.

2
타워의 수가 홀수인 경우
n = 1, m = 5
플레이어 1이 1을 남겨두면 무조건 플레이어 1이 이긴다.
```

