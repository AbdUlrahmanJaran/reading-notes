# Trees
A tree is a nonlinear hierarchical data structure that consists of nodes connected by edges.

- ``Node`` - A Tree node is a component which may contain its own values, and references to other nodes.
- ``Root`` - The root is the node at the beginning of the tree.
- ``K`` - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- ``Left`` - A reference to one child node, in a binary tree.
- ``Right`` - A reference to the other child node, in a binary tree.
- ``Edge`` - The edge in a tree is the link between a parent and child node.
- ``Leaf`` - A leaf is a node that does not have any children.
- ``Height`` - The height of a tree is the number of edges from the root to the furthest leaf.

## Traversals
An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more!
### 1. Depth First
Depth first traversal is where we prioritize going through the depth (height) of the tree first.

Here are three methods for depth first traversal:
1. Pre-order: ``root`` >> ``left`` >> ``right``
2. In-order: ``left`` >> ``root`` >> ``right``
3. Post-order: ``left`` >> ``right`` >> ``root``

### 2. Breadth First
Breadth first traversal iterates through the tree by going through each level of the tree node-by-node. Traditionally, breadth first traversal uses a queue to traverse the width/breadth of the tree.

## Binary Search Trees
A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

### Searching a BST
Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

- The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height).
- The Big O space complexity of a BST search would be O(1)