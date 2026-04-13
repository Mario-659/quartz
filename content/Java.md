
### missing

- Collections
- versions / differences between them
- equals and hashvalue (how to override)
- Comparable interface

## collections

#### PriorityQueue

**Use case**: when we want to get top (max or min) value

- internally uses binary heap;
- `peek()` get top element;
- `poll()` get and remove top element - *O(log n)* as it re-heapifies;
- `offer()` put new element
- does not guarantee other elements are sorted;
