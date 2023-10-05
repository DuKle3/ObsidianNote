- prev : [[DFS]]
---
- Breadth First Search

## Using Queue
- BFS pseudoCode
```
Initialize the fringe (a queue with the starting vertex) and mark that vertex.
Repeat until fringe is empty:
  Remove vertex v from the fringe.
  For each unmarked neighbor n of v:
    Mark n.
    Add n to fringe.
    Set edgeTo[n] = v.
    Set distTo[n] = distTo[v] + 1
```

- A *fringe* is just a term we use for the data structure (store the node on the frontier of our traversla's discovery process)
- we have two helper method : `edgeTo[...]` `distTo[...]`

### Invariant
- Distance to all items on **Queue** is always k or k+1 for some k.

![[BFSDrawing1|700]]
![[BFSDrawing2|700]]

Next : [[BFS Implementation]]