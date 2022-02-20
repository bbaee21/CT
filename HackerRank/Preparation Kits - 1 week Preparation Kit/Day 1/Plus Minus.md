# Plus Minus



```
def plusMinus(arr):
    # Write your code here
    arr_cnt = len(arr)
    positive = 0
    negative = 0
    zero = 0
    
    for i in range(arr_cnt):
        if arr[i] > 0:
            positive += 1
        elif arr[i] < 0:
            negative += 1
        elif arr[i] == 0:
            zero += 1
            
    res_p = float(positive) / float(arr_cnt)
    res_n = float(negative) / float(arr_cnt)
    res_zero = float(zero) / float(arr_cnt)
            
    print(f'{res_p:.6f}')
    print(f'{res_n:.6f}')
    print(f'{res_zero:.6f}')
```



```
처음 positive, negative, zero 리스트로 만들고, 해당 하는 부분을 append 스택 채워넣듯이 한 다음,
리스트 갯수 세서 최종 나눠서 output 만들려고 접근.
근데 굳이 리스트에 넣고, 리스트 길이 재면 일 더 늘어나니까 
반복문 돌면서 양수, 음수, 0에 해당하면 += 1만 해주면 되니까 수정

마지막 출력에서 float(부동소수점), 소수점 자리 설정을 안해둬서 출력에서 실패.

출력방식(f'string)을 통한 소수점 표현방법 학습
```

