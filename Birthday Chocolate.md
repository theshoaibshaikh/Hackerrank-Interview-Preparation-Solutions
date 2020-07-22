# Birthday Chocolate

### Problem:
<a>https://www.hackerrank.com/challenges/the-birthday-bar/problem</a>

#### Solution:

```python
def birthday(s, d, m):
    count=0

    for i in range(len(s)-m+1):
        #print(s[i:i+m])
        total=sum(s[i:i+m])
        if total==d:
            count+=1
    return count
```
