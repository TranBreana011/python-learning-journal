Things I learned this week:

Trees: 
Heaps are types of trees, used in priority queues
- trees are a fundamental ADT that extends the concepts we learned with linked lists
- trees are fundamental data structures that are used in many cases to store data or implement algorithms
- in a tree, each node connects to any number of other nodes so long as we do not create a cycle
- behavior: branching, the end result is a tree that's faster to traverse than a linked list
- exception: if the link would create a cycle
- cycle: occurs when you can traverse from one node back to itself without ever using a edge twice
- edge: another way to refer to links
- dont mistake cycles with backtracking
- whole point about trees are that they use cycles
- a linkedlist is a subset of a tree
- a tree is a subset of a graph
- without knowing the lowest num we have to traverse

Depth vs. Width (What's more important)
- We want a balance
- O(n) now but we want better

Binary Trees:
- a subtype of Tree most similar to a list
- a list of node has up to one successor, a Binary Tree has two
- in a Binary Search Tree, the order of what is stored in each successor matters
- Components: Node, Left Child, Right Child
- Node: contains some comparable value
- Left Child: all values less than or equal to node
- Right Child: all values greater than node
- works with any comparable value

More Tree Components:
- Root: the root is the topmost node in a BST. It doesn't have a parent and serves as the entry point to the tree. All nodes in a BST are descendants of the root, either directly or indirectly
- maintaining the root position is critical
- Leaves: they are terminal nodes (a left is any node without any children), located at the outermost level of the tree. A leaf cannot have a child nodes.
- Height/Depth: the length of the longest path from root to leaf
- Subtree: A portion of a BST that forms a BST, any node with its children is a subtree
- Tree is a naturally recursive DS,

Types of BSTs:
- certain binary tree structures can affect the speed of operations on the tree. the following describe special types of binary trees.
- a binary tree is full if every node contains 0 or 2 children
- a binary tree is complete if all levels, except possibly the last level, contain all possible nodes and all nodes in the last level are as far left as possible
- a binary tree is perfect, if all internal nodes have 2 children and all leaf nodes are at the same level
- if we are going in at a perfect tree and spliting in each level, then each level will be doubled by the previous level by taking in an extra step
- it would be O(log n) since each level is doubled per ONE step
- as the size of the array increases, the less steps u get
- we are getting better returns the bigger the n gets
- we don't have to worry about the data set size

BST Applications:
- Database Systems:
    - indexing: BSTs are widely used in data bases to index data, allowing for faster search, add, delete, and upgrade operations on the data base records. Indexing using BSTs can significantly optimize the performance of database systems
- Query Processing: The sortednature of BSTs assists in efficienty query processing, especially when dealing with range queries and ordered retrievals in database management systems.
    - File Systems: BSTs are integral in managing file systems, where they are used to locate files and directories swiftly, contributing to the overall performance and responsiveness of the file system
 
Operations:
- Search:
    - Binary Search Trees lend themselves naturally to searching
        - its in the name after all
    - we can follow the binary search algorithm, adapting it for traversal through a tree
    - always going to be in sorted order because values smaller will be on the left and values bigger than will be on the right
    - this operation is O(log n) because
    - if our binary search tree is perfect then it will be O(log n)
        - can't always count on perfect
        - only if we have 1, 2, 4, 16
    - if our binary search tree is complete then it is O(log n)
    - if our binary search tree is full, it helps us find if the bst is complete or full
  1. we start at the root
     - if less go left
     - if greater go right
     - if equal depends on tree requirements, could updates go left, ignore operation, etc
  3. compare values
  4. once leaf is reached, add new node to the leaf

Insertion Algorithm
- adding a node is not sufficient, we must also maintain all properities of a BST while doing so
- ex. tree.insert(35, "__")
- parent.left = New Node

Insertion Efficiency:
- looking at it closely, insertion is very similar to search
- we're just searching for a leaf to place a node at
- in a balanced tree, insertion is a O(log n) operation
- In the worst case scenario, insertion is O(n)

Deletion Algorithm
- removing a node is much more complex than searching or inserting, only really simple when you remove a leaf node
- 1. locate the Node via search
  2. check possible node deletion case
     - if the node is a leaf, remove it (break parent's link)
     - if the node has one child, link the node's parent to that child
     - if node has two children, find the inorder successor (the smallest value in the right subtree) and replace the value of the node to be deleted with the value of the inorder successor
- the garagbe can will clean up our deletions

Deletion Efficiency:
- while deletion relies on a number of matters...

Tree Traversal Types:
- Inorder Traversal:
  - steps: traverse down left subtree, visit the root, traverse down right subtree
  - usage: using in a bst, inorder traversal will visit nodes in ascending order
- Preorder Traversal:
  - steps: visit the root, traverse down the left subtree, traverse the right subtree
  - usage: using preorder traversal, it is possible to create a copy of the BST since you are visiting the nodes in the order in which they would be added
  - very useful
- Postorder Traversal: bottom->top, left->right
  - steps: traverse the left subtree, traverse the right subtree, visit the root
  - usage: while not as important in python, post order traversal is helpful in deleting the tree while not accidentally unlinking any node and causing memory leak

