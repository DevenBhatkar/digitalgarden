---
{"dg-publish":true,"permalink":"/workspace/3-java/type-conversion-in-java/","noteIcon":""}
---

### 📌 What is Type Conversion?

Type conversion means **changing the type of a value** from one data type to another.

---

### 🔹 Two Types of Type Conversion:

#### 1. **Implicit Conversion (Widening)**

- Happens **automatically**
    
- When converting from a **smaller type to a larger type** (e.g., `byte → int`)
    
- ✅ No data loss

```java
byte b = 12;
int a = b;  // Implicit conversion (widening)
```
#### 2. **Explicit Conversion (Narrowing)**

- Done **manually using casting**
    
- When converting from a **larger type to a smaller type** (e.g., `int → byte`)
    
- ❌ May cause **data loss**
```java
int a = 256;
byte b = (byte) a;  // Explicit conversion (narrowing)
```
If the value of `a` is out of `byte`'s range, data will be lost.

---

### 🧠 Key Notes

- You **cannot change the type of a variable**, but you can **assign values between different types** using conversion.
    
- Implicit conversion is **safe**, explicit conversion **needs caution**.
    
- Java compiler **stops you** from narrowing unless you use explicit casting.

[[Workspace/3.JAVA/📚Logical Operators in Java\|next]]