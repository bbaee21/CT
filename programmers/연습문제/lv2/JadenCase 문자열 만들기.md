# JadenCase 문자열 만들기



```
https://programmers.co.kr/learn/courses/30/lessons/12951?language=python3#
```



```
def solution(s):
    answer = ''
    
    s = s.lower()
    ls_s = s.split(' ')
    
    for i in range(len(ls_s)):
        if ls_s[i] == '':
            answer += " "
            continue
        if ls_s[i] != '':
            if ls_s[i][0].isdigit():
                answer += ls_s[i]
        
            if ls_s[i][0].isalpha():
                upper_alpha = ls_s[i][0].upper()
                rest_ls = ls_s[i][1:]
                answer += (upper_alpha + rest_ls)
        answer += " "
        
    return answer[:-1]
```

