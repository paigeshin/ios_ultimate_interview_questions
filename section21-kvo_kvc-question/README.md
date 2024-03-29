# KVO and KVC 1 ~ 6

### 1) What is KVO? Advantages?

**Answer:**

- **Key Value Observing** is a process of observing changes of an object.
- KVO helps to update the UI when there is a change in the property value that is displayed in the user interface.

### 2) What is KVC?

**Answer:**

- Key Value Coding is a process of alternate way to access Properties of a Class

```swift
class BankAccount: NSObject {

    @objc dynamic var balance: Int = 0

    func deductAnnumalMaintenance() {
        balance -= 25
    }

    func depositAmount(amount: Int) {
        balance += amount
    }

    func withdrawAmount(amount: Int) {
        balance -= amount
    }

}

class Human: NSObject {

    @objc var myAccount: BankAccount = BankAccount()
    var observer: NSKeyValueObservation?

    func observeChangesInMyBalance() {
        self.observer = self.observe(\.myAccount.balance, options: [.old, .new]) { human, change in
            print(change)
        }
    }

    deinit {
        observer?.invalidate()
    }

}

let human: Human = Human()
human.observeChangesInMyBalance()
human.myAccount.deductAnnumalMaintenance()
// NSKeyValueObservedChange<Int>(kind: __C.NSKeyValueChange, newValue: Optional(-25), oldValue: Optional(0), indexes: nil, isPrior: false)
human.myAccount.depositAmount(amount: 300)
// NSKeyValueObservedChange<Int>(kind: __C.NSKeyValueChange, newValue: Optional(275), oldValue: Optional(-25), indexes: nil, isPrior: false)
```

### 3) Can we use KVC for Structures?

**Answer:**

- NO

### 4) What is KVC?

**Answer:**

- Key Value Coding is a process of alternate way to access Properties of a Class.

```swift
class BankAccount: NSObject {

    @objc dynamic var balance: Int = 0

    func deductAnnumalMaintenance() {
        balance -= 25
    }

    func depositAmount(amount: Int) {
        balance += amount
    }

    func withdrawAmount(amount: Int) {
        balance -= amount
    }

}

class Human: NSObject {

    @objc var myAccount: BankAccount = BankAccount()
    var observer: NSKeyValueObservation?

    func observeChangesInMyBalance() {
        self.observer = self.observe(\.myAccount.balance, options: [.old, .new]) { human, change in
            print(change)
        }
    }

    deinit {
        observer?.invalidate()
    }

}

let human: Human = Human()
human.observeChangesInMyBalance()
human.myAccount.balance = 3000

// You can access `@objc dynamic var balance: Int` through "balance"
human.myAccount.setValue(2000, forKey: "balance")
print(human.myAccount.balance) // 2000
```

### 5) What is dynamic keyword?

**Answer:**

- dynamic says to compiler that you want to use **Objective-C dynamic dispatch.**
- Mainly used for KVO and for core data properties.

### 6) What is @objc keyword?

**Answer:**

- @objc indicates that the code is available for not only swift code, but also for objc code.

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

[Section 18, Memory Management](/section18-memory_management/README.md)

[Section 19, protocols](/section19-protocols/README.md)

[Section 20, collections](/section20-collections/README.md)

Section 21, KVO and KVC

[Section 22, Exception Handling](/section22-exeception_handling-question/README.md)

[Section 23, Framework](/section23-framework-question/README.md)

[Section 24, Objective-C](/section24-objective_c-question/README.md)