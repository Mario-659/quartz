
A function is idempotent when applied multiple times to the same value will not change the outcome.

### mathematics

Absolute value is idempotent.


```
|a| = ||a||
```

Function that flips a sign is not idempotent.

```
a(x)  = -x
a(x) != a(a(x))
```
### software development

Let's say user A wants to send 10$ to user B. Service Y is in the middle. Consider following:

```
            User A             Service Y            User B

1st try     Send 10$  --->        |
                                Error
                                  |
           <--- Error msg ----    |
-------           

1st retry   Send 10$ --->         |
                                  | --- Send 10$ -->   | Money received
                                  |                    |
                                  |  <-- Confirmation  |
             Confirmation failed  |
-------            
2nd retry   Send 10$ --->         |
                                  | --- Send 10$ -->   | Money received
                                  |                    |
                                  |  <-- Confirmation  |
           <--- Confirmation ---  |
```

Behavior above is not idempotent because the intended action is to send the 10$ once. If the system were idempotent at 2nd retry  Service Y would return Confirmation without sending the money to User B.

[baeldung](https://www.baeldung.com/cs/idempotent-operations)