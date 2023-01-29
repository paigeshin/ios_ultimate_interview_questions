# Operator Questions 1 ~ 6

### 1) What are the conditional statements available in Swift?

**Answer**

- if
- if-else
- if-else ladder
- switch

```swift
let isAlien: Bool = true

// if
if isAlien {
  print("Alien")
}

// if - else
if isAlien {
  print("Alien")
} else {
  print("Probably Human")
}

// if - else ladder
if isAlien {
  print("Alien")
} else if isAlien != true {
  print("Probably Human")
} else {
  print("What else?")
}

// switch
switch isAlien {
  case true:
    print("Alien")
  case false:
    print("Probably Human")
}
```

### 2) What is fast enumeration in Swift?

**Answer**

- Process of iterating through all elements of a collection in an efficient way. It is faster than general for loop.

```swift
let numbers: [Int] = [1, 2, 3, 4, 5, 6, 7, 8, 9]
for number in numbers {
  print(number) //1, 2, 3, 4, 5, 6, 7, 8, 9
}
```

### 3) What is the difference between 'while' and 'repeat-while loops' in swift?

**Answer**

- While is `entry control` loop whereas do-while is `exit control` loop
- `entry control` loop versus `exit control` loop

```swift
// Enter Loop
var i: Int = 0

while i < 5 {
  print(i)
  i += 1
}

// Exit Loop
var j: Int = 0

repeat {
  print(i)
  i += 1
} while i < 5
```

### 4) What is switch case and how to declare a swift switch case?

**Answer**

- Switch is one of the conditional statements. It is an alternate to general if-else ladder statement.

```swift
let input: Int = 10

switch input {
  case 0:
    print("Value falls under 0")
  case 1...5:
    print("Value falles between 1 to 5")
  case 6,7,8,9:
    print("Value falls between 6 to 9")
  case 10:
    print("Value is 10")
  default:
    print("Not matched anywhere")
}
```

_Warning_

- You don't need to use break but you can use break keyword when you don't want to execute code.

_Professional Tips_

- Use switch when handling network status code.

### 5) Is default case necessary in Swift's Switch case?

**Answer**

- Default case is necessary in switch case, otherwise, you will see `Switch must be exhasutive` message.

### 6) What is Fall-through keyword in swift?

**Answer**

- Fall-through executes the next followed case irrespective of case matching. Place dependent case below the fall-through case

```swift
let input: Int = 15

switch input {
case 0:
    print("Value falls under 0")
case 11...15:
    print("Value falls between 11 to 15")
    fallthrough
case 9:
    #warning("This line will be executed when value is 11...15!!!")
    print("Value is 9 and this will be executed when value is between 11...15")
case 10:
    print("Value is 10")
default:
    break
}
```
# Table Of Contents

[Section 1, Data Type](/section1-datatypes/README.md)

[Section 2, Operator](/section2-operator/README.md)

Section 3, Conditional Statement

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