- If there is nothing at index, create a `LinkedList`
- If there is already something at index, simply add our new item to list.

## Method workflow
- `add` item:
	1. Get hashcode
	2. create new List, or add item to List.

- `contains` item: 
	1. Get hashcode
	2. If index is empty, return `false`
	3. Otherwise, check the Linked-List.

### Runtime Complexity
- Why is `contains` $\Theta(Q)$ ?
- Why is `add` $\Theta(Q)$ ?

### TradeOff
1. Space : Still unsolved
2. Handling collisions : ✅
3. Runtime complexity : we've lost some, in worst case will be $\Theta(N)$ .

## Solving space
- **modulo**

## Where we are
1. Space : ✅
2. Handling collisions : ✅
3. Runtime complexity : We lost some earlier at $\Theta(Q)$ for `add` and `contains`.

Next : [[Hash Table]]