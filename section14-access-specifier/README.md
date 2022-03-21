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
