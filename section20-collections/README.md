# Collections 1 ~ 4

### 1) What are the collections available in Swift?

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

### 2) What is the difference between Array and Set?

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

### 3) What is the difference between Tuple vs Dictionary?

**Answer:**

- Tuples are mainly used to return multiple values from a method.
- Dictionaries are mainly to store the data in the form of key value pairs.
- Tuples can optionally have keys.
- Dictionary contains keys.
- Tuple contains pre-defined number of values.
- Dictionary has no limitation on storing key-value pairs.
- Tuple has no methods to perform operations.
- Dictionary has set of methods to perform operations.

### 4) Is String, Array, Dictionary and Set are Classes or Structures?

**Answer:**

- String, Array, Dictionary and Set are Structures. Those are value types.

# Table Of Contents

[Section 1, Data Type](/section1-datatypes/README.md)

[Section 2, Operator](/section2-operator/README.md)

[Section 3, Conditional Statement](/section3-conditional-statement/README.md)

[Section 4, Enum](/section4-enum/README.md)

[Section 5, functions](/section5-function/README.md)

[Section 6, struct](/section6-struct/README.md)

[Section 7, initializers](/section7-initializers/README.md)

[Section 8, closures](/section8-closures/README.md)

[Section 9, OOP](/section9-oop/README.md)

[Section 10, static type vs dynamic type](/section10-static_dynamic_type_difference/README.md)

[Section 11, optional](/section11-optional/README.md)

[Section 12, generic](/section12-generic/README.md)

[Section 13, subscript](/section13-subscript/README.md)

[Section 14, access specifier](/section14-access-specifier/README.md)

[Section 15, higher order function](/section15-higher_order_fuctions/README.md)

[Section 16, delegate](/section16-delegate/README.md)

[Section 17, extension](/section17-extension/README.md)

[Section 18, Memory Management](/section18-memory_management/README.md)

[Section 19, protocols](/section19-protocols/README.md)

Section 20, collections

[Section 21, KVO and KVC](/section21-kvo_kvc-question/README.md)

[Section 22, Exception Handling](/section22-exeception_handling-question/README.md)

[Section 23, Framework](/section23-framework-question/README.md)

[Section 24, Objective-C](/section24-objective_c-question/README.md)