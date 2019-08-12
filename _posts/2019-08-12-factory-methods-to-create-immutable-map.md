# Factory methods to create Immutable Map

### Creating Immutable Map prior to Java 9
###### Create Empty Map
We used to use the unmodifiableMap() method of Collections class to create unmodifiable(immutable) Map

```
Map<String, String> map = new HashMap<String, String>();
Map<String, String> immutableMap = Collections.unmodifiableMap(map)
```

###### Creating Non Empty Map

```
Map <String, String> map = new HashMap<String, String>();
map.put("keyone", "truong");
map.put("keytwo", "dam");
```
Map <String, String> immutableMap = Collections.unmodifiableMap(map);

### Java 9 Factory Methods to create immutable Map
###### Create Empty Map
```
Map<String, String> immutableMap = Map.of();
```
###### Creating Non Empty Map
```
Map<String, String> immutableMap = Map.of("keyone", "truong", "keytwo", "dam");
```
immutableMap ==> {keyone=truong, keytwo=dam}

### What is an immutable Map?
- Immutable Map doesn’t allow addition, deletion and update of its elements. If you try to perform these operations then the program will throw `UnsupportedOperationException`.

```
jshell> Map<String, String> immutableMap =
Map.of("Key1", "truong", "Key2", "dam")
immutableMap ==> {Key1=truong, Key2=dam}

jshell> immutableMap.put("Key3", "hello");
| java.lang.UnsupportedOperationException thrown:
| at ImmutableCollections.uoe (ImmutableCollections.java:71)
| at ImmutableCollections$AbstractImmutableMap.put
(ImmutableCollections.java:558)
| at (#2:1)
```

- They do not allow null elements. Adding null elements will throw the same `UnsupportedOperationException`.
