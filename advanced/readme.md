## Hashable objects
Hashing is a mechanism to convert large chunk of data into smaller amount(typically a single integer) in a repeatable way so that it can be looked up in a table in constant time O(1) time complexity.

When we call hash() on the object, it should not return error.

```
>>> hash(100)
100
>>> hash("prateek")
-6598330506749444061
>>> hash([1,2])
TypeError: unhashable type: 'list'
```
