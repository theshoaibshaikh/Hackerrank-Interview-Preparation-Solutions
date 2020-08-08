# Super Reduced String

### Problem:
<a>https://www.hackerrank.com/challenges/reduced-string/problem</a>

### Solution:

* ***python***
```python
def superReducedString(s):
    sl = []
 
    for c in s:
        if sl==[]:
            sl.append(c)
        else:
            if sl[-1] == c:
                sl.pop()
            else:
                sl.append(c)
                
    if len(sl)==0:
        return "Empty String"
    else:
        return ''.join(sl)
```

* ***java***
```java
static String superReducedString(String s) {
        StringBuilder sb=new StringBuilder(s);
        boolean flag=true;
        while(flag)
        {
            flag=false;
            for(int i=0;i<sb.length()-1;i++)
            {
                if(sb.charAt(i)==sb.charAt(i+1))
                {
                    sb.delete(i,i+2);
                    flag=true;
                }
            }
            if(!flag)
                break;
        }
        if(sb.length()==0)
            return "Empty String";
        else
            return sb.toString();
    }
```
