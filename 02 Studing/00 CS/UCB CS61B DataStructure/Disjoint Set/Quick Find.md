- Using a single array of integers
1. The **indices of the array** represent the elements of our set.
2. The **value at an index** is the set number it belongs to.

- for example
![[QuickFindDraw|800]]


| Implementation | Constructor      | `connect`        | `isConnect`      |
| -------------- | ---------------- | ---------------- | ---------------- |
| List Of Sets   | $\Theta(N)$ | $O(N)$      | $O(N)$      |
| Quick Find     | $\Theta(N)$ | $O(N)$ | $O(\log 1)$ |


- Next : [[Quick Union]]