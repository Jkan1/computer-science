# Java Collections API

* ArrayList 
    * Interface : List
    * Not Synchronized like vector
    * Can be Synchronized by 2 ways
          * Collections.synchronizedList() method 
          * Using CopyOnWriteArrayList (Creates separate array copy for modifications after Iterator initilized)
    * Thread-Safe means it will throw error on concurrent Access/Modifications

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
    * 
    


    
