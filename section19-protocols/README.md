# Protocols 143 ~ 154

### 1) What is Protocol? What kind of methods the protocol contains?

**Answer:**

- Protocol is a set of Property and Method declarations which are expected to be implemented in the adopting class.

### 2) Can we define methods in Protocol?

**Answer:**

- No, protocol just contains method declarations.

```swift
protocol AProtocol {
		// You can delare property without assigning value
    var initialValue: Int { get set }
	  // You can make read-only property
		var getOnly: Int { get }
    // You can have function without defining its body
    func add()
		func subtract()
}

struct Calculator: AProtocol {

		var initialValue: Int
		var getOnly: Int

		func add() {

		}

    func subtract() {

    }


}
```

### 3) Can we extend Protocols?

**Answer:**

- Yes. To provide default implementations, we can extend protocols.

```swift
protocol AProtocol {
		// You can delare property without assigning value
    var initialValue: Int { get set }
	  // You can make read-only property
		var getOnly: Int { get }
    // You can have function without defining its body
    func add()
		func subtract()
}

// Through extension, you can define properties and methods
extension AProtocol {

    // You can assign values within extension
    var initialValue: Int {
        get {
            return 0
        }
        set {

        }
    }

		var getOnly: Int {
			get {
					return 0
			}
		}

    // You can make body within extension
    func add() {
        print("Add")
    }

}

struct Calculator: AProtocol {

    // You must implement subtract() method because it doesn't have body
    func subtract() {

    }


}
```

### 4) How to adopt protocols or how to conform protocol?

**Answer:**

```swift
extension ObjectName: ProtocolName {

}
```

### 5) How to declare ‘class-only’ adoptable protocol?

**Answer:**

- By making protocol extend **AnyObject.**

```swift
protocol AProtocol: AnyObject {
    var initialValue: Int { get set }
    func add()
}

// Compile Error
struct Calculator: AProtocol {

}
```

### 6) How to declare Optional Methods and Properties in Protocols?

**Answer:**

- Use
  - @objc optional var variableName: Int { get set }
  - @objc optional func methodName()
  - But this protocol is only available to **class-type**

### 7) What are the advantages of Protocols?

**Answer:**

- To achieve multiple inheritance
- To achieve delegation
- To segregate specific feature methods into a single unit

```swift
protocol AProtocol {
    var property1: String { get set }
    func method1()
}

protocol BProtocol {
    var property2: String { get set }
    func method2()
}

struct aStruct: AProtocol, BProtocol {
    var property1: String

    func method1() {

    }

    var property2: String

    func method2() {

    }

}
```

### 8) How to provide default implementation for protocol methods?

**Answer:**

- Yes, by using protocol extensions we can provide default behavior for the protocol methods.

```swift
protocol AProtocol {
		// You can delare property without assigning value
    var initialValue: Int { get set }
	  // You can make read-only property
		var getOnly: Int { get }
    // You can have function without defining its body
    func add()
		func subtract()
}

// Through extension, you can define properties and methods
extension AProtocol {

    // You can assign values within extension
    var initialValue: Int {
        get {
            return 0
        }
        set {

        }
    }

		var getOnly: Int {
			get {
					return 0
			}
		}

    // You can make body within extension
    func add() {
        print("Add")
    }

}

struct Calculator: AProtocol {

    // You must implement subtract() method because it doesn't have body
    func subtract() {

    }


}
```

### 9) Can we declare stored properties in Protocols?

**Answer:**

- No, Protocols do not contain stored properties. We must specify the declared property is **get only** or **get** and **set**.

```swift
protocol AProtocol {
		// You can delare property without assigning value
    var initialValue: Int { get set }
}

// Through extension, you can define properties and methods
extension AProtocol {

    // You can assign values within extension
    var initialValue: Int {
        get {
            return 0
        }
				set {

				}
    }


}
```

### 10) What is the default behavior of Protocol Methods?

**Answer:**

- By default, all methods in Protocol are **required.**

### 11) Can we declare an optional variable as let?

**Answer:**

- No, Optional variables are not expected to have a value in future. So to set or assign a value in future, the optional variable must be **var.**

### 12) Is Swift Object-Oriented Language or Protocol Oriented Programming Language?

**Answer:**

- Swift is Protocol Oriented Programming Language.
