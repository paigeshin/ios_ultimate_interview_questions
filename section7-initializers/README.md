# Initializer Questions 1 ~ 10

### 1) What is initializer?

**Answer:**

- Initializer is a method that constructs the object with proper default values.

```swift
struct SomeStruct {

	init() {}

}
```

### 2) What are the different types of initializers available in Swift?

**Answer:**

- Default
- Customized
- Convenience
- Failable
- Required

```swift
/*** Class & Struct Initializers ***/

// Default
struct SomeStruct {

	// init() {}

}

// Customized
struct SomeStructWithCustomization {

	let value1: String = "value"
	let value2: String

	init(value2: String) {
		self.value2 = value2
	}

	init(value1: String, value2: String) {
		self.value1 = value1
		self.value2 = value2
	}

}

// Convenience
struct SomeStructWithConvenience {
	let value1: String
	let value2: String

	init(value1: String, value2: String) {
		self.value1 = value1
		self.value2 = value2
	}

	// Convenience init
	// Convenience init should initialize `init(value1: String, value2: String)`
	// Why doing this? Because it can be convenient
	convenience init() {
		self.init(value1: "value1", value2: "value2")
	}

}

// Failable

// Required
protocol SomeStructProtocol {
	init(value1: String)
}

struct SomeStructWithRequiredInitializer: SomeStructProtocol {

	let value1: String

	required init(value1: String) {
		self.value1 = value1
	}

}

```

### 3) What is the default initializer in Swift?

**Answer:**

- **init** is the default initializer in Swift.

```swift
struct SomeStruct {

	// init() {}

}

class SomeCalss {

	// init() {}

}
```

### 4) What is parameterized / Custom Initializer?

**Answer:**

- init method with some input parameters to construct the object with custom values.

```swift
class Car {

	var model: Int = 0
	var speed: Int = 0
	var color: String = ""

	init() {
		self.model = 2022
		self.speed = 0
		self.color = "Red"
	}

	init(model: Int, color: String) {
		self.model = model
		self.speed = 0
		self.color = color
	}

}

let car: Car = Car()

print(car.color) // Red

let purpleCar: Car = Car(model: 2022, color: "Purple")

print(purpleCar.color) // Purple
```

### 5) What is designated initializer in Swift?

**Answer:**

Default init method is the designated initializer

### 6) What is convenience initializer in Swift?

**Answer:**

- **Convenience Initializer** is a kind of initializer which sets custom values for a few properties of an Object. Use convenience keyword to create convenience initializer.
- **Designated initializer** must be called before setting the custom values.

```swift
class Car {

	let model: Int
	let speed: Int
	let color: String

	init(model: Model, speed: Int, color: String) {
		self.model = model
		self.speed = speed
		self.color = color
  }

	//Convenience init must call `**Designated initializer`** first!
	convenience init(color: String) {
		init(model: 2022, speed: 80, color: color)
	}

}

let car: Car = Car(color: "Red")
print(car.model) // 2022

let newCar: Car = Car(model: 2024, speed: 120, color: "Blue")
print(car.model) // 2024

```

### 7) What is failable initializer in Swift?

**Answer:**

- An initializer which may fail to construct Object, User **init?(params)** to create failable initializers.

```swift
class Car {
	var model: Int = 0
	var color: String = ""
	var numberOfGears: Int = 0

	init(price: Int) {
			if price < 0 {
				return nil
			}
			self.model = 2019
			self.color = "Blue"
			self.numberOfGears = 5
	}

}
```

### 8) Can I declare a convenience initializer without designated initializer?

**Answer:**

- No

```swift
class Car {

	let model: Int
	let speed: Int
	let color: String

//	init(model: Int, speed: Int, color: String) {
//		self.model = model
//		self.speed = speed
//		self.color = color
//	}

	convenience init(color: String) {
		#warning("Compilation Error")
		self.init() // Cannot invoke 'Car.init'
		self.color = color
	}

}
```

### 9) What is deinit? Can we call deinit method?

**Answer:**

- **deinit** is a method which gets called automatically when the object is getting cleaned from memory. Additionally, you can dispose any resources in **deinit** method.

```swift
class Car {

	let model: Int
	let speed: Int
	let color: String

	init(model: Int, speed: Int, color: String) {
		self.model = model
		self.speed = speed
		self.color = color
	}

	deinit {
		print("Clear Car Object From Memory")
	}

}

var car: Car? = Car(model: 2024, speed: 500, color: "Red")
car = nil // Clear Car Object From Memory

#warning("We cannot call deinit method")
car.deinit // not callable
```

### 10) Designated Initializer vs Convenience Initializer

**Answer:**

- Designated initializer is common initializer which makes sure all properties of a class are assigned with proper values.
- Convenience initializer calls designated initializer and makes sure all properties are initialized. hen the custom values will be assigned for some properties.

# Table Of Contents

[Section 1, Data Type](/section1-datatypes/README.md)

[Section 2, Operator](/section2-operator/README.md)

[Section 3, Conditional Statement](/section3-conditional-statement/README.md)

[Section 4, Enum](/section4-enum/README.md)

[Section 5, functions](/section5-function/README.md)

[Section 6, struct](/section6-struct/README.md)

Section 7, initializers

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
