# Minimum Absolute Difference in an Array

### Problem

Consider an array of integers, **arr=[arr[0],arr[1],....,arr[n-1]]**. We define the absolute difference between two elements, a[i] and a[j](where i!=j), to be the absolute value of a[i]-a[j].
Given an array of integers, find and print the minimum absolute difference between any two elements in the array. 

### Function Description

Complete the minimumAbsoluteDifference function in the editor below. It should return an integer that represents the minimum absolute difference between any pair of elements.
<br>
minimumAbsoluteDifference has the following parameter(s):
<br>
* **n**: an integer that represents the length of arr
* **arr**: an array of integers

### Solution

```python
def minimumAbsoluteDifference(arr):
    arr=sorted(arr)#sort array
    mindiff=abs(arr[0]-arr[1])#initialize min diff
    for i in range(0,len(arr)-1):
        #find difference between adjacent elements
        diff=abs(arr[i]-arr[i+1])     
        if diff < mindiff:
            mindiff=diff
    
    return mindiff
```
