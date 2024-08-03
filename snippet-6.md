# snippet-6

Consider the Java code given below, and choose the correct option/s suitable for Line 1.

```java
public class Show{
    public <T> void display(T[] elements) {
        for (T element : elements){
            System.out.println(element);
        }
        System.out.println();
    }
}
public class Example{
    public static void main(String args[]) {
        ----------------------------- //Line 1
        Show obj1=new Show();
        obj1.display(arr1);
    }
}

```

```

1. Integer[] arr1 = {10, 20, 30, 40, 50};
2. String[] arr1 = {"IIT","Madras","Java","Programming"};
3. int[] arr1 = { 10, 20, 30, 40, 50 };
4. double[] arr1= {20.5,30.7,56.6,67.8,0.25};
```

Solution: The type variable allows any type of array object. Option 1: Integer object array can be passed to the type variable . Option 2: String object array can be passed to the type variable . Option 3: int primitive type array passed to the type variable is invalid. Option 4: double primitive type array passed to the type variable is invalid.
