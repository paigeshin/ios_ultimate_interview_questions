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
