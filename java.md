# Java coding convention

## Maps names

There are 2 popular nameing conventions for maps:
- keysToValues
- valuesByKeys 

The first is more like showing an action, and the second is showing a noun. So the second aproach is preferable.

**Example**: If the map contains 'userId' as key and 'room number' as value the map should be
named as 'roomNumbersByUserIds':

```java
Map<String, Integer> roomNumbersByUserIds = Map.of(
    "001", 100,
    "003", 213,
    "a12", 507 
)
```

