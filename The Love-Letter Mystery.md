# The Love-Letter Mystery

### Problem

James found a love letter that his friend Harry has written to his girlfriend. James is a prankster, so he decides to meddle with the letter. He changes all the words in the letter into palindromes.
<br>
To do this, he follows two rules:
<br>
1. He can only reduce the value of a letter by 1, i.e. he can change d to c, but he cannot change c to d or d to b.
2. The letter a may not be reduced any further.
Each reduction in the value of any letter is counted as a single operation. Find the minimum number of operations required to convert a given string into a palindrome.
<br>
For example, given the string s = cde, the following two operations are performed: cde → cdd → cdc.

### Function Description
Complete the theLoveLetterMystery function in the editor below. It should return the integer representing the minimum number of operations needed to make the string a palindrome.
<br>
theLoveLetterMystery has the following parameter(s):
<br>
* s: a string

### Solution

```python
def theLoveLetterMystery(s):
    i=0
    j=len(s)-1
    count=0
    while i<j:
        count+=abs(ord(s[i]) - ord(s[j]))
        i+=1
        j-=1
    return count
```
