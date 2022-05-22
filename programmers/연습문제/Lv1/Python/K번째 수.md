# K번째 수



```
https://programmers.co.kr/learn/courses/30/lessons/42748
```



```
def solution(array, commands):
    answer = []
    i, j, k = [], [], []
    
    for m in range(len(commands)):
        i.append(commands[m][0])
        j.append(commands[m][1])
        k.append(commands[m][2])
    
    for l in range(len(i)):
        
        temp = array[i[l] - 1:j[l]]
        temp.sort()
        answer.append(temp[k[l] - 1])
    
    return answer
```

