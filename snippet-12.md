# snippet-12

Explain the Java code line:

```java
Stream<String> fruitstream=fruits.stream();
IntSummaryStatistics summary = fruitstream.collect(Collectors.summarizingInt(String::length));
```



The code snippet you've provided attempts to create a summary of the lengths of the strings in a `Stream<String>`, but there is an issue. Once you convert the `List<String>` to a `Stream<String>` with `fruits.stream()`, the stream can only be consumed once. Therefore, you can't use the same stream after it's been used.

Here is a corrected version of your code:

```java
List<String> fruits = Arrays.asList("apple", "banana", "orange");

IntSummaryStatistics summary = fruits.stream()
    .collect(Collectors.summarizingInt(String::length));

System.out.println("Count: " + summary.getCount());
System.out.println("Sum of lengths: " + summary.getSum());
System.out.println("Average length: " + summary.getAverage());
System.out.println("Max length: " + summary.getMax());
System.out.println("Min length: " + summary.getMin());
```

#### Explanation:

* `List<String> fruits = Arrays.asList("apple", "banana", "orange");`: Creates a list of strings.
* `fruits.stream()`: Converts the list into a stream.
* `.collect(Collectors.summarizingInt(String::length))`: Collects statistics (count, sum, average, max, and min) based on the lengths of the strings.
* `summary.getCount()`, `summary.getSum()`, etc.: Retrieve the respective statistics.

This corrected code will work as expected and print out the summary statistics for the lengths of the strings in the list.
