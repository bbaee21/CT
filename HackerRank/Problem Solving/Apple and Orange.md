# Apple and Orange

```
https://www.hackerrank.com/challenges/apple-and-orange/problem?isFullScreen=true
```



```
def countApplesAndOranges(s, t, a, b, apples, oranges):
    # Write your code here
    
    count_apple = 0
    count_orange = 0
    
    
    for i in range(len(apples)):
        if a + apples[i] >= s and a + apples[i] <= t:
            count_apple += 1
            
    for j in range(len(oranges)):
        if b + oranges[j] >= s and b + oranges[j] <= t:
            count_orange += 1
            
    print(count_apple)
    print(count_orange)
```

