# Minimum Swaps 2

### Problem:
You are given an unordered array consisting of consecutive integers  [1, 2, 3, ..., n] without any duplicates. You are allowed to swap any two elements. You need to find the minimum number of swaps required to sort the array in ascending order.
<br>
For example, given the array  we perform the following steps:<br>

i  | arr                     | swap (indices)  
-- | ----------------------- | ------------------
0  | [7, 1, 3, 2, 4, 5, 6]   | swap (0,3)      
1  | [2, 1, 3, 7, 4, 5, 6]   | swap (0,1)      
2  | [1, 2, 3, 7, 4, 5, 6]   | swap (3,4)      
3  | [1, 2, 3, 4, 7, 5, 6]   | swap (4,5)      
4  | [1, 2, 3, 4, 5, 7, 6]   | swap (5,6)      
5  | [1, 2, 3, 4, 5, 6, 7]   |                

<br>
It took 5 swaps to sort the array.          <br>

### Algoithm:
1. For i=0..length(arr)
2. if i+1 == element at i <br>
   then i++ <br>
   else     <br>
      swap(element at i, element at element value-1)   <br>
      swap_count++ <br>

### Solution:
```python
def minimumSwaps(arr):
    swap_count=0
    l=len(arr)
    i=0

    while(i<l):
        if i+1 != arr[i]:
            arr[arr[i]-1],arr[i]=arr[i],arr[arr[i]-1]
            swap_count+=1
        else:
            i+=1

    return swap_count
```
