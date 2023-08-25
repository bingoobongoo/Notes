**Union Find** is a [[Data Structures|data structure]] that keeps track of elements which are split into one or more disjoint sets. It has two primary operations: **find** and **union**.

## Where is union find used?

- [[Kruskal's Minimum Spanning Tree]] algorithm
- Grid prelocation
- Network conectivity
- Least common ancestor in trees
- Image processing

## [[Big-O Notation|Complexity]]

| Operation | Complexity |
| --- | --- |
| Construction | $O(n)$ |
	| Find | $\alpha(n)$ |
| Union | $\alpha(n)$ |
| Get component size | $\alpha(n)$ |
| Check if connected | $\alpha(n)$ |
| Count Components | $O(n)$ |
$\alpha(n)$ - amortized constant time

## Union and Find operations

1. To begin using Union Find, first construct a **bijection** (a mapping, wich is like assigning unique identifier to every object) between your objects  and the integers in the range <0, n).

> [!NOTE]
> This step is not necessary in general, but it will allow us to construct an array-based union find

2. Store Union Find information in an array. Each index has an associated object (letter in this example) we can lookup through our mapping.![[Pasted image 20230709163916.png]]

3. To **find** which component a particular element belongs to find the root of that component by following the parent nodes until a self loop is reached (a node who's parent is itself).

4. To **unify** two elements find which are the root nodes of each component and if the root nodes are different make one of the root nodes be the parent of the other.


> [!NOTE] Remarks
> In this data structure we don't really "un-union" elements, as this operation would be very inefficient to do since we would have to update all the children of a node. 
> The number of components is equal to the number of roots remaining. Also, remark that the number of root nodes never increases.


## Path compression

In union find, we can compress data structure, by changing nodes pointers such that they point directly to the root node of the group, so that we can find root nodes so much quicker in the future.

![[Pasted image 20230719163639.png]]

![[Pasted image 20230719163748.png]]

