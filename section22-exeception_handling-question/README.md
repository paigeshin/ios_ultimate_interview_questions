# Exception Handling 1 ~ 3

### 1) What is an Exception? What is Exception Handling?

**Answer:**

- Exception is a **Runtime Error.**
- The process of Handling the runtime errors is known as **Exception Handling.**
- Use **do**, **try**, **catch**, **throw** and **throws** to achieve exception handling.

### 2) What are the advantages of exception handling?

**Answer:**

- Exception Handling is helpful to co-workers of a team to indicate that there is some **dangerous code, “**please be cautious while using that piece of code”.

### 3) What is defer keyword?

**Answer:**

- A block of code which gets executed just before the execution control comes out of that method.

```swift
struct AnyStruct {

	func method() {
			defer {
					print("This is the last statement which gets executed")
			}

			print("Run first")
			print("Run second")
			print("Run third")
	}

}

let executor: AnyStruct = AnyStruct()
executor.method()
// Run first
// Run second
// Run third
```
