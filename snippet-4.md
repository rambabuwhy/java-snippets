# snippet-4

final overriding

```java
class SuperClass {
    final void finalMethod() {
        System.out.println("This is a final method in SuperClass");
    }
}

class SubClass extends SuperClass {
    // Trying to override the final method will result in a compilation error
    // void finalMethod() {
    //     System.out.println("Attempting to override final method in SubClass");
    // }
}

public class Main {
    public static void main(String[] args) {
        SubClass subClass = new SubClass();
        subClass.finalMethod(); // Calls the final method in SuperClass
    }
}

```

Answer:

compilation error:  Trying to override the final method will result in a compilation error
