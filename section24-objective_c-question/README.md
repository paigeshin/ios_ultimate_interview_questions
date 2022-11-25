# ObjectiveC 1 ~ 14

### 1) What is id?

**Answer:**

- Id is a generic datatype available in Objective-C. Id is capable of holding any kind of object but not primitive Datatype value.

### 2) What is the difference between id and Any?

**Answer:**

- Any variable is capable of holding primitives and Objects whereas id variable only holds objects.

### 3) What is @synthesize?

**Answer:**

- @synthesize tells to the compiler that the accessor methods (Setters and Getters) should be generated for the given variables.

### 4) What is the Top most or Root class in Objective-C?

**Answer:**

- **NSObject** is the Root class in Object-C.

### 5) What is Category?

**Answer:**

- Category is an alternate way to add new functionality without subclassing. The newly added functionality gets available to the all instances of this.

### 6) What is formal Protocol?

**Answer:**

- Protocol is a set of methods declaration.
- A **formal** protocol declares a list of methods that client classes are expected to implement.

### 7) What is informal Protocol?

**Answer:**

- Informal protocol is a Protocol which is the combination of Required and Optional Methods.

### 8) What is the difference between Objective-C Enum and Swift Enum?

**Answer:**

- Objective-C enum does not have raw and associated values.
- Swift enums can have methods.

### 9) Difference between #import and #include?

**Answer:**

- #import includes the files or frameworks only once
- #include includes the files or frameworks every time you compile

### 10) What is auto-release pool?

**Answer:**

- A chunk of memory dedicated for auto-released objects. Objects added to auto-release pool will be cleaned by the runtime system when the objects are of no use.

### 11) What is auto-release?

**Answer:**

- Auto-release is delayed release. When you call auto-release over an object, the object will be added to auto-release pool.

### 12) When do we use Auto-release on objects?

**Answer:**

- Use auto-release when you are not sure that when to release the object.
- The best usecase is when you are creating an object and sharing it with different parts of the program. Use autorelease while sharing so that when different parts of the program done using the object, the object will be released from the autorelease pool.

### 13) What are the property attributes available in Objective-C?

**Answer:**

- retain / strong
- weak
- assign
- readwrite
- readonly
- copy
- setter=
- getter=
- atomic
- nonatomic

### 14) What is the difference between Copy and Weak?

**Answer:**

- Weak just shares the ownership without increasing the retain count.
- Copy entirely creates new object and sets the retain count as 1 for the newly created object.

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

[Section 21, KVO and KVC](./section21-kvo_kvc-question/)

[Section 22, Exception Handling](./section22-exeception_handling-question/)

[Section 23, Framework](./section23-framework-question/)

Section 24, Objective-C
