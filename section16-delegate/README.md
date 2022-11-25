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

Section 16, delegate

[Section 17, extension](/section17-extension/README.md)

[Section 18, Memory Management](/section18-memory_management/README.md)

[Section 19, protocols](/section19-protocols/README.md)

[Section 20, collections](/section20-collections/README.md)

[Section 21, KVO and KVC](/section21-kvo_kvc-question/README.md)

[Section 22, Exception Handling](/section22-exeception_handling-question/README.md)

[Section 23, Framework](/section23-framework-question/README.md)

[Section 24, Objective-C](/section24-objective_c-question/README.md)