# Viral Advertising

### Problem

HackerLand Enterprise is adopting a new viral advertising strategy. When they launch a new product, they advertise it to exactly 5 people on social media.
<br>
On the first day, half of those  people ***(i.e., floor(5/2)=2)*** like the advertisement and each shares it with 3 of their friends. At the beginning of the second day, floor(5/2)*3=2*3 people receive the advertisement.
<br><br>
Each day, ***floor(recipients/2)*** of the recipients like the advertisement and will share it with 3 friends on the following day. Assuming nobody receives the advertisement twice, determine how many people have liked the ad by the end of a given day, beginning with launch day as day 1.
<br>
For example, assume you want to know how many have liked the ad by the end of the 5th day.
<br>
<br>
Day | Shared | Liked | Cumulative
----|--------|-------|------------
1   |   5    | 2     |  2
2   |   6    | 3     |  5
3   |   9    | 4     |  9
4   |  12    | 6     | 15
5   |  18    | 9     | 24
<br>
The cumulative number of likes is 24.

### Function Description
Complete the viralAdvertising function in the editor below. It should return the cumulative number of people who have liked the ad at a given time.

viralAdvertising has the following parameter(s):

* n: the integer number of days

### Solution

```python
def viralAdvertising(n):
    k=5
    count=0
    for i in range(n):
        k=math.floor(k/2)
        count+=k
        k=k*3
    return count
```
