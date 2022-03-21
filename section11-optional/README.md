# Optional Questions 1 ~ 17

### 1) What is Optional and How to declare an Optional?

**Answer:**

- Optional is a variable which is capable of holding a value or absence of a value(i.e. nil)

```swift
var aOptional: Int?
aOptional = nil
var bOptional: Int!

// Compile Error
var geneal: Int = nil
```

### 2) What is Optional Unwrapping and What are the different ways to unwrap optionals?

**Answer:**

- Extracting the underlying value of an Optional Variable is called Optional Unwrapping.
- Force Unwrapping(!)
- Optional Binding
- Guard Statement
- Nil Coalescing Operator (??)

### 3) What is Implicit Unwrapping and how to declare implicit unwrapped Optional? When do you declare an implicit optional variable?

**Answer:**

- Process of conveying to compiler that the variable must contain a value before it is used.

```swift
var aOptional: Int?
var bOptional: Int! // Implicit Optional
bOptional = 10

// Force Unwrapping
let sum: Int = aOptional! + bOptional
```

### 4) What is Optional Binding?

**Answer:**

- Optional Binding is one of the optional unwrapping techniques.

```swift
var aOptional: Int?
var bOptional: Int! // Implicit Optional
aOptional = 10
bOptional = 20

// aOptional is unwrapped with Optional Binding
if let unwrappedAOptional = aOptional {
	print(aOptional + bOptional) // 30
} else {
	print("Optional has no value")
}
```

### 5) What is ?? in Swift?

**Answer:**

- ?? is nil-coalescing operator, which helps to provide a default value if optional variable has no value when unwrapping
- `let value = optional ?? DefaultValue`

```swift
var aOptional: Int?

// if aOptional has no value, its default value is set to 0
print(aOptional ?? 0) // 0
```

### 6) What is guard statement?

**Answer:**

- Make sure some condition should be met
- You can use guard statement to unwrap optional variable

```swift
var aOptional: Int?
aOptional = 15

guard let unwrappedAOptional: Int = aOptional else {
	print("optional has no value!")
	// if aOptional has no value, execution code stops here
	return
}

print(unwrappedAOptional) // 15
```

### 7) What is Force unwrapping in Swift?

**Answer:**

- Force unwrapping is one of the optional unwrapping technique. Use force unwrapping when you are sure the optional variable contains a value.
- Fore unwrapping is not good practice which may lead to crashes.

```swift
var aOptional: Int?

// Crashes occur because aOptional doesn't have any value
print(aOptional)
```

### 8) What is the difference between Optional Binding and Guard statement?

**Answer:**

- The variable you declares in `if let` statement is accessible within that block of code.
- The variable you declares in `guard let` is accessible in the rest of the method.

```swift
var aOptional: Int?
var bOptional: Int! // Implicit Optional
aOptional = 10
bOptional = 20

if let unwrappedAOptional = aOptional {
  // only within this block, you can access unwrappedAOptional
	let sum: Int = unwrappedAOptional + bOptional
	print(sum) // 30
}

// The rest of programs can access unwrappedAOptional.
guard let unwrappedAOptional = aOptinoal else { fatalError("aOptional is nil") }
let sum: Int = unwrappedAOptional + bOptional
print(sum) // 30
```

### 9) Can we access guard statement variable inside the else block?

**Answer:**

- NO

```swift
var aOptional: Int?
guard let unwrappedAOptional = aOptinoal else {
  // Compile Error, You can't access variable declared in 'guard' condition
	print(unwrappedAOptional) //Not Possible
	fatalError("aOptional is nil")
}
```

### 10) Is optional Enum Type or Struct Type?

**Answer:**

- Optional is an enum. It contains following cases.
  - none
  - some

### 11) Can we use var in optional binding or guard statement instead of let?

**Answer:**

- Yes, you can use var instead of let.

```swift
var aOptional: Int?

if var value = aOptional {

}

guard var value = aOptional else { return }
```

### 12) What is fast enumeration?

**Answer:**

- Process of iterating through all elements of a collection in an efficient way. It is **faster than general for loop.**

```swift
let data: [Int] = [1, 2, 3, 4, 5, 6, 7, 8, 9]
for value in data {
}
```

### 13) What is Optional Chaining?

**Answer:**

- The process accessing Optional variables’ sub properties or sub sub properties which are again optionals.
- `let value = optionalProperty?.subOptionalProperty?.subSubOptionalProperty`
- If any of the property is optional, the complete result will be **nil.**

```swift
struct Store {
	var name: String?
	var brand: Brand?
}

struct Brand {
	var title: String?
	var founded: String?
}

let store: Store? = Store()
// Optional Chaining
store?.brand?.title
```

### 14) What is the difference between nil and .none?

**Answer:**

- Both are same

```swift
struct Store {
	var name: String?
	var brand: Brand?
}

struct brand {
	var title: String?
	var founded: String? = .none
}

let store: Store? = Store()

print(store?.brand?.found == nil) // true

```

### 15) What happens when you call a method over optional whose value is nil?

**Answer:**

- Application will crash

```swift
struct Store {
	var name: String?
	var brand: Brand!
}

struct brand {
	var title: String?
	var founded: String? = .none

  func displayTitle() {
		  print(title ?? "no title")
  }

}

let store: Store? = Store()
// Error
store?.brand.displayTitle()

```

### 16) What is Type Checking Operator in Swift?

**Answer:**

- **“is”** is a Type checking operator

```swift
var someVar: Any = "Hello I am a String"

if someVar is String {
		print(someVar) // Hello I am a String
} else if someVar is Double {
		print("Some value is double") // This won't be printed
}
```

### 17) What is as?, as! in Swift?

**Answer:**

- as? is Optional Consideration
- as! is Forceful Consideration

```swift
var someVar: Double = 20.0
var aVar: Int = 10

// Forceful Consideration
let forcefulConsiderationResult: Int = aValue + (someVar as! Int)
print(forcefulConsiderationResult) // 30

// Optional Consideration
if let unwrappedSomeVar = someVar as? Int {
	let optionalConsiderationResult: Int = aVar + unwrappedSomeVar
	print(optionalConsiderationResult) // 30
}
```
