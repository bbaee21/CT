# New Year Chaos



```
https://www.hackerrank.com/challenges/one-week-preparation-kit-new-year-chaos/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-four
```



```
def minimumBribes(q):
    # Write your code here
    bribe = 0
    
    for i in range(len(q) - 1, 0, -1):
        if q[i] != i + 1:
            if q[i - 1] == i + 1:
                bribe += 1
                q[i - 1], q[i] = q[i], q[i - 1]
            elif q[i - 2] == i + 1:
                bribe += 2
                q[i - 2], q[i - 1], q[i] = q[i - 1], q[i], q[i - 2]
            else:
                print("Too chaotic")
                return
    print(bribe)
```

