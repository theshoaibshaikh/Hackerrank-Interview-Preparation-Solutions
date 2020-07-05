# Recursive Digit Sum

### Problem

We define super digit of an integer **x** using the following rules:
<br>
Given an integer, we need to find the super digit of the integer.
<br>
* If x has only 1 digit, then its super digit is x.
* Otherwise, the super digit of x is equal to the super digit of the sum of the digits of x.

### Function Description
Complete the function superDigit in the editor below. It must return the calculated super digit as an integer.
<br>
superDigit has the following parameter(s):
<br>
* **n:** a string representation of an integer
* **k:** an integer, the times to concatenate n to make p

### Solution

```python
#The Digit Sum of a Number to Base 10 is Equivalent to Its Remainder Upon Division by 9
def superDigit(n, k):
    n=int(n)
    x = n * k % 9
    return (x or 9) #return x or 9 if x is 0 
```
