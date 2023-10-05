- Using a single array of integers
1. The **indices of the array** represent the elements of our set.
2. The **value at an index** is the set number it belongs to.

- for example
![[QuickFindDraw|800]]

| Implementation | Constructor      | `connect`        | `isConnect`      |
| -------------- | ---------------- | ---------------- | ---------------- |
| List Of Sets   | $\Theta(\log N)$ | $O(\log N)$      | $O(\log N)$      |
| Quick Find     | $\Theta(\log N)$ | $\Theta(\log N)$ | $\Theta(\log 1)$ | 

- Next : [[Quick Union]]