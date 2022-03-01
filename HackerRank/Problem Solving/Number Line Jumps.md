# Number Line Jumps

```
https://www.hackerrank.com/challenges/kangaroo/problem?isFullScreen=true
```



```
def kangaroo(x1, v1, x2, v2):
    # Write your code here
    
    while True:
        if v1 <= v2:
            return 'NO'
        x1 += v1
        x2 += v2
            
        if x1 == x2:
            return 'YES'
            break
        if x1 > x2:
            return 'NO'
```

