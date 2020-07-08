# Anagram

### Problem

Two words are anagrams of one another if their letters can be rearranged to form the other word.
<br>
In this challenge, you will be given a string. You must split it into two contiguous substrings, then determine the minimum number of characters to change to make the two substrings into anagrams of one another.
<br>
For example, given the string 'abccde', you would break it into two parts: 'abc' and 'cde'. Note that all letters have been used, the substrings are contiguous and their lengths are equal. Now you can change 'a' and 'b' in the first substring to 'd' and 'e' to have 'dec' and 'cde' which are anagrams. Two changes were necessary.

### Function Description

Complete the anagram function in the editor below. It should return the minimum number of characters to change to make the words anagrams, or -1 if it's not possible.
<br>
anagram has the following parameter(s):
<br>
* s: a string

### Solution

```python
def anagram(s):
    med=len(s)//2
    a=s[0:med]
    b=s[med:]

    if len(a)==len(b):
        ac=Counter(a)
        bc=Counter(b)
        d=ac-bc
        return len(list(d.elements()))
    else:
        return -1
```
