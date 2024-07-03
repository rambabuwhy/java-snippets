# snippet-3

Method hiding or static method overriding&#x20;

```java
class SuperClass {
    static void staticMethod() {
        System.out.println("Static method in SuperClass");
    }
}

class SubClass extends SuperClass {
    static void staticMethod() {
        System.out.println("Static method in SubClass");
    }
}

public class Main {
    public static void main(String[] args) {
        SuperClass superClass = new SuperClass();
        SuperClass subClassAsSuper = new SubClass();
        SubClass subClass = new SubClass();

        superClass.staticMethod(); // Calls SuperClass's staticMethod
        subClassAsSuper.staticMethod(); // Still calls SuperClass's staticMethod
        subClass.staticMethod(); // Calls SubClass's staticMethod
    }
}

```

## Answer:

Static method in SuperClass

Static method in SuperClass

Static method in SubClass

## Solution:

In this example:

* `superClass.staticMethod()` calls the `staticMethod` in `SuperClass`.
* `subClassAsSuper.staticMethod()` calls the `staticMethod` in `SuperClass`, because the type of `subClassAsSuper` is `SuperClass`, even though it holds an instance of `SubClass`.
* `subClass.staticMethod()` calls the `staticMethod` in `SubClass`.

This demonstrates that the static method in the superclass is hidden by the static method in the subclass, but it is not overridden. The method called depends on the type of the reference, not the type of the object.

