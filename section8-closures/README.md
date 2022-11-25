# closure questions 1 ~ 7

### 1) What is Closure? How to declare closures?

**Answer:**

- Closure is a block of statements which can be passed as an argument to a method.
- Closure can be added to collections.
- Closure can be saved in a variable.

```swift
/*** Closures ***/

func add(a: Int, b: Int) -> Int {
	return a + b
}

let addClosure: (Int, Int) -> Int = { (a: Int, b: Int) -> Int in
    return a + b
}

let result: Int = add(a: 5, b: 12)
print(result) // 17

let resultWithClosure: Int = addClosure(3, 8)
print(resultWithClosure) // 11

func emptyFunction() {
		print("This is empty function")
}

let emptyClosure: () -> Void {
		print("This is empty closure")
}

emptyFunction() // This is empty function
emptyClosure() // This is empty closure
```

### 2) What is completion handler in Swift?

**Answer:**

- Takes a closure as an argument. Very common practice when developing with Swift.

```swift
func methodThatExpects(completion: (Int, Int) -> Int) -> Void {
    let result: Int = completion(10, 20)
    print("Result: \(result)") // 30
}

methodThatExpects { (a, b) -> Int in
    return a + b
}
```

### 3) How to avoid retain cycle in closures?

**Answer:**

- Use **[weak self]** or **[unowned self]**

```swift
class Example {

    var someVar: Int = 10

    func methodThatExpects(completion: (Int, Int) -> Int) -> Void {
        let result: Int = completion(10, 20)
        print("Result: \(result)") // 30
    }

    // Whenever this method is called, someVar is set to 20
    func callClosure() {
        methodThatExpects { [weak self] (a, b) -> Int in
            self?.someVar = 20
            return a + b
        }
    }

}
```

### 4) What is escaping Closure?

**Answer:**

- A closure is passed as an argument to a method. That closure will be called after some time of execution control when coming out of that method.
- **@escaping** keyword to indicate that the closure will be called after some time of control.
- By marking **@escaping**, closure is called even when function execution is finished.

```swift
class NetworkService {

    var numberOfCallCounts: Int = 0

    func call(completion: @escaping() -> Void) {
        numberOfCallCounts += 1
        DispatchQueue.main.asyncAfter(deadline: .now() + 3) {
            completion()
        }
        print("Number Of Call Counts: ", numberOfCallCounts)
    }


}

let networkService: NetworkService = NetworkService()
networkService.call {
    print("Hey Closure!")
}

// Output

// Number Of Call Counts: 1
/* After Three Seconds */
// Hey Closure!

```

### 5) Does closure capture values?

**Answer:**

- Yes closures capture values

### 6) What is Trailing Closure?

**Answer:**

- A method which has closure as the last parameter is called **trailing closure.**

```swift
func someMethod(arg1: String, arg2: String, completion: () -> Void) {

}
```

### 7) What is the shorthand syntax for Closures?

**Answer:**

- A syntax which enables us to use $0 and $1 to refer input arguments of a closure

```swift
/*** Example 1  ***/
func callMyName(completion: (String, String) -> Void) {
    completion("Paige", "Shin")
}

callMyName(completion: { print("\($0), \($1)") })

callMyName { print("\($0), \($1)") }

callMyName {
    print("\($0), \($1)")
}

/*** Example 2 ***/
let closure: (Int, Int) -> Void = { print($0 + $1) }
closure(10, 20) // 30

let closure2: (Int, Int) -> Void = { (a: Int, b: Int) -> Void in
		print(a + b)
}
closure2(10, 30) // 40

// Practical Example
let names: [String] = ["Paige", "Sunghee"]
// sorted alphabetically using closure shorthand syntax
names.sorted { $0 > $1 }
```

# Table Of Contents

[Section 1, Data Type](./section1-datatypes/)

[Section 2, Operator](./section2-operator/)

[Section 3, Conditional Statement](./section3-conditional-statement/)

[Section 4, Enum](./section4-enum/)

[Section 5, functions](./section5-function/)

[Section 6, struct](./section6-struct/)

[Section 7, initializers](./section7-initializers/)

Section 8, closures

[Section 9, OOP](./section9-oop/)

[Section 10, static type vs dynamic type](./section10-static_dynamic_type_difference/)

[Section 11, optional](./section11-optional/)

[Section 12, generic](./section12-generic/)

[Section 13, subscript](./section13-subscript/)

[Section 14, access specifier](./section14-access-specifier/)

[Section 15, higher order function](./section15-higher_order_fuctions/)

[Section 16, delegate](./section16-delegate/)

[Section 17, extension](./section17-extension/)

[Section 18, Memory Management](./section18-memory_management/)

[Section 19, protocols](./section19-protocols/)

[Section 20, collections](./section20-collections/)

[Section 21, KVO and KVC](./section21-kvo_kvc-question/)

[Section 22, Exception Handling](./section22-exeception_handling-question/)

[Section 23, Framework](./section23-framework-question/)

[Section 24, Objective-C](./section24-objective_c-question/)
