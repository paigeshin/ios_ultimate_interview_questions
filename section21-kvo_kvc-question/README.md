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

[Section 16, delegate](./section16-delegate/)

[Section 17, extension](./section17-extension/)

[Section 18, Memory Management](./section18-memory_management/)

[Section 19, protocols](./section19-protocols/)

[Section 20, collections](./section20-collections/)

Section 21, KVO and KVC

[Section 22, Exception Handling](./section22-exeception_handling-question/)

[Section 23, Framework](./section23-framework-question/)

[Section 24, Objective-C](./section24-objective_c-question/)