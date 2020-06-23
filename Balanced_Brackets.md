# Balanced Brackets

**Problem** <br>
A bracket is considered to be any one of the following characters: (, ), {, }, [, or ].<br>
<br>
Two brackets are considered to be a matched pair if the an opening bracket (i.e., (, [, or {) occurs to the left of a closing bracket (i.e., ), ], or }) of the exact same type. There are three types of matched pairs of brackets: [], {}, and ().<br>
<br>
A matching pair of brackets is not balanced if the set of brackets it encloses are not matched. For example, {[(])} is not balanced because the contents in between { and } are not balanced. The pair of square brackets encloses a single, unbalanced opening bracket, (, and the pair of parentheses encloses a single, unbalanced closing square bracket, ].<br>
<br>
By this logic, we say a sequence of brackets is balanced if the following conditions are met:<br>
* It contains no unmatched brackets.
* The subset of brackets enclosed within the confines of a matched pair of brackets is also a matched pair of brackets.

Given n strings of brackets, determine whether each sequence of brackets is balanced. If a string is balanced, return YES. Otherwise, return NO.

**Function Description**

Complete the function isBalanced in the editor below. It must return a string: YES if the sequence is balanced or NO if it is not.
<br>
isBalanced has the following parameter(s):

* s: a string of brackets

**Solution** <br>

```python
def isBalanced(s):
    opBrack=['[','{','(']
    clBrack=[']','}',')']

    st=[] #stack 
    for ch in s:
        #if opening bracket then push
        if ch in opBrack:
            st.append(ch)
        else:
            #if closing bracket then getting it's index from clBrack
            pos=clBrack.index(ch) 
            if len(st)!=0 and opBrack[pos] == st[-1]:
                st.pop()
            else:
                return "NO"
    if len(st)==0:
        return "YES"
    else:
        return "NO"
```
