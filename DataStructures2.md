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
    * Order (represents the upper bound on the number of children. ie. the maximum number possible)
    * Level (each step from top to bottom)
    * Height (no. of edges from leaf to some node)
    * Depth (no. of edges from root to some node)
    * Path
    
  * **Generalization :** Bottom Up & **Specialization :** Top to Bottom
    
  * Tree Traversals
    * Depth First Traversals:
      * Inorder (Left, Root, Right) : 4 2 5 1 3
      * Preorder (Root, Left, Right) : 1 2 4 5 3
      * Postorder (Left, Right, Root) : 4 5 2 3 1
    * Breadth First or Level Order Traversal : 1 2 3 4 5
    
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
      * The Value stored in each Node must be, Greater than or Equal to any Value stored in the Left Sub-Tree, and Less than or Equal to any Value stored in the Right Sub-Tree.
      
    
    * **Multiway Search Tree**
      * Can have more than one Value per Node.
      * They are written as **m-way Trees** where m means the order of the tree.
      * A Multiway tree can have **m-1** values per Node and **m** children.
      * Example : B-Tree of order 5, each Node can have max of 4 values and 5 children.
      
      * B-Trees and B+ Trees
        * https://www.youtube.com/watch?v=aZjYr87r1b8
        * B-Tree 
          * m/2 children
          * Root can have min 2 children
          * Leaf Nodes at same Level
          * Bottom Up
    
    * **AVL Tree**
      * Self Balancing Binary Search Tree. A Binary Tree is said to be Balanced if the difference between the heights of left and right subtrees of every Node in the Tree is either -1,0 or +1 ( known as Balance Factor).
      * Balance Factor : height(left_subtree) - height(right_subtree)
      * During a modification operation if the height difference of more than 1 arises between two subtrees, the Parent subtree has to be rebalanced to satisfy AVL property.
      * Tree Rotations
        * Rotation is process of moving the Nodes to either Left or Right to make Tree Balanced.
        * Single Left Rotation (LL)
        * Single Right Rotation (RR)
        * Left Right Rotation (LR)
        * Right Left Rotation (RL)
        
    
