# Data Structures

## Array
  
  * It holds the same type of data.
  * Elements are stored in contagious memory locations, i.e continuous memory locations with a single name.
  * Elements can be accessed by iterating through the indices.
  * Cannot be dynamically resized. This may cause the memory assigned to be wasted or insufficient.
  
  * Access Time - O(1)
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
    * Linear Search 
      Avg. Time Complexity : O(n), Case : For Small list
    * Binary Search
      Avg. Time Complexity : O(log n), Case : Sorted array, Large List


## Structure

  * Compound data type, used for grouping other data types.
    Collection of different data types i.e. can be simple or other compund data types.
    
  * **Self-Refrential Structures**
    * A structure definition which includes at least one member that is a pointer to the structure of its own kind.
      For an example, a Linked list Node containing an address to another Node.


### *ADT (Abstract Data Type)*

## Linked List

  
