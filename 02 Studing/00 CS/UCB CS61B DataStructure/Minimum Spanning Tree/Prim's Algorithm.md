## First Approach
- Start from some arbitrary start node.
	- Add shortest edge that has one node inside the MST under construction.
	- Repeat until V-1 edges.
> [!Note]
> If edges are not unique, the spanning tree may not be unique.


![[Prim's Demo Conceptual|700]]

## Implementation
- The conceptual version is highly ineffiecient.
	- Iterating over purple edges shown is unnecessary and slow

> We can use some cleverness and a PQ to speed things up.

- Very similar to Dijkstra's !

## Better Approach
- Insert all vertices into fringe PQ, storing vertices in order of distance from tree.
- Repeat: Remove (closest) vertex v from PQ, and relas all edges pointing from v.
> [!Note]
> 1. 虛線表示"暫存" (目前最優解)，利用 distTo 和 edgeTo 來實現暫存功能。
> 2. 當 Vertex 從 fringe 中移除，才表示確定了路徑 (可以發現 distTo 被消掉)


![[Prim's Demo 1|700]]![[Prim's Demo 2|700]]
# Prim's vs Dijkstra's
- Prim's and Dijkstra's algorithm are exactly the same, except:
	- Dijkstra's considers =="Distance from the source."==
	- Prim's considers =="Distacne from the tree." ==

## Implementation (Pseudocode)
```java
public class PrimMST {
  public PrimMST(EdgeWeightedGraph G) {
    edgeTo = new Edge[G.V()];
    distTo = new double[G.V()];
    marked = new boolean[G.V()];
    fringe = new SpecialPQ<Double>(G.V());

    distTo[s] = 0.0;
    setDistancesToInfinityExceptS(s);
    insertAllVertices(fringe);

    /* Get vertices in order of distance from tree. */
    while (!fringe.isEmpty()) {
      int v = fringe.delMin();
      scan(G, v);
    }
  }
}

  private void scan(EdgeWeightedGraph G, int v) {
    marked[v] = true;
    for (Edge e : G.adj(v)) {
      int w = e.other(v);
      if (marked[w]) { continue; }
      if (e.weight() < distTo[w]) {
        distTo[w] = e.weight();
        edgeTo[w] = e;
        pq.decreasePriority(w, distTo[w]);
      }
    }
  }
```

## Runtime
- PQ operation count:
	- Insertion: V, each $O(\log V)$ time.
	- Delete-min: V, each $O(\log V)$ time.
	- Decrease priority: $O(E)$, each costing $O(\log V)$ time.

- Overall runtime: $O(V \log V + V \log V + E \log V)$
	- Assuming E > V, --> $O(E \log V)$.

Next : [[Kruskal's Algorithm]]