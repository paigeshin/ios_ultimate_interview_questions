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
