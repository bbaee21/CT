# Counting Sort 1



```
def countingSort(arr):
    # Write your code here
    cnt_list = [0] * 100
    
    
    for item in arr:
        cnt_list[item] += 1
        
    return cnt_list
```



```
카운팅 소트 문제. 배열에 있는 숫자의 갯수를 세서 반환한다.

1
문제에서 n -> 100이 주어졌기 때문에, 숫자를 셀 리스트에 100을 곱해서 만들어준다.
2
그 다음 arr배열을 돌면서 해당 숫자를 인덱스로 하는 cnt_list에 1을 더해준다.
3
마지막으로 반환
```

