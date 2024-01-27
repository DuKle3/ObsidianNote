### Goal : Find the shortest paths from *source* to some *target*
skip : [[Dijkstra's#Dijkstra's Algorithm|Dijkstra's Algorithm]]
## Creating an Algorithm
- Algorithm begins in state below. All vertices unmarked. All distances infinite.  
- No edges in the SPT
![[Dijkstra's Drawing|650]]

### Bad algorithm 1 : Perform a DFS. 
- For each edge from v to w, if w is not already part of SPT, add the edge
![[Dijkstra's Drawing 1|700]]

### Bad algorithm 2 : Perform a DFS.
- For each edge from v to w, add edge to the SPT **only if that edge yields better distance.** -> call this "edge relaxation"


![[Dijkstra's Drawing 2|700]]
- Improvements :
	- Use beeter edges if found.

### Dijkstra's Algorithm : Perform a *best first search*
- For each from v to w, **relax that edge**.
![[Dijkstra's Drawing 3|700]]
- Improvements :
	- Use better edges if found.
	- Traverse "best first".

## Dijkstra's Algorithm
- Insert all vertices into fringe PQ, storing vertices in order of distance from source.
- Repeat : Remove vertex v from PQ, and relax all edges pointing from v.
![[Dijkstra's Drawing Demo|700]]
![[Dijkstra's Drawing Demo2|700]]

## Correctness and Runtime
### Pseudocode

```python
def Dijkstra's():
	PQ.add (source, 0)
	for other vertices v, PQ.add(v, infinity)
	while (PQ is not empty):
		p = PQ.removeSmallest()
		Relax all edges from p

def Relaxing(vertex p,vertex q, weight w):
	if (distTo[p] + w < distTo[q]):
		distTo[q] = distTo[p] + w
		edgeTo[q] = p
		PQ.changePriority(q, distTo[q])

```

### Invariants
- edgeTo[v] is the best known predecessor of v.
- distTo[v] is the best known total distance from *source* to v.
- PQ contains all unvisited vertices in order of distTo.

### Properties
- Always visits vertices in order of total distance from source.
- Relaxation always fails on edges to visited (white) vertices.


### Runtime
- PQ operation count, assuming binary heap based PQ:

| operations        | # of operations | Cost per opertaion | Total cost         |
| ----------------- | --------------- | ------------------ | ------------------ |
| PQ add            | V               | $O(V)$        | $O(V \log V)$ |
| PQ removeSmallest | V               | $O(\log V)$        | $O(V \log V)$      |
| PQ changePriority | E               | $O(\log V)$        |  $O(E \log V)$                  |

- Overall runtime : $O(V \log V + V \log V + E \log V)$ 
- Assuming E > V --> $O(E\log V)$

- Next: [[A star|A*]]