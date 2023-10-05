### Common design pattern in graph algorithms

- Create a graph object.
- Pass the graph to a graph-processing method (or constructor) in a client class.
- Query the client class for information.

```java
public class Paths {
  /** Find all paths from G. */
  public Paths(Graph G, int s);

  /** Is there a path from s to v ? */
  boolean hasPathTo(int v);

  /** Path from s to v. */
  Iterable<Integer> pathTo(int v);
}
```

## DFS, Recusive Implementation

```java
public class DepthFirstPaths {
    private bollean[] marked;
    private int[] edgeTo;
    private int s;

    public DepthFirstPaths(Graph G, int s) {
        ...
        dfs(G, s);
    }

    private void dfs(Graph G, int v) {
        marked[v] = true;
        for (int w : G.adj(v)) {
            if (!marked[w]) {
                edgeTo[w] = v;
                dfs(G, w);
            }
        }
    }
    ...
}
```

### Runtime of Constructor
- $O(V + E)$
	1. Each vertex is visited a most once : $O(V)$
	2. Each edge is considered at most twice : $O(E)$  (no more tehan 2E calls)

- Argument: Can only visit a vertex if there is an edge to it.
	- \# of DFS calls i bounded above by E.
	- So why not just say $O(E)$
 
> No!
> Because Constructor has to create an all false marked array.