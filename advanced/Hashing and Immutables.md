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

## Immutable objects

Immutable objects are the type of objects that cannot be modified once they are created

```
>>> i = 100
>>> i+2
102
>>> i
100
```

## Immutable objects in Python
- Integer, Numerical types
- String
- Boolean
- Tuple

## Mutable objects in Python
- List
- Dict
- Sets

## Hashable Types in Python
- The atomic immutable types are all hashable, such as str, bytes, numeric types
- A frozen set is always hashable(its elements must be hashable by definition)
- A tuple is hashable only if all its elements are hashable
- User-defined types are hashable by default because their hash value is their id()

> [!Important]
> Although elements of sets are immutable, but set itself is mutable, that's why sets are not hashable
