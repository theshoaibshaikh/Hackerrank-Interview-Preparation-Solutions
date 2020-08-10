# Left Rotation

### Problem
<a>https://www.hackerrank.com/challenges/array-left-rotation/problem</a>

### Solution

* **Java**
```java

static int[] leftRotate(int a[],int d)
    {
        int n=a.length;
        int b[]=new int[n];
        int j=0;
        for(int i=d;i<n;i++)
        {
            b[j]=a[i];
            j++;
        }
        for(int i=0;i<d;i++)
        {
            b[j]=a[i];
            j++;
        }
        return b;
    }

````
