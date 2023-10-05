```java
public public class BreadthFirstPaths {
    private boolean[] marked;
    private int[] edgeTo;
    ...

    private void bfs(Graph G, int s) {
        Queue<Integer> fringe = new Queue<Integer>();
        fringe.enqueue(s);
        marked[s] = true;
        while (!fringe.isEmpty) {
            int v = fringe.dequeue();
            for (int w : G.adj(v)) {
                if (!marked[w]) {
                    fringe.enqueue(w);
                    marked[w] = true;
                    edgeTp[w] = v;
                }
            }
        }
    }
}
```

## Runtime 
- is also $O(V + E)$
	- Based on same cose model: $O(V)$.next() calls and $O(E)$ marked[w] checks.