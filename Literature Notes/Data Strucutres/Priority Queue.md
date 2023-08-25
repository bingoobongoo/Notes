A **priority queue** is an [[Data Structures#Abstract Data Type|Abstract Data Type]] that operates similar to a normal [[Queue|queue]] except that ==each element has a certain priority==. The priority of elements in the priority queue determine the order in which elements are removed from it.

> [!NOTE] Comparable Data
> Priority queues only support **comparable data**, meaning the data inserted into the priority queue must be able to be ordered in some way either from least to greatest or from greatest to least. This is so that we are able to assign relative priorities to each element.
> 

## [[Heap]] 

A priority queue uses something called **heap** to determine which data should it remove from queue. A heap is a tree based [[Data Structures|data structure]] that satisfies the **heap invariant** (also called heap property): If A is a parent node of B, then A is ordered with respect to B for all nodes A, B in the heap.

![[Pasted image 20230623114716.png]]

## Where is a Priority Queue used?

- Used in certain implementations of [[Dijkstra Alghorithm]]
- Anytime there is a need to fetch the 'next best' or 'next worst' element
- Used in [[Huffman Coding]] (which is often used as a lossless data compression)
- [[Best First Search]] algorithms such as A* use priority queue to continuously grab the next most promising node
- Used in [[Minimum Spanning Tree]] alghorithm

## [[Big-O Notation|Complexity]] of Priority Queue with heap

| Operation | Complexity |
| --- | --- |
| Binary Heap Construction | $O(n)$ |
| Polling | $O(\log n)$ |
| Peeking | $O(1)$ |
| Adding | $O(\log n)$ |
| Naive Removing | $O(n)$ |
| Advanced Hash Table Removing | $O(\log n)$ |
| Naive Contains | $O(n)$ |
| Contains with Hash Table | $O(\log n)$ |

## Ways of implementing a Priority Queue

Priority queue are usually implemented with heaps since this gives them the best possible time complexity.

The priority queue is an abstract data type, hence heaps are not the only way to implement it. As an example, an unsorted list could be used, but this would result in not that good time complexity.

![[Pasted image 20230627214926.png]]

![[Pasted image 20230627215102.png]]

## [[Hash table]]

A **hash table** provides a constant time lookup and update for a mapping from a key (the node value) to a value (the index).

It helps to reduce a time for removing an element from heap by reducing complexity from $O(n)$ to $O(\log n)$. 
