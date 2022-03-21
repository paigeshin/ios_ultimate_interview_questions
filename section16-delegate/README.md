# Delegate 121 ~ 122

### 121) What is Delegation?

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

### 122) Can delegate be a weak and why delegate must be weak?

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
