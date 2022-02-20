# Mock Test - Find the Median



```
def findMedian(arr):
    # Write your code here
    arr.sort()
    
    median_idx = len(arr) // 2
    
    result = arr[median_idx]
    
    return result
```



```
주어진 배열에서 중간값 찾는 문제
홀수 배열이 주어지니, 중간값에 해당하는 인덱스 찾으려고 접근

1
우선 sort() 함수를 통해 오름차순 정렬
(ex. [1, 3, 4, 2, 5] => [1, 2, 3, 4, 5])
2
중간값은 가운데 위치함. 그리고 해당 인덱스는 배열에 있는 숫자의 개수에서 2로 나눴을 때 몫인 것을 확인.
(ex. [1, 2, 3, 4, 5] => 5개의 수, 가운데 값은 3 / 3의 인덱스는 2 => 5 / 2 몫 2)
3
결과값을 출력할 result 변수에 중간값 담고 출력
```

