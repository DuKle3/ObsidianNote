- prev : [[Binary Search Tree]]
## Invariant
- B-Tree (also referred to as 2-3 Trees), bushy structure.
- Each node can have up to `2 items` and `3 children` (for 2-3 Tree)
- ==All leaves are the same distance from the root==

## Runtime
- largest possible height is all non-leaf nodes have 1 items.
- smallest possible hieght is all nodes have L items.
- Overall height is therefore $\Theta(\log N)$
## Detail
### adding

1. adding to a leaf node.
2. pushing the excess items up until it follows the rules.

![[Pasted image 20230924204033.png]]
![[Pasted image 20230924204042.png]]
![[Pasted image 20230924204716.png]]
- [B-Tree Visualizer](https://tinyurl.com/balanceYD)

### Deletion (Extra)
TODO:

Next: [[Red-Black Tree (LLRBs)]]