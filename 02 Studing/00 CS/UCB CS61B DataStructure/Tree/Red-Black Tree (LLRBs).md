- prev : [[B-Tree]]
- LLRBs are a **representation** of B-Tree, because it is easier to work with in code.
- Recap [[Tree Rotation]]
## Invariant
1. No node ever has 2 red links. (follow the 2-3 Tree rules)
2. Every path from the root to a leaf has **the same number of black links**.
   (this is because every leaf in a 2-3 tree has the same numbers of links from root.)

## Runtime
1. height $O(\log N)$
2. `contains` is trivially $O(\log N)$
3. `insert` is $O(\log N)$
	1. add the new node.
	2. rotation and color flip operation per insert.
## Detail
- 2-3 Tree
![[Pasted image 20230924205659.png]]
- corresponding LLRB
![[Pasted image 20230924205724.png]]

### Height
- total height is H (black) + H + 1 (red) = 2H + 1 
> red edges have most black edge + 1.
- ![[Pasted image 20230924205902.png]]

### Insertion Rules
1. When inserting : Use a red link.
2. If there is a right leaning "3-node" : `RotateLeft`
3. If there is are two consecutive left links. : `RotateRight`
4. If there are any nodes with two red children : `ColorFlip`
![[Pasted image 20230924210309.png]]
![[Pasted image 20230924210951.png]]
### Implementation
`put` function only 3 line more than BST. (Not include helper method)
```java
private Node put(Node h, Key key, Value val) {
if (h == null) { return new Node(key, val, RED); }

int cmp = key.compareTo(h.key);
if (cmp < 0) {
	h.left = put(h.left, key, val);
}
else if (cmp > 0) {
	h.right = put(h.right, key, val);
}
else {
	h.val = val;
}

if (isRed(h.right) && !isRed(h.left))      { h = rotateLeft(h); }
if (isRed(h.left)  &&  isRed(h.left.left)) { h = rotateRight(h); }
if (isRed(h.left)  &&  isRed(h.right))     { flipColors(h);}
}
```