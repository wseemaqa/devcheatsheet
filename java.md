---
Title: Java
Description: A Java cheat sheet for developers 
---

## Java Cheat Sheet

### JDK versions and release date

Here's a list of java versions and release date starting from Java 7

|JDK VERSION|RELEASE DATE|SUPPORT UNTIL|
|:----:|:------:|:------:|
|Java 7 (LTS)|July 2011|July 2019|
|Java 8 (LTS)|July 2014|March 2022|
|Java 9 |September 2017|March 2018|
|Java 10 | March 2018|September 2018|
|Java 11 (LTS)| September 2018 | September 2021
|Java 12| March 2019| September 2019
|Java 13 | September 2019| March 2020
|Java 14| March 2020| September 2020|
Java 15| September 2020 | March 2021|
|Java 16| March 2021| September 2021|
|Java 17 (LTS)| September 2021| September 2026|
|Java 18|March 2022|September 2022|
|Java 19| September 2022| March 2023|
|Java 20| March 2023| September 2023|
|Java 21| September 2023| September 2028|

### Data Types

Java Data types and Size

|Data Type|Category|Size|Range|Literals|Default|
|:----:|:------:|:------:|:------:|:------:|:------:|
|short|signed 16 bits|16|-32768 to 32767| |0|
|byte|assigned 8 bits|8|-128 to 127| |0|
|char|unsigned 16 bits|16|the complete unicode character set|''|\u0000|
|int|signed 32 bits|32|-2147483648 to 2147483647| |0|
|long|signed 64 bits|64|-9223372036854775808 to 9223372036854775807|L or l|0|
|float|32 bits|32|1.40239846e-45f to 3.40282347e+38f|F or f|0.0f|
|double|64 bits|64|4.94065645841246544e-324 to 1.79769313486231570e+308|D or d|0.0d|
|boolean|unsigned 8 bits|1|False (0) or True (1)|true/false |false|

### Declaring Variables, Methods and Classes

In java, variable, classes and methods can be declared with specific keywords, and the data type that define them.

Keywords:

- Public
- Static
- Final
- Private

### Compiling a Java program

When you create a program in java, the name of the class containing the main method must be the same name used to create the program. Ending with the .java file extension.

``
classNameProgram.java
``

call the java compiler to compile the program before executing

``
javac classNameProgram
``

Then execute the program with

``
java classNameProgram
``

### Declaring User Input

The most common way to declare input from a user is with the Scanner class, and the BufferedReader class.

Using the Scanner class

```java
Scanner userInput = new Scanner(system.in);

// with String data type
String s = userInput.nextLine();

// with int data type
int number = userInput.nextInt();

```

Using the BufferedReader class

```java
BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
String name = reader.readLine();
```

### Java operators

|Type|Operator|
|:------:|:------:|
|Ternary|?:|
|Unary|++x, –x, x++, x–, +x, –x, !, ~|
|Logical| &&, \|\||
|Assignment|=, +=, -=, *=, /=, %=, &=, ^=, |=, <<=, >>=, >>>=|
|Arithmetic|+, – , *, ? , %|
|Relational|<, >, <=, >=,==, !=|
|Shift|<<, >>, >>>|
|Bitwise|^, &, \||

### Java Loops

The java loops are divided into 3 types.

- For loops
- While loops
- Do-while loops

Using For loop

```java
public class MyClass {
    public static void main(String args[]) {
        int x = 0;
        for( x = 1 ; x <= 10 ; x++ ){
        System.out.println(x);
        }
    }
}
```

Using while loop

```java
public class MyClass {
    public static void main(String args[]) {
    long i = 0, fact = 1, num = 5 ;
    i = num ;
    while(num != 0)
    {
      fact = fact * num;
      --num;
    }
    System.out.println("The factorial of " + i + " is: " +fact);
    }
}
```

do-while loop

```java
public class MyClass {
    public static void main(String args[]) {
        char ch = 'A' ;
        do{
      System.out.println( ch + " " );
      ch++;
    } while(ch <= 'G');
    }
}
```

### Java String Methods

The java string methods are listed below

```java
String example1;
String example2;

String sample1 = example1.equals(example2); //compares the values
String sample2 = example1.equalsIgnoreCase() //compares the values ignoring the case
example1 = example1.length() //calculates length
example1 = example1.charAt(i) //extract i'th character
example1 = example1.toUpperCase() //returns string in ALL CAPS
example1 = example1.endsWith(); //Checks if string ends with the given suffix/char
example1 = example1.toCharArray(); // converts the string to a character type array
example1 = example1.toLowerCase() //returns string in ALL LOWERvCASE
example1==example2 //compares the address in the memory;
example1 = example1.replace(oldVal, newVal) //search and replace
example1 = example1.trim() //trims surrounding whitespace
example1 = example1.contains("value"); //check for the values
example1 = example1.IsEmpty(); //checks if the String is empty
```

### Java conditions

Java supports mathematical conditions

If statement

```java
if (2 < 18) {
  System.out.println("2 is less than 18");
}
```

Using the else statement

