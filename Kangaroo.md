# Kangaroo

### Problem

You are choreographing a circus show with various animals. For one act, you are given two kangaroos on a number line ready to jump in the positive direction (i.e, toward positive infinity).<br>

The first kangaroo starts at location x1 and moves at a rate of v1 meters per jump.<br>
The second kangaroo starts at location x2 and moves at a rate of v2 meters per jump.<br>

You have to figure out a way to get both kangaroos at the same location at the same time as part of the show. If it is possible, return YES, otherwise return NO.

### Function Description

Complete the function kangaroo in the editor below. It should return YES if they reach the same position at the same time, or NO if they don't.<br>

kangaroo has the following parameter(s):<br>
x1, v1: integers, starting position and jump distance for kangaroo 1<br>
x2, v2: integers, starting position and jump distance for kangaroo 2<br>

### Solution
```python
def kangaroo(x1, v1, x2, v2):
    for i in range(10000):
        if x1==x2:
            return "YES"
        else:
            x1=x1+v1
            x2=x2+v2

    return "NO"
```
