# snippet-13

## serialize and deserialize:&#x20;

The code you provided is attempting to serialize and deserialize an object of the `Example` class using `ObjectOutputStream` and `ObjectInputStream`.&#x20;

1. **Implement `Serializable` interface** in the `Example` class.
2. **Ensure all fields in the class are serializable**. Since `String` and `int` are serializable, you don’t need to worry about them.

```java
import java.io.*;

// The Example class implements Serializable
class Example implements Serializable {
    String str;
    int x;

    Example(String str, int x){
        this.str = str;
        this.x = x;
    }

    public String getStr(){
        return str;
    }

    public int getX(){
        return x;
    }
}

public class Main{
    public static void main(String[] args) throws Exception {
        // Create an ObjectOutputStream to serialize the object
        ObjectOutputStream os = new ObjectOutputStream(new FileOutputStream("File.ser"));
        os.writeObject(new Example("Moon", 1));
        os.close(); // Close the stream after writing

        // Create an ObjectInputStream to deserialize the object
        FileInputStream fis = new FileInputStream("File.ser");
        ObjectInputStream ois = new ObjectInputStream(fis);
        Example e = (Example) ois.readObject();
        ois.close(); // Close the stream after reading

        // Print the deserialized object's data
        System.out.print(e.getStr() + "\n" + e.getX());
    }
}
```

#### Explanation:

* **`Serializable` Interface**: By implementing the `Serializable` interface, you are informing the Java runtime that the `Example` class can be serialized.
* **Stream Closure**: It’s a good practice to close the streams (`os`, `fis`, and `ois`) after their use to prevent resource leaks.

#### Output:

When you run this corrected code, the output will be:

```
Moon
1
```

