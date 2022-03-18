# Enum Questions 23 ~ 28

### 23) What is Enum?

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

### 24) What is rawValue in enum?

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

### 25) What is Associated values in Swift?

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

### 26) Is enum `value type` or `reference type`?

**Answer:**

- Enum is **Value Type**

### 27) Value Type vs Reference Type

**Answer:**

- Value type creates new instances and assigned when they passed to a method or assigned.
- Reference type just shares address of that Object when they are passed as arguments or assigned.

### 28) What is the difference between Swift Enum and Objective-C Enum?

**Answer:**

- Obj-c enums doesn’t allow Raw and Associated Values
