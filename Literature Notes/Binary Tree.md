A **tree** is an undirected [[Graphs|graph]] which satisfies any of the following points:
- An acyclic connected graph
- A connected graph with *N* nodes and *N-1* edges
- A graph in which any two vertices are connected by exactly one path

If we have a **rooted tree**, then we will want to have a reference to the root node of our tree. It doesn't matter which node is selected as a root node, because any node can root the tree.

A **child** is a node that extends from another node. A **parent** is the inverse of this.

A **leaf node** is a node with no children.

A **binary tree** is a tree where each node has at most 2 child nodes.

## Where are Binary Trees used?

- Binary Search Tree (BST)
- Used in implementations of binary heaps
- Syntax trees (used by compilers and calculators)
- Treap - a probalistic DS (uses a randomized BST)

## [[Big-O Notation|Complexity]]

| Operation | Average | Worst |
| --- | --- | --- |
| Insert | $O(\log n)$ | $O(n)$ | 
| Delete | $O(\log n)$ | $O(n)$ |
| Remove | $O(\log n)$ | $O(n)$ |
| Search | $O(\log n)$ | $O(n)$ |

## Adding elements to BST

Binary Search Tree (BST) elements must be **comparable** so that we can order them inside the tree.

When inserting an element we want to compare its value to the value stored in the current node we're considering to decide on one of the following:
- Recurse down left subtree (< case)
- Recurse down right subtree (> case)
- Handle finding a duplicate value (= case)
- Create a new node (found a null leaf)

## Removing elements from BST

Removing elements from a BST can be seen as a two step process:
1. **Find** the element we wish to remove (if it exists).
2. **Replace** the node we want to remove with its successor (if any) to maintain the BST invariant.

> [!NOTE] BST invariant
> Left subtree has smaller elements and right subtree has larger elements

### Find phase

When searching BST for a node with a particular value one of four things will happen:
1. We hit a **null node** at which point we know the value does not exist within our BST
2. Comparator value **equal to 0** (value has been found)
3. Comparator value **less than 0** (the value, if it exists, is in the left subtree)
4. Comparator value greater than 0 (the value, if it exists, is in the right subtree)

### Remove phase

When removing node from BST four cases might happen:
1. Node to remove is a leaf node
2. Node to remove has a right subtree but no left subtree
3. Node to remove has a left subtree but no right subtree
4. Node to remove has both subtrees 

Fist 3 cases are pretty straightforward, but the forth case is more difficult. We either must find the **largest value** in the **left subtree**, or the **smallest value** in the **right subtree**. When we do so, we simply copy this value to the removed node place and remove original place of copied value (always will be case 1, 2 or 3 removal).

## Tree Traversals

These three types of traversals are naturally defined recursively:

![[Pasted image 20230723115001.png]]

### Preorder Traversal

Preorder traversal iterates through leftmost branch of tree first, and then where there is no more left child nodes, it goes back until there is right child node. The process ends when all nodes are visited.

![[Pasted image 20230723120029.png]]

### Inorder Traversal

Inorder traversal iterates through leftmost branch of tree first, but prints node value only when there is no left subtrees left. The process ends when all nodes are visited.

![[Pasted image 20230723120634.png]]


> [!NOTE] Inorder Traversal in BST
> Inorder traversal prints out binary search tree values in increasing order.

### Postorder Traversal

Postorder traversal traverses the left subtree followed by the right subtree, then prints the value of the node.

![[Pasted image 20230723121407.png]]

### Level Order Traversal

In a level order traversal we want to print the nodes as they apper one layer at a time. To obtain this ordering we want to do a [[Breadth First Search]] from the root node down to the leaf node.