
It says that while designing [[distributed system]] out of three properties:
- Availability - response is sent for every read request
- Consistency - data is consistent across nodes
- Network Partition - system is reliable upon network partition between nodes

we can have only *2 out of 3*.

## example scenario

In the following scenario:

```js
1. User A ---write---> Node A
2. User B ---read ---> Node B
```

we can have a system that is:

a) AP - Available and Network Partition resistant. User B will get a response but the data he will receive will not be consistent with User A write request.
b) CP - Consistent and Network Partition resistant. User B will not get response which will make the data consistent across the system.

## reality

The original theorem is based on abstract model. In reality there we must always design a system that is network partition resilient.

In real life scenario we are not choosing *on/off* for these properties - we are fine tuning them. CAP theorem is based on abstract model. In reality distributed systems use variety of techniques to minimize compromises (quorium).

## PACELC



## availability vs consistency

[[ACID]] philosophy:
- traditional approach
- consistency over availability

[[BASE]] philosophy:
- availability over consistency

## Related

[[linearizability]]



# 1st from memory
12-02-2026 18:30

CAP applies to distributed systems. It says that out of three properties:
- Availability - response is sent for every read request
- Consistency - data is consistent across nodes
- Network Partition - system is reliable upon network partition between nodes

We can have only 2 out of three. For example in scenario below:
```js
1. User A ---write---> Node A
2. User B ---read ---> Node B
```

We can have either:
a) AP - User B gets response (system is available) but the data is not consistent with write request of User A
b) CP - User B doesn't get response (system is not available) but the data remains consistent

We need to make compromises based on domain of the project. In financial systems consistency is more important that availability, while for social media platform availability is more important that consistency.

In real life scenario we are not choosing *on/off* for these properties - we are fine tuning them. CAP theorem is based on abstract model. In reality distributed systems use variety of techniques to minimize compromises (quorks).

## What did I miss
Formal definitions:
1. linearizability
2. total availability

quorum - not qorks.
PACELC

P is unavoidable.

Latency assigned to availability.