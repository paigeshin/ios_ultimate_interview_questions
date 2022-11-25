# Delegate 1 ~ 2

### 1) What is Delegation?

**Answer:**

- Delegation is one of the design pattern which is used to establish the communication between one to one objects.

```swift
protocol ADelegate {
    func eventOccured()
}

class A {

    var delegate: ADelegate?

    func makeEvent() {
        delegate?.eventOccured()
    }

}

class B: ADelegate {


    let a: A

    init(a: A) {
        self.a = a
        a.delegate = self
    }

    func eventOccured() {
        print("class A made an event")
    }

}

let a: A = A()
let b: B = B(a: a)
a.makeEvent() // class A made an event
```

### 2) Can delegate be a weak and why delegate must be weak?

**Answer:**

- Delegate variable must be week because its parent reference object can be removed from the memory at any point of time.

```swift
protocol ADelegate: AnyObject {
    func eventOccured()
}

class A {

    // Declared with weak
    weak var delegate: ADelegate?

    func makeEvent() {
        delegate?.eventOccured()
    }

}

class B: ADelegate {

    let a: A

    init(a: A) {
        self.a = a
        a.delegate = self
    }

    func eventOccured() {
        print("class A made an event")
    }

}
```

# Table Of Contents

[Section 1, Data Type](./section1-datatypes/)

[Section 2, Operator](./section2-operator/)

[Section 3, Conditional Statement](./section3-conditional-statement/)

[Section 4, Enum](./section4-enum/)

[Section 5, functions](./section5-function/)

[Section 6, struct](./section6-struct/)

[Section 7, initializers](./section7-initializers/)

[Section 8, closures](./section8-closures/)

[Section 9, OOP](./section9-oop/)

[Section 10, static type vs dynamic type](./section10-static_dynamic_type_difference/)

[Section 11, optional](./section11-optional/)

[Section 12, generic](./section12-generic/)

[Section 13, subscript](./section13-subscript/)

[Section 14, access specifier](./section14-access-specifier/)

[Section 15, higher order function](./section15-higher_order_fuctions/)

Section 16, delegate

[Section 17, extension](./section17-extension/)

[Section 18, Memory Management](./section18-memory_management/)

[Section 19, protocols](./section19-protocols/)

[Section 20, collections](./section20-collections/)

[Section 21, KVO and KVC](./section21-kvo_kvc-question/)

[Section 22, Exception Handling](./section22-exeception_handling-question/)

[Section 23, Framework](./section23-framework-question/)

[Section 24, Objective-C](./section24-objective_c-question/)