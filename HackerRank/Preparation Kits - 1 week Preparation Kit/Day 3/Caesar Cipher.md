# Caesar Cipher



```
https://www.hackerrank.com/challenges/one-week-preparation-kit-caesar-cipher-1/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-three
```



```
def caesarCipher(s, k):
    # Write your code here
    trans = []

    
    for char in s:
        trans.append(ord(char))
        
    for i in range(n):
        # uppercase - 65 - 90
        if 65 <= trans[i] <= 90:
            trans[i] = (65 + (trans[i] - 65 + k) % 26)
            # 65 - a
            # 65 - 65 = (0 + 3) % 26 = 3
            # 65 + 3 = 68
        # lowercase - 97 - 122
        elif 97 <= trans[i] <= 122:
            trans[i] = (97 + (trans[i] - 97 + k) % 26)
    
    res = "".join(map(chr, trans))
        
    return res
```

