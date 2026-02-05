## 2047B - Replace Character
### the code which got accepted
```py
from collections import Counter
t = int(input())
for _ in range(t):
    n = int(input())
    s = input().strip()
    freq = Counter(s)
    maxfr = max(freq.values())
    target = max(chr for chr in freq if freq[chr] == maxfr)
    minfr = min(freq.values())
    to_change = min(chr for chr in freq if freq[chr] == minfr)
    slist = list(s)
    for i in range(n):
        if slist[i] == to_change:
            slist[i] = target
            break
    print(''.join(slist))
```
