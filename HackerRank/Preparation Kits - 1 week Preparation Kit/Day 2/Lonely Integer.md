# Lonely Integer



```
def lonelyinteger(a):
    # Write your code here
    
    res = 0
    
    for num in a:
        res = res ^ num

        
    return res
```



```
주어진 배열에서 중복되는 수가 없는 숫자를 반환해야하는 문제.
(ex. [1, 2, 3, 1, 2, 3, 4] / => 4)

처음에 while, for 반복문을 통해 해결해보려고 했었다.
stack = [] 빈 배열을 두고, 
stack = [] + a a를 딥 카피해서 반복문 => 원래 배열 a와 비교
하지만.. 생각처럼 되지 않았다. 예외도 많고 while break 조건도 잘 생각하지 못했다.

인터넷의 도움을 빌렸다.. 하
XOR 비트 연산자를 통해 쉽게 해결할 수 있었다. 며칠 전 코딩테스트에서 XOR로 고생했었는데
다시 보면서 학습했다. 
이 문제에서 적용한 것은 x ^ x = 0 / x ^ 0 = x의 성질을 활용해서 문제를 풀 수 있었다.
비트가 같은 경우 0을 반환, 다를 땐 본인을 반환하는 XOR에 대해 학습할 수 있었다. 
```

