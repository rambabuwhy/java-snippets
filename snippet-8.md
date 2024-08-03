# snippet-8

```java
import java.util.*;
public class Process{
    private int pid;
    public Process(int pid) {
        this.pid = pid;
    }   
    public int getPID() {
        return pid;
    }
}

public class FClass {
    public static void main(String[] args){
        Queue<Process> pq = new LinkedList<Process>();
        for (int i = 0; i < 5; i++)
            pq.add(new Process(i + 1000));
        while(!pq.isEmpty()) {
            Process curPorc = _____________; //LINE 1
            System.out.print(curPorc.getPID() + " -> ");
        }
    }
}
```

```
Identify the appropriate option(s) to ll in the blank at LINE 1,
such that the output is: 1000 -> 1001 -> 1002 -> 1003 -> 1004 ->


pq.peek()
pq.remove()
pq.poll()
pq.element()
```

Solution: \
pq.remove() \
pq.poll()\
\
Since the while loop checks for if the queue is empty, within the loop the statement at LINE must return the element from the front of the queue and remove it from the queue. Thus, option-2 and option-3 are correct.
