## Invariant
- For a node X, every key in the left is less than X and every key in the right is greater than X.

## Runtime
- O(log N) for "bushy" tree
- O(N)     for "splindly" tree

## Implementation
### Insert
```java
static BST insert(BST T, Key ik) {
if (T == null) {
	return new BST(ik);
}
if (ik < T.key) {
	T.left = insert(T.left, ik);
}
else if (ik > T.key) {
	T.right = insert(T.right, ik);
}
return T;
}
```

> [!Note]
> A commom rookie bad habit to avoid : *Arms length recursion*
```java
 if (T.left == null) {
 	T.left = new BST(ik);
 }
else if (T.right == null) {
	T.right = new BST(ik);
}
```

### Delete
1. Deletion key has no children. -> just delete
2. Deletion key has one child. -> move its parent pointer.
3. Deletion key has two children.
	1. find the largest in the left 
	2. find the smallest in the right
	3. choose one to replace it.

> Leap of Faith
```java
private Node remove(Node x, K key) {  
    int cmp = x.key.compareTo(key);  
    if (cmp > 0) {  
        x.left = remove(x.left, key);  
    }    
    if (cmp < 0) {  
        x.right = remove(x.right, key);  
    }    
    else {  
        if (x.left == null) {  
            return x.right;  
        }        
        if (x.right == null) {  
            return x.left;  
        }        
        Node originalNode = x;  
        x = getMinNode(x.right);  
        x.left = originalNode.left;  
        x.right = remove(originalNode.right, x.key);  
    }    
    return x;  
}
```

![[BST Deletion|600]]

Next: [[B-Tree]]