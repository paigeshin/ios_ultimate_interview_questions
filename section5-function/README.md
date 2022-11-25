# Functions 1 ~ 7

### 1) What is function? What is the difference between function and Method?

**Answer:**

- Function / Method is a block of statements which performs some specific task.
- Function is global whereas Method is associated with a `Class` and `Structure`.

```swift
// Global Scope
// Function Example
func function() {
	print("I'm a Function")
}

function()

// Method
class Car {
	func method() {
		print("I'm a Method beloing to `Car`")
	}
}

let car: Car = Car(
car.method()
```

### 2) What is `inout` parameter in Swift?

- The input arguments of a method by default are `let` constants. To **change the value of input arguments the input keyword helps.**
- To **pass the references** of the arguments to a method we use inout keyword.

```swift
// Without `inout`
class Car {

	func refuel(input: Double) {
		input += 10 // Error, because `input` here is `Constant`
	}

}
```

```swift
// With `inout`
class Car {

	func refuel(input: inout Double) {
		input += 10 // It works!
	}

}

// parameter with `&`
let car: Car = Car()
let baseValue: Double = 20.0
car.refuel(input: &baseValue)
```

### 3) Instance method vs Type Method?

- Methods are two types: **Instance** methods and **Type** Methods.
- **Instance methods** are tied up with the instance of a class. So access instance methods using object.
- **Type methods** are tied up with classes. Use ClassName. TypeMethod.
- Use **static / class** to declare **Type Methods**

```swift
class SomeClass {

	class func typeMethod() {
		print("This is TypeMethod")
	}

	static func staticMethod() {
		print("Another type of TypeMethod")
	}

	func method() {
		print("This is method")
	}

}

let someClass: SomeClass = SomeClass()

// call method
someClass.method()

// call type method
someClass.typeMethod()
someClass.staticMethod()
```

### 4) What is the difference between `class func` and `static func` ?

**Answer:**

- **class function — can be overridden,** but **static func cannot be overridden**

```swift
class MyClass {

// Instance Method
func instanceMethod() {}

// Class Type Method
class func classTypeMethod() {}

// Static Type Method
static func staticTypeMthod() {}

}

// Common
MyClass.classTypeMethod()
MyClass.staticTypeMethod()

// Difference
class SubMyClass: MyClass {

	// Good!
	override class func classTypeMethod() {}

	// Compile Error
	override static func staticTypeMthod() {}

}
```

**#Tips**

- if you use `class type method` with `final` keyword, there is no difference using `static type method`.

### 5) What is variadic number of params method?

**Answer:**

- A method which accepts **dynamic number of input arguments** is known as variadic params method.

```swift
class MyClass {

	func variadicMethod(numbers: Int...) {
		print(numbers)
	}

}

let myClass: MyClass = MyClass()
myClass.variadicMethod(numbers: 1)
myClass.variadicMethod(numbers: 1, 2)
myClass.variadicMethod(numbers: 1, 2, 3)
```

### 6) How to set default value to a method input arguments?

**Answer:**

- func myName(firstName: String, lastName=”Shin”)

```swift
class MyClass {

	func defaultValueMethod(a: Int, b: Int = 10) {
		print("a: \(a)")
		print("b: \(b)")
	}

}

let myClass: MyClass = MyClass()
myClass.defaultValueMethod(a: 10) // a: 10, b: 10
myClass.defaultValueMethod(a: 5, b: 3) // a: 5, b: 3
```

### 7) Is Swift Function `Value Type` or `Reference Type` ?

**Answer:**

- It’s Reference Type

# Table Of Contents

[Section 1, Data Type](./section1-datatypes/)

[Section 2, Operator](./section2-operator/)

[Section 3, Conditional Statement](./section3-conditional-statement/)

[Section 4, Enum](./section4-enum/)

Section 5, functions

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
