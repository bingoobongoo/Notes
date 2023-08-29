A Breadth First Search is an [[Algorithms|algorithm]] for searching a [[Graphs|graph]] for a node that satisfies given property. It starts at the tree root and explores all the other nodes. The way the other nodes are explored is as follows: mark current node as visited and mark all the unvisited neighbouring nodes as "to visit". Do it for every unvisited node from the previous step before going further on.

![[Animated_BFS.gif]]

## Example of code implementation

Let q be a [[Queue]]:

```python
q.enqueue(startingNode)
startingNode.isVisited = True
while q.isEmpty == False:
	node = q.dequeue()
	for neighbour in node.neighbours():
		if neighbour.isVisited == False:
			neighbour.isVisited = True
			q.enqueue(neighbour)
```


