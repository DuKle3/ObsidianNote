- Imagine each of our sets as a tree.
- for example :
![[QuickUnionDraw|700]]

> [!Note]
> Using **only an array**. (visualize it as tree)
> we defind a helper function `find (int item)`, whick return the root.


### Method
- `connect(x, y)`
1. find(5) -> 3
2. find(2) -> 0
3. Set `find(5)`'s value to `find(2)` , aka `parent[3] = 0`
![[QuickUnionMethodDraw|700]]

- `isConnect(x, y)` : check `find(x) == find(y)`

> [!Note]
> The tree can become very long (spindly), 
> `connect, isConnect` is upper bounded be $O(\log N)$ 

## Summery
| Implementation | Constructor      | `connect`        | `isConnect`      |
| -------------- | ---------------- | ---------------- | ---------------- |
| List Of Sets   | $\Theta(\log N)$ | $O(\log N)$      | $O(\log N)$      |
| Quick Find     | $\Theta(\log N)$ | $\Theta(\log N)$ | $\Theta(\log 1)$ |
| Quick Union    | $\Theta(\log N)$ | $O(N)$      | $O(N)$                 |

- Next : [[Weighted Quick Union (WQU)]]