```java
int number = 20;
if (number < 18) {
  System.out.println("Less than");
} else {
  System.out.println("Greater than");
}
```

### Java Collections

#### 1. List

A List is an ordered Collection (sometimes called a sequence). Lists may contain duplicate elements. Elements can be inserted or accessed by their position in the list, using a zero-based index. The classes that implements List interface are:

- ArrayList
- LinkedList
- Vector
- Stack

#### 2. ArrayList

ArrayList is based on the Array data structure. It is resizable, and an implementation of the List interface. It implements all optional list operations, and permits all elements, including null.

```java
import java.util.*;
class JavaExample{
  public static void main(String args[]){
    //creating ArrayList of string type
    ArrayList<String> arrList = new ArrayList<>();

    //adding few elements
    arrList.add("Cricket"); //list: ["Cricket"]
    arrList.add("Hockey"); //list: ["Cricket", "Hockey"]

    //inserting element at first position, index 0
    //represents first element because ArrayList is based
    //on zero based indexing system
    arrList.add(0, "BasketBall"); //list: ["BasketBall", "Cricket", "Hockey"]


    System.out.println("ArrayList Elements: ");
    //Traversing ArrayList using enhanced for loop
    for(String str:arrList)
      System.out.println(str);
  }
}
```

#### 3. LinkedList

The LinkedList is a linear data structure, its elements are not stored in contiguous locations like arrays, they are linked with each other using pointers. Each element of the LinkedList has the reference(address/pointer) to the next element of the LinkedList.

```java
import java.util.*;
public class JavaExample{
  public static void main(String args[]){
    LinkedList<String> linkList = new LinkedList<>();
    linkList.add("Apple"); //["Apple"]
    linkList.add("Orange"); //["Apple", "Orange"]

    //inserting element at first position
    linkList.add(0, "Banana"); ////["Banana", "Apple", "Orange"]

    System.out.println("LinkedList elements: ");
    //iterating LinkedList using iterator
    Iterator<String> it=linkList.iterator();
    while(it.hasNext()){
      System.out.println(it.next());
    }
  }
}
```

#### 4. Vector

Vector implements List Interface. Like ArrayList it also maintains insertion order but it is rarely used in non-thread environment as it is synchronized and due to which it gives poor performance in searching, adding, delete and update of its elements.

```java
import java.util.*;
public class JavaExample{
  public static void main(String args[]){
    Vector<String> v=new Vector<>();
    v.add("item1"); //["item1"]
    v.add("item2"); //["item1", "item2"]
    v.add("item3"); //["item1", "item2", "item3"]

    //removing an element
    v.remove("item2"); //["item1", "item3"]

    System.out.println("Vector Elements: ");
    //iterating Vector using iterator
    Iterator<String> it=v.iterator();
    while(it.hasNext()){
      System.out.println(it.next());
    }
  }
}
```

#### 5. Stack

Stack class extends Vector class, which means it is a subclass of Vector. Stack works on the concept of Last In First Out (LIFO). The elements are inserted using push() method at the end of the stack, the pop() method removes the element which was inserted last in the Stack.

```java
import java.util.*;
public class JavaExample{
  public static void main(String args[]){
    Stack<String> stack = new Stack<>();

    //push() method adds the element in the stack
    //and pop() method removes the element from the stack
    stack.push("Cat"); 
    stack.push("Dog"); 
    stack.push("Cow"); 
    stack.pop(); //removes the last element
    stack.push("Ant"); 
    stack.push("Bee"); 
    stack.pop(); //removes the last element

    System.out.println("Stack elements: ");
    for(String str: stack){
      System.out.println(str);
    }
  }
}
```

#### 6. Set

A Set is a Collection that cannot contain duplicate elements. There are three main implementations of Set interface: HashSet, TreeSet, and LinkedHashSet.

- HashSet

Stores its elements in a hash table, and allows for only unique elements. It doesn’t maintain the insertion order which means element inserted last can appear at first when traversing the HashSet.

```java
import java.util.*;
public class JavaExample{
  public static void main(String args[]){
    HashSet<String> set = new HashSet<>();
    set.add("Item1");
    set.add("Item2");
    set.add("Item3");
    set.add("Item4");
    set.add("Item5");

    Iterator<String> it=set.iterator();
    while(it.hasNext()){
      System.out.println(it.next());
    }
  }
}
```

- LinkedHashSet

Maintains the insertion order. Elements gets sorted in the same sequence in which they have been added to the Set.

```java
import java.util.LinkedHashSet;
public class LinkedHashSetExample {
     public static void main(String args[]) {
         // LinkedHashSet of String Type
         LinkedHashSet<String> exampleLinkedHashSet = new LinkedHashSet<String>();

         // Adding elements to the LinkedHashSet
         exampleLinkedHashSet.add("Boy");
         exampleLinkedHashSet.add("plan");
         exampleLinkedHashSet.add("Noise");
         exampleLinkedHashSet.add("Orange");
         exampleLinkedHashSet.add("Knife");
         exampleLinkedHashSet.add("Fight");
         System.out.println(exampleLinkedHashSet);

         // LinkedHashSet of Integer Type
         LinkedHashSet<Integer> example2 = new LinkedHashSet<Integer>();

         // Adding elements
         example2.add(99);
         example2.add(7);
         example2.add(0);
         example2.add(67);
         example2.add(89);
         example2.add(66);
         System.out.println(example2);
    }
}
```

