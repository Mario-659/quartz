# note

ACID is a set of guarantees for database transactions

### Atomicity

Transactions are executed as a whole or not at all

### Consistency

Any transaction 

### Isolation

Each transaction is executed as if it was the only one even when there are multiple transactions. 
Isolation levels:

- Read Uncommitted
- Read Committed
- Repeatable Read
- Serializable

They prevent:

- Dirty read
- Non-repeatable read
- Phantom read

Every isolation level is a tradeoff between performance and correctness. 

#### Spring

In [[Spring Framework]] `@Transactional` annotation has an `isolation` attribute.

### Durability



### ACID vs BASE

RMBS DB's lean more towards [[ACID]] while NoSQL lean more towards [[BASE]]. According to [[CAP theorem]] you cannot have both.


### questions

# first active recall






