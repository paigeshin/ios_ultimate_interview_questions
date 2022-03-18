# Increase your salary dramatically by preparing for a job interview smartly

- If you are a beginner level swift developer, you are lucky to have found this repository. Not only should you learn fundamentals of Swfit Langauge, you can also prepare for your job interview

- If you are an intermediate and an advanced swift developer, make sure you know all these questions and try to answer it instantly without answers.

## Data Type Questions

### Question 1 - What is Datatype? list out a few data types in Swift

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

### Question 2 - let vs var? Constant vs Variable?

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

### Question 3 - What is Type Inference?

- The process of compiler identifying the datatype of an identifier based on the value to that identifier.

```swift
var anyInt = 3 // compiler will identify `anyInt` as Int
var anyString = "test" // compiler will identify `anyString` as String
```

### Question 4 - What is Type Annotation?

- Process of explicitly specifying the datatype of variable is known as Type Annotation.

```swift
var imExplicitlyInt: Int = 5
var imExplicitlyString: String = "string"
```

### Question 5 - How Swift is Type Safe Language?

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

### Question 6 - What is Type Casting? Give me an example?

- The process of converting one datatype value into another datatype value is known as Typecasting.

```swift
// Double to Int
var weight: Int = 0

var killograms: Double = 84.8

weight = Int(killograms)

```

### Question 7 - Does Swift support Implicit Typecasting?

- No
