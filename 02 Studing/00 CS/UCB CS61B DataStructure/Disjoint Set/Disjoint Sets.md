- Two sets are named *disjoint sets* if they have no elements in commom. A Disjoint-Sets (or Union-Find) data structure keeps track of a fixed number of elements partitioned into a number of disjoint sets. The data structure has two operation.
### API
```java
void connect(int p, int q);
boolean isConnected(int p, int q);
```

### Design decisions
1. [[Quick Find]]
2. [[Quick Union]]
3. [[Weighted Quick Union (WQU)]]
4. [[WQU with Path Compression]]