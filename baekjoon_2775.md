# baekjoon_2775

># 부녀회장이 될테야



```
T = int(input())

for tc in range(1, T + 1):
    floor = int(input())
    room = int(input())
	
	# 0층일 때 각 호 수에 있는 사람 수
    zero = [i for i in range(1, room + 1)]
	
	# 각 층 만큼 반복
    for j in range(floor):
    	# 호수만큼 반복
        for k in range(1, room):
        	# n층의 i호의 사람 수는 n-1 층의 i호까지의 사람 수 합이므로,
            zero[k] += zero[k - 1]
    print(zero[-1])
```



