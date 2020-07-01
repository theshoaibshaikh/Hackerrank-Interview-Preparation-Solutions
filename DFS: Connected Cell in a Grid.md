# DFS: Connected Cell in a Grid

### Problem
Consider a matrix where each cell contains either a 0 or a 1 and any cell containing a 1 is called a filled cell. Two cells are said to be connected if they are adjacent to each other horizontally, vertically, or diagonally.
<br>
Cells adjacent to filled cells:<br>
If one or more filled cells are also connected, they form a region. Note that each cell in a region is connected to at least one other cell in the region but is not necessarily directly connected to all the other cells in the region.

### Function Description

Complete the function maxRegion in the editor below. It must return an integer value, the size of the largest region.
<br>
maxRegion has the following parameter(s):
<br>
* **grid**: a two dimensional array of integers

### Solution

```python

#recursive function to check connection
def connected(grid,i,j):
    #check i and j in range
    if not (0 <= i < len(grid)) or not (0 <= j < len(grid[0])):
        return 0
    
    #check not filled cell
    if grid[i][j]!=1:
        return 0

    max_count=1
    grid[i][j]=-1

    for m in range(i-1,i+2):
        for n in range(j-1,j+2):
            if not(m == i and n == j):
                max_count+=connected(grid,m,n)
    return max_count


# Complete the maxRegion function below.
def maxRegion(grid):
    max_count=0
    for i in range(len(grid)):
        for j in range(len(grid[0])):
            #check connection recursively
            max_count=max(max_count,connected(grid,i,j)) 
                
    return max_count
```
