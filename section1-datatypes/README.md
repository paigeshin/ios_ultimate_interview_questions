# Data Type Questions 1 ~ 13

### 1) What is Datatype? list out a few data types in Swift

**Answer**

- Datatype is a keyword which specifies to compiler that what kind of value the declared identifier can store.

- Swift Data Types

```swift
// Int
var age: Int = 365
// Float
var weight: Float = 78.50
// Double
var carWeight: Double = 123532524.5423
// Character
var initial: Character = "A"

// String
let name: String = "Paige"
// Bool
let isProfessional: Bool = true
// Array
let evenNumbers: Array = [2, 4, 6, 8, 10, 12, 14, 16]
// Array of Int
let oddNumbers: [Int] = [1, 3, 5, 7, 9, 11]
// Set
let uniqueValues: Set = [1, 2, 3, 4, 5, 6, 7, 8]
// Set of Int
let uniqueValues2: Set<Int> = [1, 2, 3, 4, 5, 6, 7, 8]
// Dicionary
let address: Dictionary = [
    "Name": "Paige",
    "City": "Seoul"
]
// Dictionary with [String: Any] Specified
let instructor: [String: Any] = [
    "Name": "Paige",
    "Age": 31,
    "Number": 000000000
]
// Any can contain literally anything
let any: Any = 10.19
```

### 2) let vs var? Constant vs Variable?

**Answer**

- Value assigned to constant can not be modified. Use let to declare a constant.

- Value assigned to variable can be modified. Use var to declare variable.

```swift
let imConstant: Int = 3

imConstant = 4 // Error
var imVariable: Int = 5
print(imVariable) // 5
imVariable = 6
print(imVariable) // 6
```

### 3) What is Type Inference?

**Answer**

- The process of compiler identifying the datatype of an identifier based on the value to that identifier.

```swift
var anyInt = 3 // compiler will identify `anyInt` as Int
var anyString = "test" // compiler will identify `anyString` as String
```

### 4) What is Type Annotation?

**Answer**

- Process of explicitly specifying the datatype of variable is known as Type Annotation.

```swift
var imExplicitlyInt: Int = 5
var imExplicitlyString: String = "string"
```

### 5) How Swift is Type Safe Language?

**Answer**

- Swift is Type Safe Language because it doesn't allow Implicit Type Casting.

- If you declare as Int and if you try to store Double , Swift doesn't allow.

```c
// In C Language, Implicit Type Casting is allowed

int num;

float Fnum = 123.953;

num = Fnum;

printf("%d\n", num); // returns 123.000. This is implicit type casting. In Swift, you cannot do that.
```

```swift
// In Swift, Implicit Type Casting is not allowed

// Note that this is not possible in the first place
var num: Int
var Fnum: Float = 123.953

num = Fnum // Error
// Correct Way
num = Int(Fnum)!

```

### 6) What is Type Casting? Give me an example?

**Answer**

- The process of converting one datatype value into another datatype value is known as Typecasting.

```swift
// Double to Int
var weight: Int = 0

var killograms: Double = 84.8

weight = Int(killograms)

```

### 7) Does Swift support Implicit Typecasting?

**Answer**

- No

### 8) What is Tuple? When do we use Tuple?

**Answer**

- Tuple is grouping multiple values together into a single variable. Use tuple when you want to return multiple values from a method.

```swift

// Tuple Case 1
let info: (String, String, Int) = ("Paige", "Seoul", 32)
print(info.0) // Paige
print(info.1) // Seoul
print(info.2) // 32
// Tuple Case 2 assigning multiple values - Practical Example
let (name, city, age) = ("Paige", "Seoul", 32)
print(name) // Paige
print(city) // Seoul
print(age) // 32
// Tuple Case 3 key-value, - Practical Example
let infomration: (name: String, city: String, age: Int) = (name: "Paige", city: "Seoul", age: 32)
print(infomration.name) // Paige
print(infomration.city) // Seoul
print(infomration.age) // 32
```

### 9) What is String Interpolation?

**Answer**

- Process of Embedding values inside the String Object is known as String Interpolation.

```swift
let name: String = "Paige"
let age: Int = 32

print("Hello, My name is \(name) and I'm \(age) years old")
// Hello, My name is Paige and I'm 32 years old
```

### 10) What is Type Aliasing?

**Answer**

- Process of Assigning another name to an existing datatype is known as Type Aliasing.

```swift
ypealias Number = Int

let age: Number = 34

if age is Int {
    print("age is obviously int!")
}
// age is obviously int!
```

### 11) Can we use existing keyword as an identifier (variable)?

**Answer**

- By using single tick "`" marks

```swift
let `let`: Int = 40
print(`let`) = 40
```

### 12) "C", is this Character?

**Answer**

- By default, all characters are Strings. Use Type Annotation to consider it as Character.

```swift
// Type is 'String'
let initial = "C"

// Type is 'Character'
let initial: Character = "C"
```

### 13) 10.0 is float?

**Answer**

- By default, all floating point values are doubles. Use Type Annoation to consider it as Float.

```swift
// Type is 'Double' by default
let distance = 10.0

// Type is 'Float' with Type Annotation
let distance: Float = 10.0
```
# Table Of Contents

Section 1, Data Type

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

[Section 20, collections](/section20-collections/README.md)

[Section 21, KVO and KVC](/section21-kvo_kvc-question/README.md)

[Section 22, Exception Handling](/section22-exeception_handling-question/README.md)

[Section 23, Framework](/section23-framework-question/README.md)

[Section 24, Objective-C](/section24-objective_c-question/README.md)
