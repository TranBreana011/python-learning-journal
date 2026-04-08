Things I learned this week:

Tree Wrap Ups:
Binary Search Trees:
Previous Data Structures:
- simple data strucutre
- searching, insertion, and deletion operations are fairly straightforward
- average case efficiency O(log n)
- worst case scenario on all operations is Linear O(n)
- such that we have a snake-like tree
    - search node 4
    - delete node 4
    - insert item greater than 4
- unbalanced nature leads to inefficiency

Problem: Binary Search trees can wind up inbalanced depending on insertion nodes
Solution: Re-balance the tree after inserting or removing a node in order to ensure efficiency

Need a Mathematical solution: How to calculate balance
Using Height:
H(n) = max(H(subtree_L), H(subtree_R)) + 1
- H(empty) = -1             : Base Case
- H(single node) = 0        : Base Case
Balance(n) = H(subtree_L) - H(subtree_R))

-Calaculate from bottom to top
-Need all the tree to be finished 


Balance Check:
If |B(n)| > 1: Tree is unbalanced
- If balance is positive, tree is left heavy
    - R rotation, L-R rotation
- If balance is negative, tree is right heavy
    - L rotation, R-L rotation

-1, 0, 1 are all considered balance
also lets us know which side is inbalanced 

General Case: R rotation
function RightRotate(current)
    newRoot = current -> left
    current -> left = newRoot -> right
    newRoot -> right = current
    computeHeightFromChildren(current)        :recompute the height of the current node (y)
    computeHeightFromChildren(newRoot)        :recompute the height of the new root node (x)
    return newRoot
  end function

General Case: L rotation 

General Case: Double Rotation
LR Rotation
function LeftRightRotate(current)
    current -> left = leftRotate(current->left)
    return rightRotate(current)
  end function

When to use Single or Double Rotation?
- after you have determined to which side the tree skews, take the node at the root of the skewed tree (St)
- Compare the heights of St subtrees against each other
    - if the grandchild with the tallest height is in same direction as skew, only single rotation is needed
    - if the grandchild with the tallest height is in the opposite direction as skew, double rotation is needed
 
AVL Insertion/Deletion:
- perform the insertion or deletion operation as you would in a BST
- update the height of each node
- perform AVL rotations as necessary to rebalance the tree

- when it comes to performing an insertion, we are affecting everything from the path from the node to the root
- we only care about the path from the root to the node

Analysis of AVL trees:
advantages:
- height becomes O(log n)
- search, insertion, deletion operations become o(log n)

disadvantages:
- frequent rotation operations
- complexity

- the bigger the BST the more we benefit from O(log n)

an avl tree can use anything comparable 
