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

# Table Of Contents

[Section 1, Data Type](./section1-datatypes/)

[Section 2, Operator](./section2-operator/)

[Section 3, Conditional Statement](./section3-conditional-statement/)

[Section 4, Enum](./section4-enum/)

[Section 5, functions](./section5-function/)

[Section 6, struct](./section6-struct/)

[Section 7, initializers](./section7-initializers/)

[Section 8, closures](./section8-closures/)

[Section 9, OOP](./section9-oop/)

[Section 10, static type vs dynamic type](./section10-static_dynamic_type_difference/)

[Section 11, optional](./section11-optional/)

[Section 12, generic](./section12-generic/)

[Section 13, subscript](./section13-subscript/)

[Section 14, access specifier](./section14-access-specifier/)

Section 15, higher order function

[Section 16, delegate](./section16-delegate/)

[Section 17, extension](./section17-extension/)

[Section 18, Memory Management](./section18-memory_management/)

[Section 19, protocols](./section19-protocols/)

[Section 20, collections](./section20-collections/)

[Section 21, KVO and KVC](./section21-kvo_kvc-question/)

[Section 22, Exception Handling](./section22-exeception_handling-question/)

[Section 23, Framework](./section23-framework-question/)

[Section 24, Objective-C](./section24-objective_c-question/)