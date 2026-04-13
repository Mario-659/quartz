
# Note
### notions

- compensating transactions
- Choreography / Orchestration

### related

[[Spring Framework]], [[transactions]], [[distributed system]], [[idempotence]]

### resources

https://microservices.io/patterns/data/saga.html
[Saga Pattern in a Microservices Architecture - Bealdung](https://www.baeldung.com/orkes-conductor-saga-pattern-spring-boot)
[Microservices Pattern: Distributed Transactions (SAGA) - article](https://joudwawad.medium.com/microservices-pattern-distributed-transactions-saga-92b5e933cea1)



# Active recall

Saga pattern is used in distributed systems as a mechanism to execute transaction. Transaction meaning multiple actions that needs to be executed as one action.

Let's say we want to order food

```
Action 1       Action 2      Action 3                            Action  4

Order Food --> Update DB --> Send Notification To Restaurant --> Send Not. 2
```

In the scenario above there are multiple actions that are executed on different environments (e.g. Java API, DB, Message Broker). If one of the actions breaks we would want to revert to the initial state (e.g. redo changes in DB). Saga Pattern splits transaction into segments. Upon failure of one of the actions, for the failed action redo action is done as well as for all  of the previously executed actions.

*Score*: ~60-65%; missing:
- compensating transactions
- Choreography/Orchestration
- idempotent 
- eventual consistency instead of ACID
- comparison to 2PC/two-phase commit