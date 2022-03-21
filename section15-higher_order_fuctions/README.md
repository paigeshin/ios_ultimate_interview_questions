# Higher Order Functions 1 ~ 6

### 1) What are the higher order functions available in Swift?

**“Super Quick”**

**Answer:**

- Filter
- Map
- FlatMap
- CompactMap
- Reduce

### 2) What is Filter and How does it work?

**Answer:**

- Filter works on collections to filter out the elements of Collection based on some criteria.

```swift
let array: [Int] = [1, 2, 3, 4, 5, 6, 7, 8, 9]

// var evenArr: [Int] = array.filter { value -> Bool in
// 		value % 2 == 0
// }

var evenArr: [Int] = array.filter { $0 % 2 == 0 }
print(eventArr) // 2, 4, 6, 8
```

### 3) What is map and how does it work?

**Answer:**

- Map works on the collection to apply an operation on all elements of a collection.

```swift
let array: [Int] = [1, 2, 3, 4, 5, 6, 7, 8, 9]

//var mappedArray: [Int] = array.map { value -> Int in
//	value * 2
//}

var mappedArray: [Int] = arrap.map { value * 2 }

print(mappedArray) // 2, 4, 6, 8, 10, 12, 14, 16, 18
```

### 4) What is reduce and how does it work?

**Answer:**

- Reduce works on the Collection to prepare a single value from the collection of values.

```swift
let array: [Int] = [1, 2, 3, 4, 5, 6, 7, 8, 9]
var result: Int = 0

result = array.reduce(result) { partialResult, value in
    partialResult + value
}

print(result) // 45
```

### 5) What is flatmap in Swift?

**Answer:**

- Flat map extracts the Collection of collections into a collection.
- [ **[1, 2, 3]**, **[4, 5, 6]** ].flatmap ⇒ [1, 2, 3, 4, 5, 6]

```swift
let array: [[Int]] = [[1, 2, 3], [4, 5], [6, 7], [8]]
let flatMappedArr: [Int] = array.flatMap { $0 }
print(flatMappedArr) // 1, 2, 3, 4, 5, 6, 7, 8
```

### 6) What is Compact Map in Swift?

**Answer:**

- Compact Map removes all nils from the collection.

```swift
let array: [Int?] = [0, 1, 2, 3, 4, nil, nil, 7, 8, nil]
let compactMappedArr: [Int] = array.compactMap { $0 }
print(compactMappedArr) // 0, 1, 2, 3, 4, 7, 8
```
