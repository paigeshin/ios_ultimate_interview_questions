# Operator Questions 1 ~ 3

### 1) What are the operators available in Swift?

**Answer**

`Operators`

- Arithmetic Operators (+,-,\*,/,%)
- Logical Operators (<,>,<=,>=,!=,==)
- Conditional Operator (?:)
- Compound Operators (+=, -=, \*=, /=, %=)
- Nil-Coalescing Operator (??)
- Type Checking Operator (is)
- Type Considering Operator (as!, as?)
- Identity Operators (===, !==)

`Range Operators`

- Closed Range (1...10)
- Half Opened Range (1..<10)
- One Sided Range Operators (2..)

### 2) Can you explain different range operators in Swift?

**Answer**

```swift
let n: Int = 3

// Closed Range
for i in 0...n {
  print(i) // 0, 1, 2, 3
}

// Half Opened Range
for i in 0..<n {
  print(i) // 0, 1, 2
}

// One Sided Range Operators
let numbers: [Int] = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
for value in numbers[5...] {
  print(value) // 5, 6, 7, 8, 9, 10
}
```

### 3) What is identity operator in Swift?

**Answer**

- === and !== are the identity Operators in Swift. This is only used for Object Types. In other words, it's not used for Value Types.

```swift
class A {

}

let a1: A = A()
let a2: A = A()
let a3: A = a2

print(a1 === a2) // false
print(a2 === a3) // true, referencing the same memory
```

# Table Of Contents

[Section 1, Data Type](./section1-datatypes/)

Section 2, Operator

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

[Section 15, higher order function](./section15-higher_order_fuctions/)

[Section 16, delegate](./section16-delegate/)

[Section 17, extension](./section17-extension/)

[Section 18, Memory Management](./section18-memory_management/)

[Section 19, protocols](./section19-protocols/)

[Section 20, collections](./section20-collections/)

[Section 21, KVO and KVC](./section21-kvo_kvc-question/)

[Section 22, Exception Handling](./section22-exeception_handling-question/)

[Section 23, Framework](./section23-framework-question/)

[Section 24, Objective-C](./section24-objective_c-question/)
