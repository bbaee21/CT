# Queue using Two Stacks



```
https://www.hackerrank.com/challenges/one-week-preparation-kit-queue-using-two-stacks/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-five
```



```
q = int(input())

stackpush = []
stackdelete = []

for i in range(q):
    t = list(input().split())
    
    if t[0] == "1":
        stackpush.append(t[1])
        
    elif t[0] == "2":
        if not stackdelete:
            while stackpush:
                stackdelete.append(stackpush.pop())
        stackdelete.pop()
        
    else:
        if not stackdelete:
            while stackpush:
                stackdelete.append(stackpush.pop())
        print(stackdelete[-1])   
```

