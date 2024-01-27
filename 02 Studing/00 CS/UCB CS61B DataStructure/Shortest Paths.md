## Recap 
### Graph Problems
| Problem            | Problem Description                         | Solution | Efficiency                           |
| ------------------ | ------------------------------------------- | -------- | ------------------------------------ |
| s-t paths          | Find a path from s to every vertex          | DFS      | $O(V+E)$ time and $\Theta(V)$ space    |
| s-t shortest paths | Find a shortest path from s to every vertex | BFS      | $O(V+E)$ time and $\Theta(V)$ space |

#### Which is better ?
- Space Efficiency
	- DFS is worse for spindly graphs
		 - Call stack gets very deep
		 - Computer nees $\Theta(V)$ memory to remember recursive alls
	- BFS is worse for absurdly "bushy" graphs
		 - Queue gets very large

- And BFS will yields the wrong route from s to t.
![[Pasted image 20231006084038.png|700]]

## Algorithms

- [[Dijkstra's]]
- [[A star | A*]]

### Compare
- http://qiao.github.io/PathFinding.js/visual/

## Graph Problems Summery
| Probelm                 | Solution                     | Efficiency                                   |
| ----------------------- | ---------------------------- | -------------------------------------------- |
| pahts                   | [[DFS]]                      | $O(V+E)$ time, $\Theta(V)$ space             |
| shortest paths          | [[BFS]]                      | $O(V+E)$ time, $\Theta(V)$ space             |
| shortest weighted paths | [[Dijkstra's\| DijkstrasSP]] | $O(E \log V)$ time, $\Theta(V)$ space        |
| shortest weighted paths | [[A star\|A*]]               | Time depends on heuristic. $\Theta(V)$ space |

