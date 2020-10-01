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
        
## Heap

  * A Tree based data structure that satisfies Heap Property.
  * The Value of Parent is either Greater than or Equal to, OR Less than or Equal to the value of the child.
  * Types
    * Max Heap : (Value of Parent is either Greater than or Equal to value of the child)
    * Min Heap : (Value of Parent is either Less than or Equal to value of the child)
  * Uses : Heap Sort (Best In-Place sorting), Implementing Priority Queue, Selection Algo, Graph Algo.
  * Operations
    * Find Max/Min - Constant time as it's on the root node.
    * Insert - First insert then keep swapping with parent if greater/lesser than parent.
    * Delete - Element always deleted from node, Swap Root with Last element, Delete Node, (Swap root position with rightmost node), Heapify.


## Graphs

  * Consists of Nodes and Edges used to represent relations between pairs of objects.
  * Props
    * A graph G is defined as an ordered set(V, E), V(G) represents the set of Vertices and E(G) represents the Edges.
    * Directed Graph : Edges have direction, path only from one side not both sides.
    * Undirected Graph : Edges do not have any direction.
    * Uses : Network Models, Social Network.
  * Terms
    * Vertex
    * Edge
    * Undirected Graph
    * Directed Graph
    * Mixed Graph
    * Origin (in directed graph edge starting point)
    * Destination (in directed graph edge destination)
    * Adjacency (if two nodes are connected)
    * Path (Sequence of Edges btw two Vertices)
    * Degree (No. of Edges connected)
    * In-Degree (No. of Edges coming to a vertex)
    * Out-Degree (No. of Edges going out from vertex)
    * Edge Weight : Each edge of a graph has an associated numerical value, called a weight. Usually, the edge weights are non- negative integers. Weighted graphs may be either directed or undirected. The weight of an edge is often referred to as the "cost" of the edge.
    
  * Minimum Spanning Tree (MST)
    * A minimum spanning tree or minimum weight spanning tree is a subset of the edges of a connected, edge-weighted undirected graph that connects all the vertices together, without any cycles and with the minimum possible total edge weight. That is, it is a spanning tree whose sum of edge weights is as small as possible.
    * A graph can contain more than one Spanning tree.
  
  * Simple Graph: A graph is said to be simple if there are no parallel and self-loop edges.

  * Directed acyclic graph (DAG): A directed acyclic graph (DAG) is a graph that is directed and without cycles connecting the other edges. This means that it is impossible to traverse the entire graph starting at one edge.

  * Weighted Graph: A weighted graph is a graph in which a number (known as the weight) is assigned to each edge. Such weights might represent for example costs, lengths or capacities, depending on the problem.

  * Complete Graph: A complete graph is a graph in which each pair of vertices is joined by an edge. A complete graph contains all possible edges.

  * Connected graph: A connected graph is an undirected graph in which every unordered pair of vertices in the graph is connected. Otherwise, it is called a disconnected graph.

  * Representation of a graph
  
    * Adjacency List Representation
       * In this representation, every vertex of the graph contains a linked list of its neighboring vertices and edges.
       An array of lists is used where the size of the array is equal to the number of vertices. Each of the elements in the arrays contains a linked list of all the vertices adjacent to the list.

    * Adjacency Matrix Representation
       * In this representation, the graph can be represented using a matrix of size total number of vertices by the total number of vertices. Here, rows and columns both represent vertices. This matrix is filled with either 1 or 0. Here, 1 represents there is an edge from row vertex to column vertex and 0 represents there is no edge from row vertex to a column vertex.
       * Adjacency matrix representation requires O(V^2) memory locations irrespective of the number of edges in the graph.
       
  * Graph Traversal Algorithms
    * Breadth First Search (BFS)
    * Depth First Search (DFS)

  * Breadth First Search (BFS)
    * Breadth-first search begins at the root node of the graph and explores all its neighbouring nodes. For each of these nodes, the algorithm again explores its neighbouring nodes. This is continued until the specified element is found or all the nodes are exhausted.
A queue is used as an auxiliary data structure to keep track of the neighboring nodes.

  * Depth First Search (DFS)
    * Depth-first search starts on a node and explores nodes going deeper and deeper until the specified node is found, or until a node with no children is found. If a node is found with no children, the algorithm backtracks and returns to the most recent node that has not been explored. This process continues until all the nodes have been traversed.
A stack is used as an auxiliary data structure to keep track of traversed nodes to help it backtrack when required.



