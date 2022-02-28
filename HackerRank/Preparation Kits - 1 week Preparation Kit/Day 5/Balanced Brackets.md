# Balanced Brackets



```
https://www.hackerrank.com/challenges/one-week-preparation-kit-balanced-brackets/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-five
```

1차 시도

```
def isBalanced(s):
    stack = []
    answer = "YES"

    for i in range(len(s)):
        if s[i] == '{':
            stack.append('{')
        elif s[i] == '(':
            stack.append("(")
        elif s[i] == '[':
            stack.append("[")
        elif s[i] == ']':
            if len(stack) and stack[-1] == '[':
                stack.pop()
            else:
                answer = "NO"
        elif s[i] == ')':
            if len(stack) and stack[-1] == '(':
                stack.pop()
            else:
                answer = "NO"
        elif s[i] == '}':
            if len(stack) and stack[-1] == '{':
                stack.pop()
            else:
                answer = "NO"
    return answer
```

