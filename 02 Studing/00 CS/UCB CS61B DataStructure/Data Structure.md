## Search Data Structures (The particularly abstract ones)
| Name          |        Storage Operaion         | Primary Retrieval Operation | Retrieve By:   |
| ------------- |:-------------------------------:| --------------------------- | -------------- |
| List          | `add(key)` `insert(key, index)` | `get(index)`                | index          |
| Map           |        `put(key, value)`        | `get(key)`                  | key identity   |
| Set           |           `add(key)`            | `containsKey(key)`          | key idenetiy   |
| PQ            |           `add(key)`            | `getSmallest()`             | key order      |
| Disjoint Sets |      `connect(int1, int2)`      | `isConnected(int1, int2)`   | two int values |

### Abstraction often happens in layers!
- [[Priority Queues]] --> [[Heap]] --> [[Tree Representation]]
- [[Hash Table]] (TODO) --> Array of Buckets --> Bucket --> 
	- ArrayList
	- Linked List
	- BST
	- HashSet
