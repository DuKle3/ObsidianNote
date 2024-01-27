prev : [[Prim's Algorithm]]
- Consider edges in order of increasing weight. Add to MST unless a cycle is created.
	- Repeat until V-1 edges.

![[Kruskal's Demo|700]]

> Implementation: 
> 	1. PQ to store the edge (sorted)
> 	2. Use WQU to store the vertices that is connected. 


## Implementation (Pseudocode)
```java
public class KruskalMST {
  private List<Edge> mst = new ArrayList<Edge>();

  public KruskalMST(EdgeWeightedGraph G) {
    MinPQ<Edge> pq  = new MinPQ<Edge>();
    for (Edge e : G.edges()) {
      pq.insert(e);
    }
    WeightedQuickUnionPC uf = new WeightedQuickUnionPC(G.V());
    while (!pq.isEmpty() && mst.size() < G.V() - 1) {
      Edge e = pq.delMin();
      int v = e.from();
      int w = e.to();
      if (!uf.connected(v, w)) {
        uf.union(v, w);
        mst.add(e);
      }
    }
  }
}
```

## Runtime
| Operation   | Number of Times | Time per Operation | Total Time    |
| ----------- | --------------- | ------------------ | ------------- |
| Insert      | E               | $O(\log E)$        | $O(E \log E)$ |
| Delete Min  | $O(E)$          | $O(\log E)$        | $O(E \log E)$ |
| Union       | $O(V)$          | $O(\log E)$        | $O(V \log V)$ |
| isConnected | $O(E)$          | $O(\log E)$        | $O(E \log V)$ |

- Assume E > V: $O(E \log E)$

> [!Note]
> If we use pre-sorted list of Edges (instead of PQ), we can simply iterate through the list in $O(E)$ times.
> So, overall runtime can be optimize to $O(V \log V)$
> (省去Insert, Delete Min)

> [!Note]
> Also note that if we use [[WQU with Path Compression | WQUPC]] we will get $O(V log^* V)$