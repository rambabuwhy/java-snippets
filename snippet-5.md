# snippet-5

names.put(40, "four"); \
names.put(10, "one"); \
names.put(30, "three"); \
names.put(20, "two"); \
System.out.println(names);

Identify the output for the following given cases:

1. LINE 1 is Map\<Integer, String> names = new LinkedHashMap\<Integer, String>();
2. LINE 1 is Map\<Integer, String> names = new TreeMap\<Integer, String>();
3. LINE 1 is Map\<Integer, String> names = new HashMap\<Integer, String>();



## Answer:

In case 1: prints {40=four, 10=one, 30=three, 20=two} \
In case 2: prints {10=one, 20=two, 30=three, 40=four}\
In case 3: prints all four key-value pairs; however, the order cannot be deter- mined
