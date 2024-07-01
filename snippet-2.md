# snippet-2

What is the output of the following Java code?

```java
public class FClass{
    public static void main(String[] args) {
        int[] a = {1, 2, 3};
        int[] b = a;
        System.out.print(a == b);
    }
}
```

Answer: true

Solution:&#x20;

It prints true. The == operator compares whether a and b are referring to the same memory location.
