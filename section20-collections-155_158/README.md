# Collections 155 ~ 158

### 155) What are the collections available in Swift?

**Answer:**

- String
- Array
- Dictionary
- Set

```swift
/** All Collections are interable **/

let helloworld: String = "hello world"
for value in helloworld {
	print(value)
}

let arr: [Int] = [1, 2, 3, 4, 5]
for value in arr {
	print(value)
}

let setData: Set<Int> = [1, 2, 3, 4, 5]
for value in setData {
	print(value)
}

let dic: [String: Any] = [
	"key": "value",
	"key2": "value2"
]

for (key, value) in dic {
	print(key)
	print(value)
}
```

### 156) What is the difference between Array and Set?

**Answer:**

- Array is an ordered collection of similar or dissimilar values where Set is an unordered collection of similar values without duplicate elements.
- Array is an ordered collection
- Set is an unordered collection
- Set contains unique values

```swift
let arr: Array = [1, 1, 2, 2, 3, 3]
for i in arr {
    print(i) // 1, 1, 2, 2, 3, 3
}

let aSet: Set = [1, 1, 2, 2, 3, 3]
for i in aSet {
    print(i)
    // It's an unordered collection
    // all posibilities..
    // 2, 3, 1
    // 1, 2, 3
    // 3, 2, 1
    // 1, 3, 2
}
```

### 157) What is the difference between Tuple vs Dictionary?

**Answer:**

- Tuples are mainly used to return multiple values from a method.
- Dictionaries are mainly to store the data in the form of key value pairs.
- Tuples can optionally have keys.
- Dictionary contains keys.
- Tuple contains pre-defined number of values.
- Dictionary has no limitation on storing key-value pairs.
- Tuple has no methods to perform operations.
- Dictionary has set of methods to perform operations.

### 158) Is String, Array, Dictionary and Set are Classes or Structures?

**Answer:**

- String, Array, Dictionary and Set are Structures. Those are value types.
