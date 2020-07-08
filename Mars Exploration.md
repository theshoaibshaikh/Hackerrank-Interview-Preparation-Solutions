# Mars Exploration

### Problem
Sami's spaceship crashed on Mars! She sends a series of SOS messages to Earth for help.<br>
Letters in some of the SOS messages are altered by cosmic radiation during transmission. Given the signal received by Earth as a string, s, determine how many letters of Sami's SOS have been changed by radiation.
<br>
For example, Earth receives SOSTOT. Sami's original message was SOSSOS. Two of the message characters were changed in transit.

### Function Description

Complete the marsExploration function in the editor below. It should return an integer representing the number of letters changed during transmission.
<br>
marsExploration has the following parameter(s):
<br>
* s: the string as received on Earth

### Solution
```python
def marsExploration(s):
    l=len(s)//3
    count=0
    for i in range(l):
        j=0
        if s[j+i*3]!='S':
            count+=1
        j+=1
        if s[j+i*3]!='O':
            count+=1
        j+=1
        if s[j+i*3]!='S':
            count+=1
    return count
```
