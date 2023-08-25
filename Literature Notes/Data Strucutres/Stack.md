A **stack** is a one-ended linear [[Data Structures|data structure]] which models a real world stack by having two primary operations, namely **push** and **pop**.

![[Pasted image 20230622152952.png]]

### Where is stack used?

- Used by undo mechanism in text editors 
- Used in compiler syntax checking for matching brackets and braces.
- Used behind the scenes to support recursion by keeping track of previous function calls.
- Can be used to do a [[Depth First Search]] on graph.

### [[Big-O Notation|Complexity]] 

| Operation | Complexity |
| --- | --- |
| Push | $O(1)$ |
| Pop | $O(1)$ |
| Peek | $O(1)$ |
| Search | $O(n)$ |
| Size | $O(1)$ |

Stack implementation can be found [here](https://github.com/williamfiset/DEPRECATED-data-structures/blob/master/com/williamfiset/datastructures/stack/Stack.java).

