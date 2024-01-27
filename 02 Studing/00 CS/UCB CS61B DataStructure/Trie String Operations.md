prev : [[Trie]]
## Prefix
- find all keys that match a given prefix : `keysWithPrefix("sa")`
- find longest prefix of : `longestPrefixOf("sample")`

![[Prefix matching|750]]

### Collect
- Give an algorithm for collecting all the keys in a Trie.
- `collect()` returns \[a, awls, sad, sam, same, sap]

```python
def collect():
	Create an empty list of results x.
	for ch in root.next.keys():
		colHelp(c, x, root.next.get(ch))
	return x

def colHelp(String s, List<String> x, Node n):
	if n.isKey:
		x.add(s)
	for ch in n.next.keys():
		colHelp(s + ch, x, n.next.get(ch))
```

### Key with Prefix
- Give an algorithm for keysWithPrefix.
- `keysWithPrefix("sa")` : \[sad, sam, same, sap]

```
1. Find the node a corresponding to the string (Pink)
2. Create an empty list x.
3. for c in a.next.keys():
	colHelp("sa" + c, x, a.next.get(c))
```
![[Prefix matching 2]]

> Find the Node, and Call `colHelp`

# Autocomplete Problem
- When a user types in a string hello, we:
	- call `keyWithPrefix("hello")`
	- Return the 10 strings with the highest value.

- but, we have problem
	1. We are collecting billions of results only to keep 10 !
	2. This is extremely inefficient.

## More efficient Autocomplete
- One way to address this issue:
	- Each node stores its own value, and the value of its best substring.
![[Prefix matching 3|750]]

# Summery
- Theoretically better performance.
- Have to decide on a mapping from letter to node.
	1. Data Indexed Char Map.
	2. Bushy BST.
	3. Hash Table.
- Supports special string operations
	- `longestPrefixOf()`
	- `keysWithPrefix()` : The heart of autocomplete !