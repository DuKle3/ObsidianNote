## Level Order Traversal
## Pre-Order Traversal
- Start at the root, **Visit the root** (aka, do the **action**)
```java
preOrder(BSTNode x) {
  if (x == null) { return; }
  print(x.key);
  preOrder(x.left);
  preOrder(x.left);
}
```
## In-Order Traversal
- Instead of **visiting** (aka **printing** in here) first.
```java
inOrder(BSTNode x) {
  if (x == null) { return; }
  inOrder(x.left);
  print(x.key);
  inOrder(x.right);
}
```
## Post-Order Traversal
```java
postOrder(BSTNode x) {
  if (x == null) { return; }
  postOrder(x.left);
  postOrder(x.right);
  print(x);
}
```
### A useful visual trick
![[TreeTraversalsOrder|750]]
1. Pre-order : **visit** when we pass the LEFT of the Node.
2. In-order  : **visit** when we cross the BOTTOM of the Node.
3. Post-order : **visit** when we cross the RIGHT of the Node.

Next : [[Graph]]