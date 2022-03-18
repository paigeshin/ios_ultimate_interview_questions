# Functions 29 ~ 35

### 29) What is function? What is the difference between function and Method?

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

### 30) What is `inout` parameter in Swift?

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

### 31) Instance method vs Type Method?

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

### 32) What is the difference between `class func` and `static func` ?

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

### 33) What is variadic number of params method?

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

### 34) How to set default value to a method input arguments?

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

### 35) Is Swift Function `Value Type` or `Reference Type` ?

**Answer:**

- It’s Reference Type
