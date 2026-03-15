Collection in [Java]

**Key Numbers**
- Default capacity: 16
- Default load factor: 0.75
- Resize trigger: when `size > capacity * loadFactor`, the array doubles and all entries are **rehashed**

### The `hashCode()` and `equals()` Contract

- If `a.equals(b)` is true → `a.hashCode() == b.hashCode()` **must** be true
- If hashCodes are equal, `equals()` **may or may not** be true (collision)
- **If you override `equals()`, you must override `hashCode()`** — otherwise HashMap breaks (object goes into one bucket on put, looked up in a different bucket on get)

### internal implementation


### thread safety

HashMap is **not** thread safe. 

1. It can throw `ConcurrentModificationException` when two threads access the same HashMap.
2. When multiple threads will modify the same HashMap (e.g. will do resizing) it can lead to data corruption or infinite loops during iteration.

In multithread environment use [[ConcurrentHashMap]] instead. (There is also Hashtable but it's old and ConcurrentHashMap is better)

### worth remembering

- Allows one null key and null values


### time complexity

| Operation                  | Time Complexity | Space Complexity |
| -------------------------- | --------------- | ---------------- |
| Adding/removing/extracting | O(1)            | O(N)             |

### related

[[Java]], [[ConcurrentHashMap]]
### missing

buckets
hashing function
interview questions