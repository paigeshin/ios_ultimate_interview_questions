# Memory Management 1 ~ 14

### 1) What is the concept of the Memory Management?

**Answer:**

- Memory Management is the process of controlling the lifetime of an object based on its necessity

```swift
var car: Car? = Car()
car.move()
car.blowHorn()
car.stop()
car = nil //release
```

### 2) What is Manual Memory Management?

**Answer:**

- Prior to ARC, developer was responsible for retaining and releasing the objects’ memory using **release**, **retain** and **autorelease**.

### 3) What is ARC?

**Answer:**

- **Automatic Reference Counting** is a concept of managing the memory automatically by the runtime system.
- But still there are three different places where developer has to take of releasing the memory.
  - Closures
  - Delegates
  - Outlets

### 4) What is Memory Leak?

**Answer:**

- Memory Leak is a situation where the runtime system fails to release the memory of unused objects.

### 5) What is Strong?

**Answer:**

- **Strong** shares the ownership of the object and increases the reference count by 1.

```swift
class Car {

  func move() {
		print("Car is moving")
  }

}

var car: Car? = Car()
car?.move()

// Strong Reference Occured
var anotherCar: Car? = car

car?.move() // Car is moving
anotherCar?.move() // Car is moving

car = nil
car?.move() // Not executing
anotherCar?.move() // Car is moving, not released
anotherCar!.move() // Car is moving, not released
```

### 6) What is Weak?

**Answer:**

- **weak** shared the ownership of the object without increasing the reference count.

```swift
class Car {

  func move() {
		print("Car is moving")
  }

}

var car: Car? = Car(
// Strong Reference Occured
weak var anotherCar: Car? = car

car?.move() // Car is moving
anotherCar?.move() // Car is moving

car = nil
car?.move() // Not executing
anotherCar?.move() // Not executing. released
anotherCar!.move() // Crash happens
```

### 7) strong vs weak

**Answer:**

- **strong** and **weak** are memory management related keywords.
- When you assign a variable to another:
  - **strong** shares the ownership of the object and increases the reference count by 1.
  - **weak** shares the ownership and doesn’t increase the reference of that object.

### 8) What is Retain Cycle?

**Answer:**

- When two objects are pointing each other strongly and ARC fails to release memory. It leads to memory leaks. This situation is called **Retain / Reference Cycle.**

### 9) What are the different places we use weak?

**Answer:**

- Closures
- Delegates
- Outlets

```swift
class Human {

	var heart: Heart? = nil

	deinit {
			print("Human is released")
	}

}

class Heart {

	var owner: Human? = nil

	deinit {
			print("Heart is released")
	}

}

var person: Human? = Human()
var heart: Heart? = Heart()
person?.heart = heart
heart?.owner = person

person = nil // "Human is released" is not printed
heart = nil // "Heart is released" is not printed
```

```swift
class Human {

    weak var heart: Heart? = nil

    deinit {
        print("Human is released")
    }

}

class Heart {

    weak var owner: Human? = nil

    deinit {
        print("Heart is released")
    }

}

var person: Human? = Human()
var heart: Heart? = Heart()
person?.heart = heart
heart?.owner = person

person = nil // Human is released
heart = nil // Heart is released
```

### 10) weak vs unowned

**Answer:**

- **weak** and **unowned** are keywords used to avoid retain cycles.
- **weak** variable might become nil. So weak variables are declared as var and Optional.
- When **weak** is used in closures, weak references act like optionals. So when you use them in closures, you have to use optional chain with them.
- **unowned** variables never become nil. So unowned variables can be declared as let and stored.
- You can use **unowned** when the other instance has the same life time or the longer lifetime.
- Use **unowned**, when you are sure it is not nil.

### 11) Is ARC compile time mechanism or run time mechanism?

**Answer:**

- Compile Time

### 12) What is the difference between ARC and Garbage Collector?

**Answer:**

- GC takes more memory to run its algorithm.
- ArC takes less memory to function.
- GC follows Mark and Sweep algorithm.
- ARC follows the reference count of the object.
- GC impacts the performance.
- ARC doesn’t impact performance.
- GC resolves retain cycles automatically.
- ARC doesn’t resolve retain cycles automatically.

### 13) What is circular reference?

**Answer:**

- When two objects are pointing each other strongly and ARC fails to release memory.

### 14) How do you identify the retain cycle in iOS?

**Answer:**

- By using instrument tool we can identify Retain Cycles.

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

Section 18, Memory Management

[Section 19, protocols](/section19-protocols/README.md)

[Section 20, collections](/section20-collections/README.md)

[Section 21, KVO and KVC](/section21-kvo_kvc-question/README.md)

[Section 22, Exception Handling](/section22-exeception_handling-question/README.md)

[Section 23, Framework](/section23-framework-question/README.md)

[Section 24, Objective-C](/section24-objective_c-question/README.md)