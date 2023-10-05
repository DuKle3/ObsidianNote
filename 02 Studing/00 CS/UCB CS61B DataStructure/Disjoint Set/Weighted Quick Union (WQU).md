- Improving [[Quick Union]], we shorter the tree.
- **New rule** : when `connect`, we always link the root of the **smaller** to **larger** one.

![[WQUDraw|700]]

- With the new rule : **Maximum height : $\log N$**

## Summery
| Implementation | Constructor      | `connect`        | `isConnect`      |
| -------------- | ---------------- | ---------------- | ---------------- |
| List Of Sets   | $\Theta(\log N)$ | $O(\log N)$      | $O(\log N)$      |
| Quick Find     | $\Theta(\log N)$ | $\Theta(\log N)$ | $\Theta(\log 1)$ |
| Quick Union    | $\Theta(\log N)$ | $O(N)$           | $O(N)$           |
| WQU            | $\Theta(N)$      | $O(\log N)$ | $O(\log N)$                  |

> [!Note]
> why don't we link trees based on height instead of weight.
> It more simple to implement.

- Next : [[WQU with Path Compression]]