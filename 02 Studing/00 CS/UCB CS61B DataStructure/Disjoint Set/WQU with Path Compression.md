- WQU is good, but we can get better.

### Thought
- both `connect` and `isConnected` always call `find`
- Thus, calling `connect` enough, all elements will point directly to the root eventually.

### Operation
- M operations on N nodes is $O(N + M lg^* N)$ 
- $lg^*$ is less than 5 for any realistic input.
- A tighter bound : $O(N + M \alpha (N))$, where $\alpha$ is the *inverse Ackermann function*.

## Summery

| Implementation            | Constructor       | `connect`         | `isConnect`      |
| ------------------------- | ----------------- | ----------------- | ---------------- |
| List Of Sets              | $\Theta(\log N)$  | $O(\log N)$       | $O(\log N)$      |
| Quick Find                | $\Theta(\log N)$  | $\Theta(\log N)$  | $\Theta(\log 1)$ |
| Quick Union               | $\Theta(\log N)$  | $O(N)$            | $O(N)$           |
| WQU                       | $\Theta(N)$       | $O(\log N)$       | $O(\log N)$      |
| WQU with Path Compression | $\Theta(N)$ | $O(\alpha (N))^*$ |     $O(\alpha (N))^*$             |
