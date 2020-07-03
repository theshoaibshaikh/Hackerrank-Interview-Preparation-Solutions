# Strings: Making Anagrams

### Problem

Alice is taking a cryptography class and finding anagrams to be very useful. We consider two strings to be anagrams of each other if the first string's letters can be rearranged to form the second string. In other words, both strings must contain the same exact letters in the same exact frequency For example, bacdc and dcbac are anagrams, but bacdc and dcbad are not.
<br>
Alice decides on an encryption scheme involving two large strings where encryption is dependent on the minimum number of character deletions required to make the two strings anagrams. Can you help her find this number?
<br>
Given two strings, **a** and **b**, that may or may not be of the same length, determine the minimum number of character deletions required to make **a** and **b** anagrams.  Any characters can be deleted from either of the strings. 

### Function description
Complete the makeAnagram function in the editor below. It must return an integer representing the minimum total characters that must be deleted to make the strings anagrams.
<br>
makeAnagram has the following parameter(s):

* a: a string
* b: a string

### Solution
```python
def makeAnagram(a, b):
    #getting count of occurrences of elements
    a_count=Counter(a)
    b_count=Counter(b)

    ab=a_count - b_count
    bc=b_count - a_count
    
    abc=ab+bc
    
    return len(list(abc.elements()))
 ```
