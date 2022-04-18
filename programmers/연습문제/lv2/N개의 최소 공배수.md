# N개의 최소 공배수



```
https://programmers.co.kr/learn/courses/30/lessons/12953?language=python3
```



```
def solution(arr):
    answer = 0
    number = 1
    
    while True:
        answer = max(arr) * number
        
        check = True
        
        for num in arr:
            if answer % num != 0:
                check = False
                break
        if check:
            break
            
        number += 1
    
    return answer
```

