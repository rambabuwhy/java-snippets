# snippet-10

```java
import java.util.*;
public class Example {
    public static void main(String[] args) {
        List<String> list1=new ArrayList<String>();
        list1.add("IITM");
        list1.add("Java");
        list1.add("Java");
        list1.add("Programming");
        Set<String> set1=new HashSet<String>(list1);//Line 1
        for (String string : set1) {
            System.out.println(string);
        }
    }
}
```

```
Compile time error at Line 1

This code generates output:
Java
Programming
IITM

This code generates output:
Java
Java
Programming
IITM

This code generates output:
null
null
null
```

Solution: \
<mark style="color:green;">**This code generates output:**</mark> \ <mark style="color:green;">**Java**</mark> \ <mark style="color:green;">**Programming**</mark> \ <mark style="color:green;">**IITM**</mark>\
\
Here, we pass an ArrayList object in the HashSet constructor in Line 1  Duplicate elements are skipped while adding elements to the set.
