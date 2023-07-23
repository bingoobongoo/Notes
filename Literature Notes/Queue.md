A **queue** is a linear data structure which models real world queues by having two primary operations, namely **enqueue** and **dequeue**.

![[Pasted image 20230622212730.png]]

### Enqueue
This operation is simply adding new element to the end of a que. It is also called "add" or "offer".

### Dequeue
It is removal of the very first element in the que. It is also called "poll" or "remove".

## Where is a Queue used?

- Any waiting line models a queue, for example a lineup at a movie theatre.
- Can be used to efficiently keep track of the ***x*** most recently added elements.
- Web server request managment where you want first come first serve.
- [[Breadth First Search]] graph traversal.

## [[Big-O Notation|Complexity]]

| Operation | Complexity |
| --- | --- |
| Enqueue | $O(1)$ |
| Dequeue | $O(1)$ |
| Peek | $O(1)$ |
| Contains | $O(n)$ |
| Removal | $O(n)$ |
| Is empty | $O(1)$ |

The example of queue code implementation ca be found [here](https://github.com/williamfiset/DEPRECATED-data-structures/blob/master/com/williamfiset/datastructures/queue/Queue.java).

See also:
- [[Priority Queue]]