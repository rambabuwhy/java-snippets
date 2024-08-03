# snippet-7

```java
public class NumberFunction{
    public static <T extends Number> T max(T[] tArr){
        T max = tArr[0];
        for(int i = 0; i < tArr.length; i++) {
            if(tArr[i].doubleValue() > max.doubleValue()) {
                max = tArr[i];
            }
        }
        return max;
    }
}

public class FClass{
    public static void main(String[] args) {
        //LINE 1
        System.out.println(NumberFunction.max(arr));
    }
}
```



```
Identify the correct denition(s) for array arr for which the call NumberFunction.max(arr)
can return the maximum element from the array arr.

Integer[] arr = {2, 4, 1, 6, 3};
Double[] arr = {2.3, 4.2, 1.4, 2.6, 1.3};
Character[] arr = {'H', 'e', 'L', 'l', 'o'};
String[] arr = {"Apple", "test", "Apple", "Mango", "Orange"};
```

Solution: For function NumberFunction.max(arr), the type T is bounded by Number. Since Integer and Double both inherit from Number, function NumberFunction.max(arr) works correctly on them. However, it does not work for Character and String.
