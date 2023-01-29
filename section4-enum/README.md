# Enum Questions 1 ~ 6

### 1) What is Enum?

**Answer:**

- enum is a keyword used to declare User defined datatype with user defined values.

```swift
enum WeekDay {
	case monday
	case tuesday, wednesday
	case thursday
	case friday
	case saturday
	case sunday
}

var weekDay: WeekDay = .monday
weekDay = .saturday

```

### 2) What is rawValue in enum?

**Answer:**

- Value assigned to the enum cases. By default every enum case assigned by an int value start from 0.
- We can also change the enum case values by explicitly specifying the Type.

```swift
enum WeekDay: String {
	case monday = "Mon"
	case tuesday = "Tue"
	case wednesday = "Wed"
	case thursday = "Thu"
	case friday = "Fri"
	case saturday = "Sat"
	case sunday = "Sun"
}

let weekDay: WeekDay = .monday
print(weekDay.rawValue) // Mon
print(WeekDay.sunday.rawValue) // Sun
```

### 3) What is Associated values in Swift?

**Answer:**

- Enum cases which are capable of holding some values are called associated values.

```swift
enum Month {
	case GeneralMonth
	case ExtraDaysMonth(days: Int)
}

// Associated Values
let january: Month = .ExtraDaysMonth(days: 31)

switch january {
	case .GeneralMonth:
		print("It is regular month")
	case .ExtraDaysMonth(let days):
		print("It has \(days) day")
}
```

```swift
// Practical Usecases
enum Error {
	case NetworkError
	case UnknownError(code: Int, message: String)
}
```

### 4) Is enum `value type` or `reference type`?

**Answer:**

- Enum is **Value Type**

### 5) Value Type vs Reference Type

**Answer:**

- Value type creates new instances and assigned when they passed to a method or assigned.
- Reference type just shares address of that Object when they are passed as arguments or assigned.

### 6) What is the difference between Swift Enum and Objective-C Enum?

**Answer:**

- Obj-c enums doesn’t allow Raw and Associated Values

# Table Of Contents

[Section 1, Data Type](/section1-datatypes/README.md)

[Section 2, Operator](/section2-operator/README.md)

[Section 3, Conditional Statement](/section3-conditional-statement/README.md)

Section 4, Enum

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