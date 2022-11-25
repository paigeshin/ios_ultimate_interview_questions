# Access Specifier 1 ~ 5

### 1) What is Access Specifier? What are the access specifiers available in Swift?

**Answer:**

- Access Specifiers are the way to specify the availability scope of Variables and Methods.
- final
- public
- private
- fileprivate
- open
- internal

### 2) What is the default Access Specifier in Swift?

**Answer:**

- Internal

### 3) private vs fileprivate access specifier?

**Answer:**

- **private** variables are accessible only within the class.
- **fileprivate** is accessible in the entire file. Mainly useful for extensions.

```swift
class A {

	private var aPrivateVar: Int = 10

	fileprivate var aFilePrivateVar: Int = 20

	func aMethod() {
	    // private can be accessed within the same class
			print(aPrivateVar)
	}

}

class B: A {

	func bMethod() {
			// print(aPrivateVar) // Error!
			print(aFilePrivateVar) // You can access fileprivate
	}

}
```

### 4) public vs open

**Answer:**

- Public method or variable can be accessible anywhere but **public class defined in another module can’t be extended.**
- Open method or variable can be accessible anywhere but **open class defined in another module can be extended.**
- An `open` class is *accessible* and *subclassable* outside of the defining module.
- An `open` class member is *accessible* and *overridable* outside of the defining module.
- A `public` class is *accessible* but *not subclassable* outside of the defining module.
- A `public` class member is *accessible* but *not overridable* outside of the defining module.

### 5) What is final keyword?

**Answer:**

- A class defined as a final can’t be inherited but extended.

```swift
final class A {

}

// Error
class B: A {

}
```

# Table Of Contents

[Section 1, Data Type](/section1-datatypes/README.md)

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

Section 14, access specifier

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