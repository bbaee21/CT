# Zig Zag Sequence



```
def findZigZagSequence(a, n):
    a.sort()
    mid = int((n + 1) / 2)  # 수정 전
    mid = int(n // 2)  # 1 change
    a[mid], a[n-1] = a[n-1], a[mid]

    st = mid + 1
    ed = n - 1  # 수정 전
    ed = n - 2  # 2 change
    while(st <= ed):
        a[st], a[ed] = a[ed], a[st]
        st = st + 1
        ed = ed + 1  # 수정 전
        ed = ed - 1  # 3 change

    for i in range (n):
        if i == n-1:
            print(a[i])
        else:
            print(a[i], end = ' ')
    return

test_cases = int(input())
for cs in range (test_cases):
    n = int(input())
    a = list(map(int, input().split()))
    findZigZagSequence(a, n)
```



```
지그재그 반환 디버그 문제.
(ex. a = [2, 3, 5, 1, 4] => [1, 4, 5, 3, 2])

1
우선 가운데 인덱스 부분을 수정해줬다. 
첫 번째 수정의 경우 인덱스 지정이 잘못되어있었기 때문에 수정
홀수 배열이 주어지기 때문에, 가운데 인덱스는 n - 1 // 2 몫이다.
(ex. b = 5, [1, 2, 3, 4, 5] / => 5 - 1 // 2 = 2 / b[2] = 3, 가운데 인덱스)
2
앞선 라인에서 가운데 인덱스와 제일 끝 인덱스의 숫자를 변경해줬기 때문에
다음 변경될 끝 인덱스 ed는 -2를 해줘야 한다. (변경이 이뤄졌기 때문에 앞자리로 이동)
3
마지막 for 반복문 안에서는 끝에서 부터 한자리씩 앞으로 이동해야하기 때문에 ed - 1로 수정해줘야한다.
```

