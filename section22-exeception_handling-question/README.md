# Exception Handling 1 ~ 3

### 1) What is an Exception? What is Exception Handling?

**Answer:**

- Exception is a **Runtime Error.**
- The process of Handling the runtime errors is known as **Exception Handling.**
- Use **do**, **try**, **catch**, **throw** and **throws** to achieve exception handling.

### 2) What are the advantages of exception handling?

**Answer:**

- Exception Handling is helpful to co-workers of a team to indicate that there is some **dangerous code, “**please be cautious while using that piece of code”.

### 3) What is defer keyword?

**Answer:**

- A block of code which gets executed just before the execution control comes out of that method.

```swift
struct AnyStruct {

	func method() {
			defer {
					print("This is the last statement which gets executed")
			}

			print("Run first")
			print("Run second")
			print("Run third")
	}

}

let executor: AnyStruct = AnyStruct()
executor.method()
// Run first
// Run second
// Run third
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

[Section 14, access specifier](/section14-access-specifier/README.md)

[Section 15, higher order function](/section15-higher_order_fuctions/README.md)

[Section 16, delegate](/section16-delegate/README.md)

[Section 17, extension](/section17-extension/README.md)

[Section 18, Memory Management](/section18-memory_management/README.md)

[Section 19, protocols](/section19-protocols/README.md)

[Section 20, collections](/section20-collections/README.md)

[Section 21, KVO and KVC](/section21-kvo_kvc-question/README.md)

Section 22, Exception Handling

[Section 23, Framework](/section23-framework-question/README.md)

[Section 24, Objective-C](/section24-objective_c-question/README.md)