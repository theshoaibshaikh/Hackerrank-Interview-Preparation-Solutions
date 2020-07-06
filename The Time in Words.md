# The Time in Words

### Problem
Given the time in numerals convert it into words.

### Function Description
Complete the timeInWords function in the editor below. It should return a time string as described.

timeInWords has the following parameter(s):

* h: an integer representing hour of the day
* m: an integer representing minutes after the hour

### Solution

```python
def timeInWords(h, m):
    words=["zero", "one", "two", "three", "four", 
            "five", "six", "seven", "eight", "nine", 
            "ten", "eleven", "twelve", "thirteen", 
            "fourteen", "fifteen", "sixteen",  
            "seventeen", "eighteen", "nineteen",  
            "twenty", "twenty one", "twenty two",  
            "twenty three", "twenty four",  
            "twenty five", "twenty six", "twenty seven", 
            "twenty eight", "twenty nine"]; 
    
    if m==0:
        time=words[h]+" o' clock"
    elif m==1:
        time="one minute past "+words[h]
    elif m==15:
        time="quarter past "+words[h]
    elif m==45:
        time="quarter to "+words[(h%12)+1]
    elif m==30:
        time="half past "+words[h]
    elif m<30:
        time=words[m]+" minutes past "+words[h]
    elif m>30:
        time=words[60-m]+" minutes to "+words[(h%12)+1]
    return time
```
