# snippet-9

```java
import java.util.*;
public class Test{
    public static void main(String args[]) {
        LinkedList<String> obj = new LinkedList<String>();
        obj.add("A");
        obj.add("C");
        obj.add(0, "D");
        obj.add("B");
        Collections.sort(obj);
        System.out.println(obj);
    }
}

```

```
What will the output be?

[A, B, C, D]




```

Solution: \
\[A, B, C, D]\
Collections.sort(obj) sorts the elements of obj in ascending order.