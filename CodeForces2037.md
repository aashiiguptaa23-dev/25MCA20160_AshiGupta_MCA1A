## 2037C - Superultra's Favorite Permutation
### the accepted code
```py
n = int(input())
for _ in range(n):
    size = int(input())
    if size == 2 or size == 3 or size == 4:
        print(-1)
        continue
 
    print(2, end=' ')
    
    if size > 5:
        for i in range(6, size + 1, 2):
            print(i, end=' ')
 
    print(4, end=' ')
    print(5, end=' ')
 
    for i in range(1,size + 1, 2):
        if i == 5:
            continue
        print(i, end=' ')
    print()
```




