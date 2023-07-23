In programming, an array can be either **static** or **dynamic**. A static array is a fixed length container containing $n$ elements **indexable**[^1] from the range $[0, n-1]$.

Arrays are one of the most commonly used [[Data Structures|data structures]]. They are just everywhere.

### Operation [[Big-O Notation|Complexity]]

| Operation | Static Array | Dynamic Array |
| --- | --- | --- |
| Access | $O(1)$ | $O(1)$ |
| Search | $O(n)$ | $O(n)$ |
| Insertion | N/A | $O(n)$ |
| Appending | N/A | $O(1)$ |
| Deletion | N/A | $O(n)$ |

## Static Array

Elements in a static array are indexed from 0. There is no other way to access data in an array different than by its index number.

![[Pasted image 20230621234823.png]]

## Dynamic Array

In opposition to static array, dynamic array can grow and shirnk in the runtime of program.

![[Pasted image 20230621235027.png]]

## How to create dynamic array?

1) Create a static array with initial capacity.
2) Add elements to the underlying static array keeping track of number of elements added.
3) If adding another element exceeds the capacity, then create a new static array with twice the capacity of the initial array and copy the original elements into it.

Code implementation of dynamic array is [here](https://github.com/williamfiset/DEPRECATED-data-structures/blob/master/com/williamfiset/datastructures/dynamicarray/DynamicArray.java).

[^1]: Indexable means that each slot in the array can be referenced with by a number.