- Recap : [[Tree Traversal]]

## What is a graph ?
- A set of nodes (or vertices)
- A set of zero of more edges, whick connect two nodes.

### Simple Graph only
- No edge from a node to itself. *loop*
- Two nodes have at most 1 edge. *parallel edge*

- And more definitions : 
	1. directed
	2. cyclic

## Graph Traversals
- [[DFS]]  
- [[BFS]]


## Graph Representations
- Our choices can have profound implications on:
1. Runtime
2. Memory usage
3. Difficulty of implementing various graph algorithms.

### API
```java
public class Graph {
  /** Create empyt graph with v vertices. */
  public Graph(int V);

  /** add and edge v-w. */
  public void addEdge(int v, int w);

  /** vertices adjacent to v. */
  Iterable<Integer> adj(int v);

  /** number of vertices. */
  int V();

  /** number of edges. */
  int E();
  ...
}
```

### 1: Adjacency Matrix

![[GraphAdjacencyMatrix|650]]
- Total runtime to iterate over all neighbors of v is $\Theta(V)$.
	- have to iterate through Entire array.

#### Graph Printing Runtime
```java
for (int v = 0; v < G.V(); v += 1) {
  for (int w : G.adj(v)) {
    System.out.println(v + "-" + w);
  }
}
```

- --> $\Theta(V^2)$
	1. Runtime to iterate over v's neighbors
		- $\Theta(V)$
	2. How many vertices do we consider ?
		- V times.

### 2: Edge Sets: Collection of all edges.
- Ex: `HashSet<Edge>`
- {(0, 1), (0, 2), (1, 2)} : for directed graph.

### 3: Adjacency lists.
- Most popular approach for representing graphs.
![[GraphAdjacencyList|650]]
#### Graph Printing Runtime
- --> $\Theta(V + E)$
	1. Create V iterators.
	2. Print E times.

## Compare
| idea             | `addEdge(s,t)` | `for(w : adj(v))`          | `print()`       | `hasEdge(s,t)`      | space used    |
| ---------------- | -------------- | -------------------------- | --------------- | ------------------- | ------------- |
| adjacency matrix | $\Theta(1)$    | $\Theta(V)$                | $\Theta(V^2)$   | $\Theta(1)$         | $\Theta(V^2)$ |
| list of edges    | $\Theta(1)$    | $\Theta(E)$                | $\Theta(E)$     | $\Theta(E)$         | $\Theta(E)$   |
| adjacency list   | $\Theta(1)$    | $\Theta(1)$ to $\Theta(V)$ | $\Theta(V + E)$ | $\Theta(degree(v))$ |  $\Theta(E + V)$             |

- Many graph algorithms rely heavily on `adj(s)`.
- Most graph are sparse.

## BFS & DFS Implementation
- [[DFS Implementation]]
- [[BFS Implementation]]

Next : [[Shortest Paths TODO]]