- TreeSet

Sorts the elements in the ascending order while HashSet doesn’t maintain any order. TreeSet allows null element but like HashSet it doesn’t allow.

```java
import java.util.TreeSet;
public class TreeSetExample {
     public static void main(String args[]) {
         // TreeSet of String Type
         TreeSet<String> treeSetExample = new TreeSet<String>();

         // Adding elements to TreeSet<String>
         treeSetExample.add("ABC");
         treeSetExample.add("String");
         treeSetExample.add("Test");
         treeSetExample.add("Pen");
         treeSetExample.add("Ink");
         treeSetExample.add("Jack");

         //Displaying TreeSet
         System.out.println(treeSetExample);

         // TreeSet of Integer Type
         TreeSet<Integer> tSetExample2 = new TreeSet<Integer>();

         // Adding elements to TreeSet<Integer>
         tSetExample2.add(88);
         tSetExample2.add(7);
         tSetExample2.add(101);
         tSetExample2.add(0);
         tSetExample2.add(3);
         tSetExample2.add(222);
         System.out.println(tSetExample2);
    }
 }
```

#### 7. Map

A Map is an object that maps keys to values. A map cannot contain duplicate keys. There are three main implementations of Map interfaces: HashMap, TreeMap, and LinkedHashMap.

- HashMap

HashMap: HashMap is like HashSet, it doesn’t maintain insertion order and doesn’t sort the elements in any order.

```java
import java.util.*;
public class JavaExample{
  public static void main(String args[]){
    HashMap<Integer, String> exampleHashMap = new HasHashMap<>();

    //key and value pairs
    exampleHashMap.put(101, "Bright");
    exampleHashMap.put(105, "Derick");
    exampleHashMap.put(111, "Logan");
    exampleHashMap.put(120, "Paul");

    //print HashMap elements
    Set set = exampleHashMap.entrySet();
    Iterator iterator = set.iterator();
    while(iterator.hasNext()) {
      Map.Entry m = (Map.Entry)iterator.next();
      System.out.print("key is: "+ m.getKey() + " & Value is: ");
      System.out.println(m.getValue());
    }
  }
}
```

- TreeMap

TreeMap: It stores its elements in a red-black tree. The elements of TreeMap are sorted in ascending order. It is substantially slower than HashMap. Refer this guide to learn TreeMap with examples.

This is the same example that we have seen above in HashMap. Here, elements are sorted based on keys.

```java
import java.util.*;
public class JavaExample{
  public static void main(String args[]){
    TreeMap<Integer, String> example = new TreeMap<>();

    //key and value pairs
    example.put(101, "Mike");
    example.put(105, "Anthony");
    example.put(111, "Greg");
    example.put(120, "Paul");

    //print HashMap elements
    Set set = example.entrySet();
    Iterator iterator = set.iterator();
    while(iterator.hasNext()) {
      Map.Entry m = (Map.Entry)iterator.next();
      System.out.print("key is: "+ m.getKey() + " & Value is: ");
      System.out.println(m.getValue());
    }
  }
}
```

- LinkedHashMap

LinkedHashMap: It maintains insertion order. Refer this guide, to learn LinkedHashMap in detail. As you can see: In the following example, the key & value pairs maintained the insertion order.

```java
import java.util.*;
public class JavaExample{
  public static void main(String args[]){
    LinkedHashMap<Integer, String> example = new LinkedHashMap<>();

    //key and value pairs
    example.put(100, "Chris");
    example.put(120, "Paul");
    example.put(105, "Derick");
    example.put(111, "Andrew");

    //print LinkedHashMap elements
    Set set = example.entrySet();
    Iterator iterator = set.iterator();
    while(iterator.hasNext()) {
      Map.Entry m = (Map.Entry)iterator.next();
      System.out.print("key is: "+ m.getKey() + " & Value is: ");
      System.out.println(m.getValue());
    }
  }
}
```

### Java Program

A java program that reads and gets a file information

```java
import java.io.File; 

public class GetFileInfo {  
  public static void main(String[] args) {  
    File myObj = new File("filename.txt");
    if (myObj.exists()) {
      System.out.println("File name: " + myObj.getName()); 
      System.out.println("Absolute path: " + myObj.getAbsolutePath()); 
      System.out.println("Writeable: " + myObj.canWrite()); 
      System.out.println("Readable: " + myObj.canRead()); 
      System.out.println("File size in bytes: " + myObj.length());
    } else {
      System.out.println("The file does not exist.");
    }
  }  
} 
```
* **SET DATA TYPE**

```java
  public class Set<Key extends Comparable<Key>> implements Iterable<Key>
  Set() //create an empty set
  boolean isEmpty()  //return if the set is empty
  void add (Key key)  //add key to the set
  void remove(Key key)  //remove key from set
  boolean contains(Key key) //return if the key is in the set
  int size() //number of elements in set
```