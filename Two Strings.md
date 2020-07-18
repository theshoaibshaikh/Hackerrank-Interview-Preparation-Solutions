# Two Strings

### Problem

Given two strings, determine if they share a common substring. A substring may be as small as one character.

For example, the words "a", "and", "art" share the common substring a. The words "be" and "cat" do not share a substring.

### Function Description

Complete the function twoStrings in the editor below. It should return a string, either YES or NO based on whether the strings share a common substring.
<br>
twoStrings has the following parameter(s):
<br>
* s1, s2: two strings to analyze.

### Solution

```python
def twoStrings(s1, s2):
    set1=set(s1)
    set2=set(s2)

    a=set1.intersection(set2)
    if len(a)!=0:
        return "YES"
    else:
        return "NO"
```
