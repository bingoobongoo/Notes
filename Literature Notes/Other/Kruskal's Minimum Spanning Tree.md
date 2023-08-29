Given a graph $G = (V,E)$ we want to find a **minimum spanning tree** in the graph. A minimum spanning tree is a subset of the edges which connect all vertices in the graph with the minimal total edge cost.

![[Pasted image 20230709161221.png]]
(Graph before MST algorithm)

![[Pasted image 20230709161312.png]]
(Possible MST)

## List of steps

1) Sort edges by ascending edge weight
2) Walk through the sorted edges and look at the 2 nodes the edge belongs to, if the nodes are already unified we don't include this edge, otherwise we include it and unify the nodes
3) The algorithm terminates when every edge has been processed or all the vertices have benn unified


