Type of [[consistency model]].

Applies to both concurrent programming (see [[multithreading]]) and [[distributed system|distributed systems]].

# distributed systems

It specifies how distributed system should behave in environment with concurrent operations (e.g. multiple users). System is linear when it behaves as if there was single source of data. Each operation apply to data atomically.

>[!quote] 
>Linearizability provides the illusion that each operation applied by concurrent processes takes effect instantaneously at some point between its invocation and its response.

### registers

Linearizability applies to *single-object*.

Register in the context of distributed system is a key value pair.
### serializability vs linearizability

Not to confuse with [[serializability]]. Both are consistency models but:

- **serializability** is a multi-object property - guarantees that operations on objects and it's subparts happen atomically;
- linearizability is single-object property;

### resources

[linearizability in distributed systems - article](https://eli.thegreenplace.net/2024/linearizability-in-distributed-systems/)

# multithreading

TODO