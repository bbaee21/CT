# Mini-Max Sum



```
def miniMaxSum(arr):
    # Write your code here
    max_num = max(arr)
    min_num = min(arr)
    
    arr_sum = 0
    max_sum = 0
    min_sum = 0
    
    for i in range(len(arr)):
        arr_sum += arr[i]
    
    max_sum = arr_sum - min_num
    min_sum = arr_sum - max_num
    
    print(min_sum, max_sum)
```



```
input으로 5개의 정수가 담긴 array, arr이 주어진다.
arr에 담긴 5개 숫자 조합에서 합이 가장 큰 조합, 작은 조합을 찾는 문제이다.

1
우선 arr 배열의 합을 구하고, 배열에서 가장 큰 숫자를 빼는 경우와 가장 작은 숫자를 빼는 경우를 생각했다.
큰 합은 작은 숫자를 빼는 것, 작은 합은 큰 숫자를 빼면 되기 때문이다.
(ex. [1, 2, 3, 4] -> max : (1+2+3+4) - 1 = 9 / min : (1+2+3+4) - 4 = 6)
2
max_num, min_num 변수를 만들어서 max와 min 함수를 통해 큰/작은 숫자를 할당했다.
3
그리고, arr 배열의 합을 담은 arr_sum 변수를 만들고, 최종 계산을 위한 max_sum, min_sum 변수를 통해 계산했다.
4
마지막으로 출력
---------------------
쉬운 문제인데,, 항상 처음 접근 / 머리로 생각하는 부분에서 어렵게 생각하는게 좀 문제인 것 같다.
더 노력해야한다.
```



