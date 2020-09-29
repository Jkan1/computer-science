# Data Structures 1

## Array
  
  * It holds the same type of data.
  * Elements are stored in contagious memory locations, i.e continuous memory locations with a single name.
  * Elements can be accessed by iterating through the indices.
  * Cannot be dynamically resized. This may cause the memory assigned to be wasted or insufficient.
  
  * Access      - O(1)
  * Search      - O(n)
  * Insertion   - O(n)
  * Deletion    - O(n)
  * Space       - O(n)
  
  * **Calculating Address of Array Elements** 
      * A[k] = base_address(A) + size_of_element( k - lower_bound)
      
  * **Multidimensional Arrays**
    Can be Visualised as a table with rows and columns.
    
  * **Sparse Matrix**
    A matrix which contains more Zero values than Non-Zero values. These are generally used because of 2 advantages -
      * Save Space : by storing only the Non-Zero elements.
      * Save Computing Time : by storing the elements in way that is efficient for access.
      
  * Search Operations
    * **Linear Search** 
      Avg. Time Complexity : O(n), Case : For Small list
    * **Binary Search**
      Avg. Time Complexity : O(log n), Case : Sorted array, Large List


## Structure

  * Compound data type, used for grouping other data types.
    Collection of different data types i.e. can be simple or other compund data types.
    
  * **Self-Refrential Structures**
    * A structure definition which includes at least one member that is a pointer to the structure of its own kind.
      For an example, a Linked list Node containing an address to another Node.


### *ADT (Abstract Data Type)*

## Linked List

  * Linear Data Structure where each element is a separate object, known as a Node.
    Each Node contains some data and points to the next node in the structure, forming a sequence.
  * This structure allows efficient insertion or removal of elements from any position, as only the link needs to be changed.
  
  * Advantages over Arrays
    * **Flexible in size**
      Linked LIsts are not fixed in size like arrays, they can grow or shrink depending on the data to be inserted.
    * **Efficient Insertion and Deletion**
      These operations are efficient and take constant time as only the link is manipulated not the actual memory location of elements.
      
  * Disadvantages over Arrays
    * Slightly more memory usage : 
      As each element has to store its data along with the reference information.
    * Sequential access : 
      Nodes in Linked List must be read in order from the beginning.
    * Difficult reverse traversal : 
      Difficulties arise when it comes to reverse traversing in a Singly Linked List. Can be resolved using Doubly Linked Lists, but this again increases memory as we have to store the previous reference pointer also.
      
  * Access      - O(n)
  * Search      - O(n)
  * Insertion   - O(1)
  * Deletion    - O(1)
  * Space       - O(n)
  
  * **Uses of Linked List**
    * Implement other data structures : 
      Used to implement other data structures such as stacks, queues and non-linear ones like trees and graphs.
    * Hash Chaining : 
      It has uses in hash chaining for the implementation in open chaining.
      
  * **Types** 
    * **Singly Linked List :** Every Node has one pointer: next.
    * **Doubly Linked List :**  Every Node has two pointers: next and previous.
    * **Circular Linked List :** Last Node connects to the first Node forming a loop.
  
  
## Stacks

  * A Stack is a linear data structure which stores elements in LIFO (Last In First Out) order.
  * The Insertion and Deletion operations are performed at only one end.
  * A pointer keeps track of the stack's topmost element.
  * Implemented using an Array or a Linked List.
  * Examples : UNDO Operation in text editors, Parentheses checker, Expression Parsing using stacks.
  
  * Access      - O(n)
  * Search      - O(n)
  * Insertion   - O(1)
  * Deletion    - O(1)
  * Space       - O(n)
  
  * **Operations**
    * **Push**
      When an element is inserted into stack. The top pointer is moved up to point the element inserted.
    * **Pop**
      When an element is removed from stack. The top pointer is moved down to point the element below the removed element.
    * **Peek**
      This returns the value of the topmost element of the stack.
      
      
## Queues

  * The Insertion and Deletion operations are performed at two different ends.
  * It follows the FIFO (First In First Out) principle.
  * Two Pointers keep track of the Front and Rear of the Queue, these two pointers are updated to track the last and first element.
  * Insertion takes place from the Rear, and Deletion takes place from the Front.
  * Implemented using an Array or a Linked List.
  * Example : A Queue is used in process scheduling in the Operating System. 
    A series of processes wait in a Queue waiting to be be executed when required resources are free.
  
  * Access      - O(n)
  * Search      - O(n)
  * Insertion   - O(1)
  * Deletion    - O(1)
  * Space       - O(n)
  
  * **Operations**
    * **Enqueue (Insert/Store)**
    When an element is inserted into the queue.
    The Rear Pointer updates to the item just inserted to point the now-last element in Queue.
    * **Dequeue (Delete/Access)**
    When an element is deleted from the queue.
    The Front Pointer is updated to the item after the deleted item to point the now-first element in Queue
  
  * **Types**
  
    * **Double Ended Queue (Deque)****
      A Queue in which the elements can be inserted or deleted at either end.
      * Types
        * Input Restricted Queue : 
          Where Insertion takes place only from the rear end, but Deletion can take place from both ends.
        * Output Restricted Queue : 
          Where Deletion takes place from only the front, but Insertion can take place from both ends.
  
    * **Priority Queues**
      A Queue or Stack data structure, where each element has a Priority associated with it. 
      In a priority Queue, an element with high priority is served before an element with low Priority.
      
    * **Circular Queue**
      * A Circular Queue uses a single, fixed-size buffer as if it were connected end-to-end.
      Circular Queue is a good implementation for a queue that has fixed maximum size, as their is no shifting involved and the whole Queue can be used up for storing all the elements, which is not possible in an array implementation of Linear Queue.
      * Circular Queues are used for saving memory as in case of Linear Queue, even after removing an element from the front, new element cannot be inserted on the rear, since the rear-most index still contains some data.
      So Circular Queues move the Rear pointer as well, pointig to the open space in the front of the Queue, hence called Circular Queue
    
  
  
