# Modified Kaprekar Numbers

### Problem: <a>https://www.hackerrank.com/challenges/kaprekar-numbers/problem</a>

### Solution:
```python
def kaprekarNumbers(p, q):
    kap=[]
    for i in range(p,q+1):
        d=len(str(i))
        square=str(int(math.pow(i,2)))
        
        #checking if length is not 1 or right part is not 0 before adding
        if len(square)!=1 and int(square[-d:])!=0:
            square=int(square[:len(square)-d])+int(square[-d:])
        
        if int(square)==i:
            kap.append(i)
            
    if len(kap)==0:
        print("INVALID RANGE")
    else:
        for i in kap:
            print(i, end=" ")
```
