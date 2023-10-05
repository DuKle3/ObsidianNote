## Dealing with Runtime
- If we have 100 items, and our ArrayList is of size 5.
	- In the best case, all items distribute evenly.
	- In the worst case, all items collision.

- There are two ways to fix:
	1. Dynamically growing our hashtable.
	2. Improving our HashCodes.

## Dynamically growing the hash table
- Suppose we have `M` buckets and `N` items.
- We say that our **load factor** is $\frac{N}{M}$ :
	1. Create a new HashTable with `2M` buckets.
	2. Iterate old one to new table (copy).
> [!Note]
> Assuming items are evenly distributed, about $N/M$ items long.
> That is, $\Theta(N/M)$ runtime. $N/M$ is **load factor** 
> So we have $\Theta(N/M) = \Theta(1)$

Next : [[Priority Queues]] and [[Heap]]