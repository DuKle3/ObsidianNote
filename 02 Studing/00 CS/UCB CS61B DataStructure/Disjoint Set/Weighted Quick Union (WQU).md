- Improving [[Quick Union]], we shorter the tree.
- **New rule** : when `connect`, we always link the root of the **smaller** to **larger** one.

![[WQUDraw|700]]

- With the new rule : **Maximum height : $\log N$**

## Summery
| Implementation | Constructor      | `connect`        | `isConnect`      |
| -------------- | ---------------- | ---------------- | ---------------- |
| List Of Sets   | $\Theta(N)$ | $O(N)$      | $O(N)$      |
| Quick Find     | $\Theta(N)$ | $O(N)$ | $O(\log 1)$ |
| Quick Union    | $\Theta(N)$ | $O(N)$           | $O(N)$           |
| WQU            | $\Theta(N)$      | $O(\log N)$ | $O(\log N)$                  |

> [!Note]
> why don't we link trees based on height instead of weight.
> It more simple to implement.

- Next : [[WQU with Path Compression]]