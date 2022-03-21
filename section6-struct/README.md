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
