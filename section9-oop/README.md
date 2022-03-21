# oop questions 1 ~ 27

### 1) What are the Object Oriented Principles (OOPs)?

**Answer:**

- Class
- Object
- Encapsulation
- Inheritance
- Abstraction
- Polymorphism

### 2) What is Class? How to declare it?

**Answer:**

- Class is a Blueprint or Template / Logical Structure / Skeleton to create Objects
- **Class doesn’t own any memory.** Once class is created we can create any number of objects out of that class.

```swift
class TV {

	var model: Int = 2023

	func start() {

	}

	func changeChannel() {

	}

}
```

### 3) What is Instance / Object?

**Answer:**

- Object is an instance of a class.
- Object is a Physical live implementation of the Class.
- Collection of Properties and Methods.

```swift
class Example {

	// Properties
	var var1: String = ""
	var var2: String = ""

	// Methods
	func method1() {}
	func method2() {}

}

// instance, Object
let object: Example = Example()

```

### 4) What is Property?

**Answer:**

- Properties are instance members of a Class / Structure which stores information about that Class / Structure

```swift
class ExampleClass {

	// Properties, Instance Members
	var var1: String = ""
	var var2: String = ""

	// Methods, Instance Members
	func method1() {}
	func method2() {}

}

// instance, Object
let object: ExampleClass = ExampleClass()

struct ExampleStruct {

	// Properties, Instance Members
	var var1: String = ""
	var var2: String = ""

	// Methods, Instance Members
	mutating func method1() {
		var1 = "Hell World"
	}
	func method2() {}

}
```

### 5) What are the 4 types of Properties?

**Answer:**

- Stored Properties
- Computed Properties
- Lazy Properties
- Static / Type Properties

```swift
class Person {

		// Stored Properties
		let firstName: String = "Paige"
		let lastName: String = "Shin"

		// Computed Properties
		var fullName: String {
			get {
				return "\(firstName), \(lastName)"
			}
		}

		// Lazy Properties
		lazy var hasGirlfriend: Bool = {
			return true
		}()

		// Static Properties
		static let Nationality: String = "Korea"

		// Type Properties
		class var age: Int = 32

}
```

### 6) What is stored Property?

**Answer:**

- A property which holds direct value is known as Store Properties.

```swift
class Person {

		// Stored Properties
		let firstName: String = "Paige"
		let lastName: String = "Shin"

}
```

### 7) What is Computed Property?

**Answer:**

- The value of computed property gets calculated when it is accessed and the value of computed property depends on the other properties of the Class / Structure.

```swift
class Person {

		// Stored Properties
		let firstName: String = "Paige"
		let lastName: String = "Shin"

		// Computed Properties
		var fullName: String {
				return "\(firstName), \(lastName)"
		}

}
```

### 8) What is Static Property or Type Property? How to declare them?

**Answer:**

- Type properties are class level properties whose memory will be allocated **only once.**
- Access type properties using **ClassName.typePropertyName**

```swift
class Person {

		// Type & Static Properties
		static let Nationality: String = "Korea"

}

print(Person.Nationality) // Korea
```

### 9) What is lazy property?

**Answer:**

- A property whose memory will be **allocated when the variable actually used.**

```swift
class TV {

	lazy var logo: String = "Apple"

}

let tv: TV = TV()
print(tv.logo) // memory is allocated when called
```

### 10) static keyword vs class keyword

**Answer:**

- **static** is used to declare **Type Properties** and **Type Methods** in **Structures** and **Classes.**
- **class** keyword is only used in **Classes** to create Type methods but not Type Properties.

```swift
class Person {

    // Class Properties are not allowed..
    #warning("Compile Error")
    class var bloodType: String = "A"

		// Work around..
		class var born: Int {
			return 1991
		}

    // Works!
    class func sayMyName() {

    }

}
```

### 11) What are Property Observers?

**Answer:**

- **willSet** and **didSet** are the property observers.
- These blocks get triggered when there is a change in the value.

```swift
class Person {

 var age: Int? {
 	 willSet {
 		 print("Age is about to change: \(newValue)")
	 }
	 didSet {
		 print("Age is changed: \(oldValue)")
	 }
 }

}

let person: Person = Person()
person.age = 30
// Age is about to change: Optional(30)
// Age is changed: nil
person.age = 31
// Age is about to change: Optional(31)
// Age is changed: Optional(30)
```

### 12) What is get and set? How to declare get only or set property?

**Answer:**

- The read and write access of a property can be declared by using **get** and **set** keywords.
- You can access the value of get only property but cannot set the value.
- A property must contain at least **get.**

```swift
class Person {

 var age = 0
 var days: Int {
		get {
			return age * 365
		}
 }

}

let person: Person = Person()
person.age = 5
print(person.days) // 1825

// Compile Error.. because it's declared with get only
person.days = 3000
```

```swift
class Person {

 var age = 0
 var days: Int {
		get {
			return age * 365
		}
		set {
			age = newValue / 365
		}
 }

}

let person: Person = Person()
person.age = 5
print(person.days) // 1825

person.days = 3000
print(person.days) // 2920
```

