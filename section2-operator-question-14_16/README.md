# Operator Questions 14 ~ 16

### Question 14 - What are the operators available in Swift?

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

---

### Question 15 - Can you explain different range operators in Swift?

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

---

### Question 16 - What is identity operator in Swift?

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

---
