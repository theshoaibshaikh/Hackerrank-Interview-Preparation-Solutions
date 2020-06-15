# Mark and Toys
## Problem
Mark and Jane are very happy after having their first child. Their son loves toys, so Mark wants to buy some. There are a number of different toys lying in front of him, tagged with their prices. Mark has only a certain amount to spend, and he wants to maximize the number of toys he buys with this money.<br>
Given a list of prices and an amount to spend, what is the maximum number of toys Mark can buy? For example, if prices=[1,2,3,4] and Mark has k=7 to spend, he can buy items [1,2,3] for 6, or [3,4] for 7 units of currency. He would choose the first group of 3 items.

## Function Description

Complete the function maximumToys in the editor below. It should return an integer representing the maximum number of toys Mark can purchase. <br>
maximumToys has the following parameter(s):<br>

prices: an array of integers representing toy prices <br>
k: an integer, Mark's budget

## Solution:
```python
def maximumToys(prices, k):
    sorted_prices=sorted(prices)
    cost=0
    count=0
    for p in sorted_prices:
        cost=cost+p
        if cost<k:
            count+=1
    return count
```
