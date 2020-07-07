# Larry's Array

### Problem
Larry has been given a permutation of a sequence of natural numbers incrementing from 1 as an array. He must determine whether the array can be sorted using the following operation any number of times:
* Choose any 3 consecutive indices and rotate their elements in such a way that ABC->BCA->CAB->ABC

### Function Description
Complete the larrysArray function in the editor below. It must return a string, either YES or NO.

larrysArray has the following parameter(s):
* **A:** an array of integers

### Logic:
1. For each element **i** in array, count numbers greater than **i** in **range(0 to i-1)**. 
2. If final count is even then return **YES** else return **NO**

### Solution
```python
def larrysArray(A):
    count=0
    for i in range(1,len(A)):
        for j in range(0,i):
            if A[j]>A[i]:
                count+=1
    if count%2==0:
        return "YES"
    else:
        return "NO"
```
