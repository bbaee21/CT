# 문자열 내 p와 y의 개수



```
def solution(s):
    answer = True
    
    p_cnt = 0
    y_cnt = 0
    
    for i in range(len(s)):
        if s[i] == 'p' or s[i] == 'P':
            p_cnt += 1
        elif s[i] == 'y' or s[i] == 'Y':
            y_cnt += 1
            
    if p_cnt != y_cnt:
        answer = False
    elif p_cnt == 0 and y_cnt == 0:
        answer = True

    return answer
```

