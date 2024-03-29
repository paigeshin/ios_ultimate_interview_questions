# Generics 1 ~ 4

### 1) What is Generic?

**Answer:**

- Generic is a feature of Swift which helps to write Generalized / Reusable datatypes and methods.
- Generic is a feature of Swift which helps to write generalized programming.
- A Datatype which is capable of holding different types of values. Generic Datatype is not specific to Particular Datatype Values.

### 2) What is Generic Method? What is Generic Type?

**Answer:**

- A method which is capable of performing operations on different datatype values.

```swift
/** Before Refacotoring, Stack can only contain 'Int' **/
class Stack {

	var collection: [Int] = []

	func push(item: Int) {
			collection.append(item)
	}

	func pop() {
			collection.removeLast()
  }

	func display() {
			print(collection)
	}

}

var intStack: Stack = Stack()
intStack.push(item: 10)
```

```swift
/** After Refactoring, Stack can hold multiple types **/
class Stack<T> {

	var collection: [T] = []

	func push(item: T) {
			collection.append(item)
	}

	func pop() {
			collection.removeLast()
  }

	func display() {
			print(collection)
	}

}

var intStack: Stack<Int> = Stack()
intStack.push(item: 10)

let stringStack: Stack<String> = Stack()
stringStack.push(item: "Hello")
```

### 3) What is the difference between Generic and Any?

**Answer:**

- **Generic** follows Swift’s Type Safety
- **Any** doesn’t follow type safety and you need to type check every time you perform an operation.

```swift
/** After Refactoring, Stack can hold multiple types **/
class Stack {

	var collection: [Any] = []

	func push(item: Any) {
			collection.append(item)
	}

	func pop() {
			collection.removeLast()
  }

	func display() {
			print(collection)
	}

  func sum() {

    var sum: Int = 0
    for item in collection {
			sum = sum + Int(item) // Casting is needed..
		}
		print(sum)

	}

}

var intStack: Stack<Int> = Stack()
intStack.push(item: 10)
intStack.push(item: 20)
intStack.sum() // 30

```

### 4) What are the advantages of Generics?

**Answer:**

- Generic avoids writing duplicate code **while achieving Swift’s Type Safety Feature.**

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

Section 12, generic

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