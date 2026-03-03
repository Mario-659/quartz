# [[Java]]

**Key Numbers**
- Default capacity: 16
- Default load factor: 0.75
- Resize trigger: when `size > capacity * loadFactor`, the array doubles and all entries are **rehashed**

### The `hashCode()` and `equals()` Contract

- If `a.equals(b)` is true → `a.hashCode() == b.hashCode()` **must** be true
- If hashCodes are equal, `equals()` **may or may not** be true (collision)
- **If you override `equals()`, you must override `hashCode()`** — otherwise HashMap breaks (object goes into one bucket on put, looked up in a different bucket on get)




buckets
hashing function

### time complexity

| Operation                  | Time Complexity | Space Complexity |
| -------------------------- | --------------- | ---------------- |
| Adding/removing/extracting | O(1)            | O(N)             |