### 13) Can a property has only setter(set)?

**Answer:**

- **No,** Every property must contain a getter. We can declare get only property but not **set** only property.

### 14) Difference between Class vs Structures?

**Answer:**

- **Structures are value types.**
- Classes are reference types.
- **Structures don’t support inheritance.**
- classes support inheritance.
- **Structures don’t support de-initializers. ( deinit )**
- Classes support deinitializers.
- **Structures don’t follow Reference Counting.**
- Classes follow Reference Counting.
- **Mutating Keyword is needed to modify the property values in Structure’s instance methods.**
- No need of mutating keyword to modify the class variable’s value.

### 15) What is Encapsulation? Example? Advantages?

**Answer:**

- Encapsulation is process of binding instance variables / properties and methods together into a single unit.
- **Class** is an example of encapsulation.

### 16) What is Inheritance?

**Answer:**

- Deriving a class from another class or extending the functionality of a class by subclassing is known as Inheritance.

### 17) What are the advantages of Inheritance?

**Answer:**

- Reusing the existing functionality.

### 18) What is Polymorphism?

**Answer:**

- Polymorphism is the ability to appear in many forms.
- There are two kinds of polymorphism:

1. Static Polymorphism / Overloading
2. Dynamic Polymorphism / Overriding

### 19) What is Dynamic Polymorphism / Overriding?

**Answer)**

- In inheritance relationship, having **the same method with the same name with difference in implementation** in subclass and superclass is known as Overriding / Dynamic Polymorphism.

```swift
class Person {

 func run() {
     print("Running with speed of 10")
 }

}

class Man: Person {

 // Dynamic Polymorphism
 override func run() {
			//super.run() => this will run Person::class.run()
     print("Running with speed of 10")
 }

}
```

### 20) What is Static Polymorphism / Overloading?

**Answer)**

- In a class having multiple methods with same name but different in
  1. number of Parameters (or)
  2. Order of Parameters (or)
  3. Type of Parameters

```swift
class Person {

 func run() {
     print("Running with speed of 10")
 }

 // Overloading
 func run(speed: Int) {
     print("Running with \(speed)")
 }

 // Overloading
 func run(speed: Float) {
		 print("Running with \(speed)")
 }

 // Overloading
 func run(speed: Int, weight: Float) {

 }

 // Overloading
 func run(speed: Float, weight: Float) {

 }

}
```

### 21) What is Abstraction? How to achieve it?

**Answer:**

- Abstraction is the process of hiding **unnecessary** functionality and exposing **necessary** functionality.
- Abstraction can be achieved using Access Specifiers.

### 22) Does swift support multiple inheritances?

**Answer:**

- No, Use protocols to achieve Multiple Inheritance.

### 23) How to call a method with some delay?

**Answer:**

- self.perform(#selector(methodName), with nil, afterDelay: 5.0)
- DispatchQueue

```swift
class Perosn: NSObject {

  func executeSomeMethod() {
		self.perform(#selector(callAfter5Seconds), with: nil, afterDelay: 5)
	}

  @objc func callAfter5Seconds() {

	}

}
```

```swift
class Perosn {

  func executeSomeMethod() {
		DispatchQueue.main.asyncAfter(deadline: .now() + 5) { [weak self] in
			self?.callAfter5Seconds()
		}
	}

  func callAfter5Seconds() {

	}

}
```

### 24) What is Base / Root class in Swift?

**Answer:**

- Swift has no base class as in Objective-C.
- Classes can be created without any base class / parent class. In such cases, the current class itself is the base class.
- If a class is derived from any class, then the super class is its base class.

### 25) What is self and super keywords?

**Answer:**

- **self** and **super** are keywords used in instance methods of a class.
- **self** refers to the current class object in which the method is present. To refer **the current class properties and methods** use **self**.
- **super** refers to the Parent class object of the current class. To refer its **Parent class properties and methods** use **super**.

```swift
class Person {

  var age: Int
	var name: String

	init(age: String, name: String) {
    self.age = age
    self.name = name
  }

  func sayMyName() {
			print("\(self.name)")
	}

  func printMyInfo() {
      self.sayMyName()
      print("and I'm \(self.age)")
  }

}

class Woman: Person {

  override func sayMyName() {
		super.sayMyName()
  }

}
```

### 26) Can we achieve Overriding without inheritance?

**Answer:**

- No, overriding needs at least two classes and those two must be in inheritance relationship.

### 27) When do you prefer struct over class?

**Answer:**

- In Swift, **structs** and **classes** give you **value** and **reference-based** constructs for your objects.
- struct is preferred for objects designed for **data storage** like **Array.**
- struct also helps remove memory issues when passing objects in a multi-threaded environment.
- class, unlike struct, supports inheritance and is used more for containing logic like UIViewController.
- Most standard library data objects in Swift, like String, Array, Dictionary, Int, Float, Boolean, are all structs, therefore value objects.
