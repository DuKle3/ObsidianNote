prev : [[Dijkstra's]]
## Simple idea
- Estimate 
- ex : direction of map

## Demo
- Insert all vertices into fringe PQ, storing vertices in order of `d(source, v) + h(v, goal)`.
- Repeat: Remove best vertex v from PQ, and relax all edges pointing from v.

> We only care *source* -> *target*

![[A star Demo 1|700]]

## A* Heuristic Example
### How do we get our estimate ?
- Estimate is an arbitrary **heuristic** h(v, goal).
- heuristic: "using experience to learn an imporve"
- Doesn't have to be perfect.


