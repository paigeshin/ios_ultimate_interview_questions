# struct questions 1 ~ 3

### 1) What is struct? How to declare a structure?

**Answer:**

- `struct` is a keyword used to create User Defined Datatype.

```swift
struct Car {

	let model: Int = 2023

	func start() {
		print("Starting")
  }

	func stop() {
		print("Stopping")
	}

}

let car: Car = Car()
car.start()
car.stop()
```

### 2) What is mutating keyword in Swift?

**Answer:**

- mutating is a keyword which allows to modify structure variable inside the structure’s method

```swift
struct Car {

	let model: Int = 2023
	var speed: Int = 0

	func start() {
		print("Starting")
  }

	func stop() {
		print("Stopping")
	}

	// If you don't put `mutating` keyword inside a method which modifies
	// struct's properties, compiliation error will occur
	mutating func speedUp(newSpeed: Int) {
		speed = newSpeed
	}

}

let car: Car = Car()
print(car.speed) // 0
car.speedUp(newSpeed: 5)
print(car.speed) // 5
```

### 3) Is struct Value type or Reference Type?

- Structure is a value type. Structure values are copied when you pass then to a method.

**#Info**

- Value Type creates new instances and assigned when they passed to a method or assigned
- Reference Type just shares the address of that Object when they are passed as arguments or assigned

# Table Of Contents

[Section 1, Data Type](/section1-datatypes/README.md)

[Section 2, Operator](/section2-operator/README.md)

[Section 3, Conditional Statement](/section3-conditional-statement/README.md)

[Section 4, Enum](/section4-enum/README.md)

[Section 5, functions](/section5-function/README.md)

Section 6, struct

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