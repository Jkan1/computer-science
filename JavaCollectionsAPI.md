# Java Collections API


* ArrayList 
    * Interface : List
    * Not Synchronized like vector
    * Can be Synchronized by 2 ways
          * Collections.synchronizedList() method 
          * Using CopyOnWriteArrayList (Creates separate array copy for modifications after Iterator initilized)
    * **Fail-Fast** Iterator that are fail-fast in nature will throw error on concurrent Access/Modifications


* LinkedList
   * Implements List and Deque and Extends AbstractSequentialList
   * Uses doubly linked list to store the elements


* HashMap 
    * Interface : Map | Extends: abstract class AbstractMap | Implements : Cloneable and Serializable interface
    * No guarantees as to the order of the map and Order can change in time
    * Initial Capacity : 16 key-value pairs
    * Load Factor : 0.75f | 75%
    * Threshold : (16 * 0.75 = 12) | **Rehashing** takes place after inserting 12 (Threshold) key-value pairs into the HashMap
    * Synchronized: Collections.synchronizedMap(new HashMap(...))
    
    
* HashSet
    * Implements Set Interface
    * The underlying data structure for HashSet is Hashtable
    * implements the Set Interface
    * duplicate values are not allowed
    * not guaranteed to be inserted in the same order
    * Objects are inserted based on their hash code
    * NULL elements are allowed in HashSet
    * implements Serializable and Cloneable interfaces
    * Initial Capacity, Threshold and Rehashing same as HashMap.
 
 
* LinkedHashMap
    * Like HashMap with an additional feature of maintaining an order of elements
    * Implements the Map interface and extends the HashMap class
    * It contains only unique elements
    * It may have one null key and multiple null values
    * Not Synchronized
    * Hash: All the input keys are converted into a hash which is a shorter form of the key so that the search and insertion are faster
    * Synchronized: Collections.synchronizedMap(new LinkedHashMap(...));


*  LinkedHashSet
    * An ordered version of HashSet that maintains a doubly-linked List across all elements
    * Allows maximum one null element
    * Uses equals() and hashCode() methods to compare


* How in java Set interface implemented classes like HashSet, LinkedHashSet, TreeSet etc. achieve this uniqueness? 
    * It uses HashMap inside, as  key-value, the each key is the value passed in Set, and value is "PRESENT" (Dummy Value)
    

* ConcurrentHashMap
    * Enhancement of HashMap, as while dealing with Threads, HashMap is not a good choice because performance-wise HashMap is not up to the mark
    * The underlined data structure for ConcurrentHashMap is Hashtable.
    * Implements Serializable, ConcurrentMap, Map and Extends AbstractMap
    * Concurrency-Level: It is the number of threads concurrently updating the map. The implementation performs internal sizing to try to accommodate this many threads
    * Initial Capacity, Threshold and Rehashing same as HashMap
    * Is **Thread-Safe** i.e. multiple threads can operate on a single object without any complications
    * Inserting null objects is not possible in ConcurrentHashMap as key or value.
    * At a time any number of threads can perform retrieval operation but for updation in the object, the thread must lock the particular segment in which the thread wants to operate. This type of locking mechanism is known as Segment locking or bucket locking. Hence at a time, 16 update operations can be performed by threads.
    

* TreeMap
    * Implements Map and NavigableMap with AbstractMap Class
    * The storing order is maintained
    * Based upon a redblack tree data structure
    * Not synchronized
    * Not allow null keys (like Map) and thus a NullPointerException is thrown
    * Synchronized : Collections.synchronizedSortedMap(new TreeMap(...))
    
    
* HashSet vs TreeSet
    * Speed and internal implementation
         * HashMap takes constant time for Search, Insert and Delete operations on average. HashSet is faster than TreeSet. HashSet is Implemented using a hash table
         * TreeSet takes O(Log n) for Search, Insert and Delete which is higher than HashSet. But TreeSet keeps sorted data. Also, it supports operations like higher() (Returns least higher element), floor(), ceiling(), etc. These operations are also O(Log n) in TreeSet and not supported in HashSet.
    
    * Ordering
         * Elements in HashSet are not ordered. TreeSet maintains objects in Sorted order defined by either Comparable or Comparator method in Java. TreeSet elements are sorted in ascending order by default. It offers several methods to deal with the ordered set like first(), last(), headSet(), tailSet(), etc
    
    * Null Object
         * HashSet allows null object. TreeSet doesn't allow null Object and throw NullPointerException, Why, because TreeSet uses compareTo() method to compare keys and compareTo() will throw java.lang.NullPointerException.
     
    * Comparison
         * HashSet uses equals() method to compare two object in Set and for detecting duplicates. TreeSet uses compareTo() method for same purpose
         
    * NOTE : If you want a sorted Set then it is better to add elements to HashSet and then convert it into TreeSet rather than creating a TreeSet and adding elements to it

         
         
         
         
         
