# Super Reduced String

### Problem:
<a>https://www.hackerrank.com/challenges/reduced-string/problem</a>

### Solution:

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
