## Basic Idea
- Root node partitions entire space into *left* and *right* (by x).
- All depth 1 nodes partition subspace into *up* and *down* (by y).
- All depth 2 nodex partition subspace into *left* and *right* (by x)

![[KdTreeDrawing|600]]

## Insertion
![[KdTreeInsertionDrawing|700]]

## Nearest Finding
- Suppose we have the k-d tree shown.
	- We want to find nearest((0, 7)).
	- Let's do a proper k-d tree traversal.
![[KdTreeNearestDemo|700]]
![[KdTreeNearestDemo 1|700]]
![[KdTreeNearestDemo 2|700]]
![[KdTreeNearestDemo 3|700]]
![[KdTreeNearestDemo 4|700]]
![[KdTreeNearestDemo 5|700]]
![[KdTreeNearestDemo 6|700]]
![[KdTreeNearestDemo 7|700]]

## Pseudocode
```python
def nearest(Node n, Point goal, Node best):
	if n is null:
		return best
	if n.distance(goal) < best.distance(goal):
		best = n
	if goal < n (according to n's comparator):
		goodSide = n."left" child
		badSide = n."right" child
	else:
		goodSide = n."right" child
		badSide = n."left" child
	best = nearest(goodSide, goal, best)
	if bad side may useful:
		best = nearest(badSide, goal, best)
	return best
```