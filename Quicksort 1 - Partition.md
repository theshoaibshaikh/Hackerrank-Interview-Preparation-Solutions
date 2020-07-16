# Quicksort 1 - Partition

### Problem

The previous challenges covered Insertion Sort, which is a simple and intuitive sorting algorithm with a running time of O(n*n) . In these next few challenges, we're covering a divide-and-conquer algorithm called Quicksort (also known as Partition Sort). This challenge is a modified version of the algorithm that only addresses partitioning. It is implemented as follows:
<br>
Step 1: Divide
Choose some pivot element, p, and partition your unsorted array, arr, into three smaller arrays: left, right, and equal, where each element in left<p, each element in right>p, and each element in equal=p.

### Function Description

Complete the quickSort function in the editor below. It should return an array of integers as described above.
<br>
quickSort has the following parameter(s):
* arr: an array of integers where  is the pivot element

### Solution

```python
def quickSort(arr):
    piv=arr[0]

    ar1=[]
    ar2=[]
    ar3=[]
    for i in range(1,len(arr)):
        if arr[i]<piv:
            ar1.append(arr[i])
        elif arr[i]>piv:
            ar2.append(arr[i])
        else:
            ar3.append(arr[i])
    ar3.append(piv)
    return (ar1+ar3+ar2)
```
