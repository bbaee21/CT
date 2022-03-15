# 프로그래머스 

> 행렬덧셈 문제
>
> 행, 열 크기가 같은 두 행렬의 같은 행, 같은 열의 값을 서로 더한 결과를 반환하는 함수 만들기

1. 이중 반복으로 리스트 다 언팩킹 하기
2. 범위는 리스트안 인자의 수만큼만 반복. 중요쓰
3. 숫자를 더하는데, 단순히 순서대로 더하는게 아니라 인덱스 활용해서 더해주기
4. 결과 값 반환하기

```python
def solution(arr1, arr2):
    answer = []
    for i in range(len(arr1)):
        total = []
        for j in range(len(arr1[i])):
            total.append(arr1[i][j] + arr2[i][j])
        answer.append(total)
    return answer
```

