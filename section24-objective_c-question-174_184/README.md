# ObjectiveC 171 ~ 184

### 171) What id id?

**Answer:**

- Id is a generic datatype available in Objective-C. Id is capable of holding any kind of object but not primitive Datatype value.

### 172) \***\*What is the difference between id and Any?\*\***

**Answer:**

- Any variable is capable of holding primitives and Objects whereas id variable only holds objects.

### 173) What is @synthesize?

**Answer:**

- @synthesize tells to the compiler that the accessor methods (Setters and Getters) should be generated for the given variables.

### 174) What is the Top most or Root class in Objective-C?

**Answer:**

- **NSObject** is the Root class in Object-C.

### 175) What is Category?

**Answer:**

- Category is an alternate way to add new functionality without subclassing. The newly added functionality gets available to the all instances of this.

### 176) What is formal Protocol?

**Answer:**

- Protocol is a set of methods declaration.
- A **formal** protocol declares a list of methods that client classes are expected to implement.

### 177) What is informal Protocol?

**Answer:**

- Informal protocol is a Protocol which is the combination of Required and Optional Methods.

### 178) What is the difference between Objective-C Enum and Swift Enum?

**Answer:**

- Objective-C enum does not have raw and associated values.
- Swift enums can have methods.

### 179) Difference between #import and #include?

**Answer:**

- #import includes the files or frameworks only once
- #include includes the files or frameworks every time you compile

### 180) What is auto-release pool?

**Answer:**

- A chunk of memory dedicated for auto-released objects. Objects added to auto-release pool will be cleaned by the runtime system when the objects are of no use.

### 181) What is auto-release?

**Answer:**

- Auto-release is delayed release. When you call auto-release over an object, the object will be added to auto-release pool.

### 182) When do we use Auto-release on objects?

**Answer:**

- Use auto-release when you are not sure that when to release the object.
- The best usecase is when you are creating an object and sharing it with different parts of the program. Use autorelease while sharing so that when different parts of the program done using the object, the object will be released from the autorelease pool.

### 183) What are the property attributes available in Objective-C?

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

### 184) What is the difference between Copy and Weak?

**Answer:**

- Weak just shares the ownership without increasing the retain count.
- Copy entirely creates new object and sets the retain count as 1 for the newly created object.
