Video URL: [Complete Java Collections Framework & Streams Masterclass 2024
](https://www.youtube.com/watch?v=92k5uokmW9o) by [Engineering Digest](https://www.youtube.com/@EngineeringDigest)

### Collection
- `Collection` is simply an object that represents a group of objects, known as its elements.

### Collection Framework
- It provides a set of interfaces and classes that helps managing groups of objects.
- It is introduced in Java 2 (JDK 1.2).
- Before that `Java` used of to rely on veriety of class like `Vector`, `Stack`, `Hashtable` and `Arrays' to store and manipulate groups of objects.
- Before collection framework, there was
  - `Inconsistancy` : Each class has its own implementation.
  - `Lack of interoperabiliy`: These class were not designed to work together seamlessly.
  - `No common interface`: There was no common interfaces for all those classes, which means you cannot write generic code that works with all of them.
- Benefits
  - `Unified Architecture`
  - `Inter-operability`
  - `Reuasbility`
  - `Efficiency`

### Collections Types
- Collections
  - The root interface of all other collection types.
- List
  - Duplicate or ordered collection of objects.
  - Implementation: `ArrayList`, `LinkedList`, `Vector`, `Stack`
  - Key features
    - Order Preservation
    - Index based access
    - Allows Duplicates
- Set
- Queue
- Deque
  - Double Ended Queue
- Map

### Collection Hierarchy
![img.png](../../static/img/java/collection/collection-hierarchy.png)


### List Interface
#### ArrayList
- resizable array implementation of the `List` interface.
- ArrayList can grow and shrink as elements are added and removed. This dynamic resizing is achieved by `creating a new array when the current array is full and copying all elements to the new array`.
- It is implemented as an array Object references, when you add an element to the ArrayList, it is stored in the array at the next available index.
- 
```java
void main(String[] args) {
    ArrayList<Integer> list = new ArrayList<>();
    list.add(1);
    list.add(2);
    list.add(3);
    System.out.println(list);
    System.out.println(list.get(0));
    
    // print size
    System.out.println(list.size());
    
    // iteration using for loop
    for (int i = 0; i < list.size(); i++) {
        System.out.println(list.get(i));
    }
    // iteration using for-each loop
    for (int i : list) {
        System.out.println(i);
    }
    
    //contains
    System.out.println(list.contains(1));
    
    // remove by index
    list.remove(1);
    System.out.println(list);
    
    //insertion at index
    list.add(1, 2);
    System.out.println(list);
    
    // update by index
    list.set(1, 3);
    System.out.println(list);
}
```