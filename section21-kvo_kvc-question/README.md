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
