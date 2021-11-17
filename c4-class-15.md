# Read 15 - Trees

## Terminology

* Node a component which contains a value and references to other nodes
* Root - the node at the beginning of the tree
* K - the maximum number of children any node may have. In a binary tree, k = 2.
* Left - one child node in a binary tree
* Right - the other child node in a binary tree
* Edge - the link between a parent and child node
* Leaf - that does not have any children
* Height - the number of edges from the root to the furthest leaf

## Traversals

1. **Depth First Traversals**: an algorithm for traversing/searching a tree starting at a node, usually the root node, and exploring as far as possible along each branch before backtracking. There are three methods for depth first traversal:

    1. *Pre-order*: root >> left >> right

    ![pre-order](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/how-to-traverse-in-a-tree-preorder-708011002b5de4a0.png)

    2. *In-order*: left >> root >> right

    ![in-order](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/how-to-traverse-in-a-tree-inorder-b137e82e804ef68e.png)

    3. *Post-order*: left >> right >> root

    ![post-order](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/how-to-traverse-in-a-tree-postorder-13146c73f47dcf88.png)

The difference between each of them is when they are looking at the root node.

[more](https://afteracademy.com/blog/how-to-traverse-in-a-tree)

2. **Breadth First Traversals**: an algorithm for traversing/searching a tree by going through each level of the tree node-by-node.

![vs](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Sorted_binary_tree_breadth-first_traversal.svg/1200px-Sorted_binary_tree_breadth-first_traversal.svg.png)

## Binary Trees

Binary Trees restrict the number of children to two (k=2), hence our left and right children.

## K-ary Trees

Trees can have any number of children per node. K refers to the maximum number of children that each Node is able to have.

Traversing a K-ary tree requires a similar approach to the breadth first traversal. In which we move down a list of children of length k, instead of checking for the presence of a left and a right child.

![k-ary](https://drek4537l1klr.cloudfront.net/larocca/v-11/Figures/02_05.png)

## Adding a node

There are no structural rules for where nodes are supposed to go in a binary tree. One strategy for adding a new node is to transverse and look for an empty child spot from the top down. Leverage the use of breadth first traversal can be used to the first node that does not have all it’s children filled, and insert the new node as a child. Child slots are filled from left to right.

In the event of placing a node in a specific location, both the new node to create, and the parent node upon which the child is attached to are to be referenced.

* **Big O Time Complexity* for inserting a new node is O(n). Searching for a specific node will also be O(n).

* **Big O Space Complexity* for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree (max number of children at the same level for a parent).

## Binary Search Trees (BST)

A type of tree that does have some structure attached to it nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

To search a BST, compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

* **Big O Time Complexity* of a Binary Search Tree’s insertion and search operations is O(h); where h is height. The worst case is searching all the way down to a leaf, which will require searching through as many nodes as the tree has.

* **Big O Space Complexity* of a BST search is O(1); because during a search, no additional space is allocated.
