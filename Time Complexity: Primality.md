# Time Complexity: Primality

### Problem

A prime is a natural number greater than **1** that has no positive divisors other than **1** and itself. Given **p** integers, determine the primality of each integer and print whether it is Prime or Not prime on a new line.

### Function Description

Complete the primality function in the editor below. It should return Prime if **n** is prime, or Not prime.<br>
primality has the following parameter(s):<br>
* n: an integer to test for primality

### Solution

```python
def primality(n):
    if n==1:
        return "Not prime"
    if n==2:
        return "Prime"

    #finding smallet p whose square is greater than equal to n
    p=math.ceil(math.sqrt(n))

    for i in range(2,p+1):
        if n%i==0:
            return "Not prime"
    return "Prime"
```
