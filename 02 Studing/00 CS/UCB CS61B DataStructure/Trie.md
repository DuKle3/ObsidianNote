Trie is a specific implementation for Sets and Maps that is specialized for string.

- Short for Re==trie==val.
- Searching will only fail if we hit an unmarked node or we fall off the tree.

# Why
## Runtime for searching strings
| Type      | contains(x)       | add(x)           |
| --------- | ----------------- | ---------------- |
| BST       | $\Theta (\log N)$ | $\Theta(\log N)$ |
| HashTable | $\Theta(1)^+$     | $\Theta(1)^{*+}$                 |

- * : indicates "on average".
- + : Assuming items are evenly spread.

> Can we do better ?
## Implementation
### First approach
- Each node stores
	1. letter
	2. a map from c to all child nodes
	3. color

```java
public class TrieSet {
  private static final in R = 128; // ASCII
  private Node root;

  private static class Node {
    private char ch;
    private boolean isKey;
    private DataIndexedCharMap<Node> next;
    private Node(char c, boolean b, int R) {
      ch = c;
      isKey = b;
      next = new DataIndexedCharMap<>(R);
    }
  }
}
```
![[Pasted image 20231025134548.png]]

- If we use a DataIndexedCharMap to track children, every node has R links.
```java
public class DataIndexedCharMap<V> {
  private V[] items;
  public DataIndexedCharMap(int R) {
    items = (V[]) new Object[R];
  }
}
```

> [!Observation]
> The letter stored inside each node is actually reduntant.
> - The node won't be need to store the char.


## Trie Performance 

| Type               | key type   | contains(x)       | add(x)           |     |
| ------------------ | ---------- | ----------------- | ---------------- | 
| BST                | comparable | $\Theta (\log N)$ | $\Theta(\log N)$ |     
| HashTable          | hashable   | $\Theta(1)^+$     | $\Theta(1)^{*+}$ |    
| Data Indexed Array | chars      | $\Theta(1)$       | $\Theta(1)$      |     
| Trie (DIA)         | strings    | $\Theta(1)$       |  $\Theta(1)$                |     

- * : indicates "on average".
- + : Assuming items are evenly spread.

> But the Trie use huge memory.

## Alternate Child Tracking Strategies
![[Pasted image 20231025135753.png]]
### 1. Hash Table

![[Pasted image 20231025135714.png]]
### 2. BST
![[Pasted image 20231025135721.png]]

- Data Indexed Char Map : very fase, but memory hungry.
- Hash Table : Almost as fast, uses less memory.
- Balanced BST : A little slower than Hash Table, uses similar amount of memory?

Next : [[Trie String Operations]]