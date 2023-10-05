- prev : [[Priority Queues]]

## Invariant
1. Min-heap : Every node is less than or equal to both of its children.
2. Complete : Missing items only at the bottom level (if any), all nodes are as far left as possible.
![[HeapValidate|700]]

## Methods
1. `add` : Add to the end of heap temporarily. `Swin up` the hierarchy to the proper place.
	- swimming involves swapping nodes if child < parent.
2. `getSmallest` : Return the root of the heap (This is guaranteed to be the minimum by our min-heap property.)
3. `removeSmallest` : Swap the last item in teh heap into the root. Sink down the hierarchy to the proper place
	- Sinking involves swapping nodes if parent > child.
![[HeapMethods|700]]

Next : [[Tree Representation]]

