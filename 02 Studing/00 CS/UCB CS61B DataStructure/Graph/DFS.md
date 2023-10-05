- Depth-First Search

1. Mark v.
2. For each unmarked adjacent vertex w:
	1. set edgeTo[w] = v.
	2. DFS(w)

> [!Note]
> Note the order of **DFS calls** and **DFS return**.


![[DFSDrawing1|800]]
![[DFSDrawing2|800]]

- DFS Preorder : 012543678 (dfs calls).
- DFS Postorder : 347685210 (dfs returns).


Next : [[BFS]] , [[DFS Implementation]]