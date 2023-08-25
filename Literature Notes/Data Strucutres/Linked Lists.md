A **linked lists** is a sequential list of nodes that hold data and [[Pointers|pointers]] to other nodes containing data.

![[Pasted image 20230622145554.png]]

Every node has a pointer that points to anothe node and the last node points to NULL.

### Where are linked lists used?

- Used in many List, [[Stack]] and [[Queue]] implementations.
- Great for creating circular lists.
- Can easily model real world objects.
- Often used in th implementations of adjency lists for [[Graphs|graphs]].

### Terminology

**Head** - the first node in a linked list
**Tail** - the last node in a linked list
**Pointer** - reference to another node
**Node** - An object containing data and pointers

![[Pasted image 20230622150725.png]]

### Singly Linked vs Doubly Linked lists

**Singly linked** lists only hold a reference to the next node. In the implementation you always maintain a reference to the **head** node and a reference to the **tail** node for quick additions/removal.

![[Pasted image 20230622151314.png]]

**Doubly linked** lists have more references, because each node holds referecnes to next and previous node. 

![[Pasted image 20230622151342.png]]

### Singly and Doubly linked lists pros and cons

| List | Pros | Cons |
| --- | --- | ---| 
| Singly Linked | Uses less memory, simpler implementation | Cannot easily access previous elements |
| Doubly Linked | Can be traversed backwards | Takes 2 times more memory |

### [[Big-O Notation|Complexity]]

| Operation | Singly Linked complexity | Doubly Linked complexity |
| --- | --- | --- |
| Search | $O(n)$ | $O(n)$ |
| Insert at head | $O(1)$ | $O(1)$ |
| Insert at tail | $O(1)$ | $O(1)$ |
| Remove at head | $O(1)$ | $O(1)$ |
| Remove at tail | $O(n)$ | $O(1)$ |
| Remove in middle | $O(n)$ | $O(n)$ |

Code implementation of linked lists is [here](https://github.com/williamfiset/DEPRECATED-data-structures/blob/master/com/williamfiset/datastructures/linkedlist/DoublyLinkedList.java)
