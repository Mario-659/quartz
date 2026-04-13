
Also known as *Hollywood Principle* - "don't call us, we will call you". It means that framework manages application's lifecycle and calls custom code when necessary.

Most commonly realized by Dependency Injection.

Used in [[object oriented programming]].

## IoC Container

In [[Spring Framework]] 
### bottom up approach

In Spring instead of creating object on the premise Object X need Object Y (top down) the objects are created from the lowest level (e.g. DataSource). Spring makes a dependency graph and starts with leaves. See [[DAG]] to see how it can be implemented

Spring in the beginning makes a directed graph (who needs whom). Also this way it can detect cycles (A -> B, b -> A)


