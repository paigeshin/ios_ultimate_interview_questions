# Subscript 1

### 1) What is subscript? How to declare subscript? Advantages?

**Answer:**

- Subscript is a shortcut way of accessing **Class or Structure’s collection.**
- Subscript is a feature that enables classes / structures’ to access their values in a shortcut way.

```swift
struct School {

	var students: [String] = ["Paige", "Sunghee", "Seunghyun"]

	subscript(index: Int) -> String {
		return students[index]
	}

}

let school: School = School()
print(school.students[0]) // Paige
print(school[1]) // Sunghee
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

Section 13, subscript

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
