# HackerRank in a String!

### Problem
<a>https://www.hackerrank.com/challenges/hackerrank-in-a-string/problem</a>

### Solution

* **Python**
```python
def hackerrankInString(s):
    count=0
    s1="hackerrank"
    for ch in s:
        if ch==s1[count]:
            count+=1
        if count==len(s1):
            break
    if count == len(s1):
        return "YES"
    else:
        return "NO"

```

* **Java**
```java
static String hackerrankInString(String s) {
        StringBuilder sb=new StringBuilder("hackerrank");
        int count=0;
        char s_chars[]=s.toCharArray();
        for(char ch:s_chars)
        {   
            if(ch==sb.charAt(count))
                count++;
            if(count == sb.length())
                break;
        }
        
        if(count == sb.length())
            return "YES";
        else
            return "NO";

    }
```
