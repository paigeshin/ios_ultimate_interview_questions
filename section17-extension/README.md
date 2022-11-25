# Extension 1 ~ 6

### 1) What is extension?

**Answer:**

- Way of adding new functionality without subclassing is known as Extension.

```swift
class A {

	func aFunc() {

	}

}

extension A {

  func bFunc() {

	}

}

let a: A = A()
a.aFunc()
a.bFunc()
```

### 2) What is the difference between Subclassing (Inheritance) and Extension?

**Answer:**

- No overriding in extension
- No stored properties in extension (with computed property though, you can)
- Newly added functionality is available to all instances of that class

```swift
class A {

	func aFunc() {

	}

}

extension A {

  func bFunc() {

	}

}

let a: A = A()
a.aFunc()
a.bFunc()
```

### 3) Can we use stored property in extension?

**Answer:**

- No

```swift
class A {

}

// Error
extension A {
	var b: Int = 3
}
```

### 4) Can we use computed property in extension?

**Answer:**

- Yes, you can declare property with get set

```swift
class A {

}

extension A {
	var b: Int {
		get {
			return 3
		}
	}
}
```

### 5) Can we override existing methods using Extension?

**Answer:**

- No, overriding the existing functionality is not allowed in Extension.

### 6) When to choose Extensions over inheritance?

**Answer:**

- Go for extension when you want to add new functionality that should be available for all instances of that class.
- Go for subclassing when you want to extend the functionality of a class and that should be available for only newly created class. When you want to override the functionality of a class, go for subclassing.

# Table Of Contents

[Section 1, Data Type](./section1-datatypes/)

[Section 2, Operator](./section2-operator/)

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

Section 17, extension

[Section 18, Memory Management](./section18-memory_management/)

[Section 19, protocols](./section19-protocols/)

[Section 20, collections](./section20-collections/)

[Section 21, KVO and KVC](./section21-kvo_kvc-question/)

[Section 22, Exception Handling](./section22-exeception_handling-question/)

[Section 23, Framework](./section23-framework-question/)

[Section 24, Objective-C](./section24-objective_c-question/)