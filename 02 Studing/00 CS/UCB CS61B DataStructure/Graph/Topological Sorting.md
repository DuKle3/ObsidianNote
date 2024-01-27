- What algorithm do we use to find a valid ordering for these tast ?

![[Topological Sort Drawing]]

> [!Answer]
> - DFS postorder in a list.
> - Topological ordering is given by the reverse of the list.

- Post Order : \[7 4 1 3 0 6 5 2]

![[Pasted image 20231025145337.png]]

- We can think the process as sorting our nodes so they appear in an order consistent with edges.

# Directed Acyclic Graphs
- also called **DAG**
- A topological sort only exist in DAG. (no cycle)

## Shortest Paths
- Algorithm for DAG when nagative edges exist.

> [!Answer]
> Visit vertices in topological order.

## Longest Paths
### For general Graph
- Best known algorithm is exponential (really bad).
- Most important unsolved problem in mathematics.

### For DAG
- We can flip the sign of the edge weights
- Run DAG SPT
- Flip the sign again.
  Complete
![[Pasted image 20231025150018.png]]![[Pasted image 20231025150021.png]]