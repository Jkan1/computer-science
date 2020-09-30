# Data Structures 2

## Trees

  * Hierarchical data structure where the information is represented in the form of parent and children i.e represented as a set of linked nodes.
  * The children of each node could be accessed by traversing the tree until the specific value is reached.
  * Advantages
    * Trees with ordering provide moderate access/search speed (quicker than Linked List).
    * Trees provide moderate insertion/deletion speed (quicker than Arrays).
  * Examples: File System Structure, HTML DOM Structure, Router Algorithm.
  * Terminology
    * Root
    * Parent Node
    * Child Node
    * Siblings
    * Leaf Node
    * Internal Node
    * External Node
    * Degree (no. of children)
    * Level (each step from top to bottom)
    * Height (no. of edges from leaf to some node)
    * Depth (no. of edges from root to some node)
    * Path
    
  * **Types**
  
    * **Binary Tree**
      * Every Node can have maximum of 2 children, known as Left child and Right Child.
      * Props
        * Max number of nodes at Level 'L' : **(2 * L) - 1**
        * Max number of nodes in Binary Tree of Height 'H' : **(2 * H) - 1**
        * Min Height or Level of Binary Tree with 'N' Nodes : **ceil( log( N + 1 ) )**
        * Min Levels of Binary Tree with 'F' Leaf Nodes : **ceil( log( F ) ) + 1**
      
      * **Types**
        * **Strictly Binary Tree :**
          A Binary Tree in which every Node has either Two or Zero children.
          
        * **Complete Binary Tree :**
          A Binary Tree in which every Internal Node has exactly Two children and all Leaf Nodes are at same Level.
          
        * **Extended Binary Tree :**
          A Full Binary Tree obtained by adding dummy Nodes.
          
        * **Threaded Binary Tree :**
          A Binary Tree in which all Left child pointers that are NULL points to its In-Order predecessor, and all Right child pointers that are NULL points to its In-Order successor.
          
          
    * **Binary Search Tree**
    * **Multiway Search Tree**
    * **AVL Tree**
