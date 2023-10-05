prev : [[Hashing]]

- Recall that **ASCII**, the largest value is 126 (base / multiplier)
- If we still use prev algorithm to calculate HashCode, we will encounter **Overflow**

### Overflow issues
- There are a total 4,294,967,296 integers in Java.

> We must handle collisions.

## Hash Codes
- In computer science, taking an object and convertin it into some integer is called "computing the **hash code** of the object".
- Every Object in Java has a default `.hashcode()` method.(Java computes this by figuring out wherer the `Object` sits in memory)

- [[Hash#^e1a320| Properties of HashCodes]]

### Pending issues
- Space : still wasteful
- Handling Collisions

Next : [[Hashing Handling Collisions]]