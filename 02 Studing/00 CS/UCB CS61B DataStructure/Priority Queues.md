### API
```java
/** (min) PQ : Allowing tracking and removal of the smallest item. */
public interface MINPQ<Item> {
	public void add(Item x);
	public Item getSmallest();
	public Item removeSmallest()
	public int size();
}
```

## Summery 
- PQ is an Abstract Data Type that optimizes for handling minimum or maximum elements.
- There can be *space/memory* benefits to using this data structure.
- A proper data structure for this is to use [[Heap]].
### Implementation
| Data Structure | add              | getSmallest      | removeSmallest   |
| -------------- | ---------------- | ---------------- | ---------------- |
| Ordered Array  | $\Theta(\log N)$ | $\Theta(\log 1)$ | $\Theta(\log 1)$ |
| Bushy BST      | $\Theta(\log N)$ | $\Theta(\log N)$ | $\Theta(\log N)$ |
| Hash Table     | $\Theta(\log 1)$ | $\Theta(\log N)$ | $\Theta(\log N)$ |
| Heap           | $\Theta(\log N)$ | $\Theta(\log 1)$ | $\Theta(\log N)$                 |

## Note
1. Heap is log N time AMORTIZED (some risizes)
2. Heap handle duplicate. (more naturally than BSTs)
3. Array based heaps take less memory.