## Warm-up Problem
- Given a undirected graph, determine if it contains any cycles.

### Approach 1: Do DFS from 0
- keep going until you see a marked vertex.
- Potential danger:
	- look back
	- Sol: just don't count the node you came from.

- Worst case: $O(V + E)$ 

### Approach 2: Use a WeightedQuickUnionUF object
- For each edge, check if the two vertices are connected.
	- If not, union them.
	- If so, there is a cycle.

- Worst case: $O(V + E log^* V)$ 

# Spanning Trees
- Given an **undirected** graph, a **spanning tree** T is a subgraph of G
	- Is connected.
	- Is acyclic.
	- Includes all of the vertices.
![[SpanningTreeValid|750]]
## Minimum spanning Tree (MST)
- A minimum spanning tree is a spanning tree of minimum **total weight**.

## MSP vs SPT
- If the MST for this graph also a shortest paths tree ?
- If so, using which node as the starting node for this SPT ?
![[MST vs SPT|600]]
> SPT from B, also a MST.

> [!Note] 
> A shortest paths tree depends on the **start vertex**.

- So, potential algorithm : 
	1. find good vertex
	2. do Dijkstra
- is it work ?

#### Example:
- Is there a node whose SPT is also the MST ?
- No

![[SpanningTreeFromSPT|700]]

## Cut Property
- A **cut** is an assignment of a graph's nodes to two non-empty sets.
- A **crossing edge** is an edge which connects a node from one to a node from the other set.

> [!property]
> Given any cut, minimum weight crossing edge is in the MST.
![[CutProperty|650]]


## Algorithm
1. [[Prim's Algorithm]]
2. [[Kruskal's Algorithm]]