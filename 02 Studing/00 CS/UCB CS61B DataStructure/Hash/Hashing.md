prev : [[Tree]]
Skip to summery : ...
## Issue with BST
1. Require items be comparable
2. complexity of $\Theta (\log N)$ 

### A first attempt: `DataIndexedIntergerSet`
- maintain a gigantic array.
```java
public class DataIndexedIntegerSet {
  private boolean[] present;
  public DataIndexedIntegerSet() {
    present = new boolean[200000000];
  }
  public void add(int i) {
    present[i] = true;
  }
  public boolean contains(int i) {
    return present[i];
  }
}
```

> [!Note] 
> 1. Extremely wasteful
> 2. What about `String`
### Solving the word-insertion problem
#### Strategy 1: Use the first letter
- "cat" -> 3, "Dog" -> 4
- but, we will encounter **collision**

#### Strategy 2: Avoiding collision
- use **base 26** 
- "cat" = "c" $26^2$ + "a" $26^1$ + "t" $26^0$ = 2074

#### Where are we?
- better than $\Theta(\log N)$ .
- Allow for non-comparable
- can insert Integer and English word
- **But still very wasteful**

Next : [[Hashing Inserting Strings and Overflow]]