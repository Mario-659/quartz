
A set of related operations that should be executed as single operation

```
			            -----  Microservice  -----
	Updates DB		  /			                   \  Produces Event
					 |                              | 
					 |                              |
	Transaction  ----------------------------------------
                     |                              |
                     |                              |
                    \/                             \/
                 Database                     Message Broker
```


- local transactions vs distributed transactions
- ACID, CAP, BASE
- two phase commit 2PC commit, three commit
- long lived distributed transactions

### local vs distributed transactions

### related

[[distributed system]]



