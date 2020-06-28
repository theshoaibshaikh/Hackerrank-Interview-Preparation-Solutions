# Recursion: Fibonacci Numbers

### Problem

The Fibonacci Sequence
<br>
The Fibonacci sequence appears in nature all around us, in the arrangement of seeds in a sunflower and the spiral of a nautilus for example.
<br>
The Fibonacci sequence begins with fibonacci(0)=0 and fibonacci(1)=1 as its first and second terms. After these first two elements, each subsequent element is equal to the sum of the previous two elements.

### Function Description

Complete the recursive function fibonacci in the editor below. It must return the n th element in the Fibonacci sequence.
<br>
fibonacci has the following parameter(s):
* n: the integer index of the sequence to return

### Solution

```python

def fibonacci(n):

    if n==0:
        return 0
    if n==1:
        return 1
    
    return (fibonacci(n-1)+fibonacci(n-2))
    
```
