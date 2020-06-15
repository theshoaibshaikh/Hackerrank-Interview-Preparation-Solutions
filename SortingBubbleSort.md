# Sorting: Bubble Sort

## Problem:
Consider the following version of Bubble Sort:
```
for (int i = 0; i < n; i++) {
    
    for (int j = 0; j < n - 1; j++) {
        // Swap adjacent elements if they are in decreasing order
        if (a[j] > a[j + 1]) {
            swap(a[j], a[j + 1]);
        }
    }
    
}
```

Given an array of integers, sort the array in ascending order using the Bubble Sort algorithm above. Once sorted, print the following three lines:<br>

Array is sorted in numSwaps swaps., where numSwaps is the number of swaps that took place.<br>
First Element: firstElement, where firstElement is the first element in the sorted array.<br>
Last Element: lastElement, where lastElement is the last element in the sorted array.<br>

## Function Description

Complete the function countSwaps in the editor below. It should print the three lines required, then return.<br>
countSwaps has the following parameter(s):<br>
* a: an array of integers .

## Solution:

```python
def countSwaps(a):
    count=0
    l=len(a)
    for i in range(0,l):
        for j in range(0,l-1):
            if a[j]>a[j+1]:
                a[j],a[j+1]=a[j+1],a[j]
                count+=1
    print("Array is sorted in {} swaps.".format(count))
    print("First Element: {}".format(a[0]))
    print("Last Element: {}".format(a[l-1]))
 ```
