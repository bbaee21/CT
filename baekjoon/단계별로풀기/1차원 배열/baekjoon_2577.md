# baekjoon_2577



````
https://www.acmicpc.net/problem/2577
````



```
A = int(input())
B = int(input())
C = int(input())

X = str(A * B * C)

nums = {'0' : 0, '1' : 0, '2' : 0, '3' : 0, '4' : 0, '5' : 0, '6' : 0, '7' : 0, '8' : 0, '9' : 0}

for num in X:
  nums[num] += 1

for key, value in nums.items():
  print(value)
```

