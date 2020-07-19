# Greedy Florist

### Problem

A group of friends want to buy a bouquet of flowers. The florist wants to maximize his number of new customers and the money he makes. To do this, he decides he'll multiply the price of each flower by the number of that customer's previously purchased flowers plus 1. The first flower will be original price, <b>(0+1)*original price</b>, the next will be <b>(1+1)*original price</b> and so on.
<br>
Given the size of the group of friends, the number of flowers they want to purchase and the original prices of the flowers, determine the minimum cost to purchase all of the flowers.

### Function Description

Complete the getMinimumCost function in the editor below. It should return the minimum cost to purchase all of the flowers.
<br>
getMinimumCost has the following parameter(s):
<br>
* c: an array of integers representing the original price of each flower
* k: an integer, the number of friends

### Solution

```python
def getMinimumCost(k, c):
    c=sorted(c,reverse=True) #sort in rev
    prev_purch=0
    amount=0
    for i in range(len(c)):
        amount+=(prev_purch+1)*c[i]
        if (i+1)%k==0: #after one purchase turn of friends
            prev_purch+=1
    return amount
```
