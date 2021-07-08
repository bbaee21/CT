# baekjoon_11653

> 정수 N이 주어졌을 때, 소인수분해하는 프로그램을 작성하시오.





```
N = int(input())

def Solution(N):
    jjack = 2
	
	# 1이 나올 때까지 반복
    while N != 1:
    	# 소인수 분해, 2(짝수)로 시작
    	# 나눠지는 경우 jjack 으로 출력
        if N % jjack == 0:
            N = N / jjack
            print(jjack)
        else:
        	# 안 나눠지는 경우 +1 해서 다시 반복
            jjack += 1

Solution(N)
```