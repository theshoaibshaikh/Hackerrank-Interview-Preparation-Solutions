# Flipping bits

### Problem

You will be given a list of 32 bit unsigned integers. Flip all the bits (1->0 and 0->1) and print the result as an unsigned integer.

### Function Description

Complete the flippingBits function in the editor below. It should return the unsigned decimal integer result.
<br>
flippingBits has the following parameter(s):
<br>
n: an integer
<br>

### Solution:
```python
def flippingBits(n):
    #converting to 32 bit binary
    nbin=format(n,'032b')
    ib_string=""
    #replacing 0 with 1 and 1 with 0
    for bit in nbin:
        if bit == "1":
            ib_string += "0"
        else:
            ib_string += "1"
    return int(ib_string,2) 
```
