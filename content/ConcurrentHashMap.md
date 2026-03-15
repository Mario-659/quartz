
```
ConcurrentHashMap<String, String> concurrentMap = new ConcurrentHashMap<>();
```

## how it works internally

It is implemented similarly as [[HashMap]] and it achieves thread safety by dividing hash map into segments which are locked during write operations.
## hash map vs concurrent hash map

**Null keys and values** -- while HashMap allows one null key and multiple null values the ConcurrentHashMap does not allow neither of them, because it's considered as anti pattern (when `get(foo)` returns null would it mean that there is no such key or there is key `foo` with value null?). 

See [Why ConcurrentHashMap does not support null values - reddit](https://www.reddit.com/r/java/comments/ojc7w/why_concurrenthashmap_does_not_support_null_values/)

## interview questions

[11 Java ConcurrentHashMap Interview Questions Answers - blog](https://javarevisited.blogspot.com/2017/08/top-10-java-concurrenthashmap-interview.html)

## related

[[multithreading]]; [[HashMap]]; [[Java]]