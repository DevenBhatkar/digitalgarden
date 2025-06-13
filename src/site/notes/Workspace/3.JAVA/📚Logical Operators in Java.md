---
{"dg-publish":true,"permalink":"/workspace/3-java/logical-operators-in-java/","noteIcon":""}
---

### 📌 What are Logical Operators?

Logical operators are used to **combine multiple conditions** and return a **boolean result** (`true` or `false`).

---

### 🔹 Operators explained:

|Operator|Name|Meaning|
|---|---|---|
|`&&`|Logical AND|True **only if both** conditions are true|
|`||`|
|`!`|Logical NOT|Reverses the boolean value (true ↔ false)|

---

### 🧪 Examples :
```java
int a = 5;
int b = 6;

// AND (&&)
System.out.println(a < b && b < 10);  // true && true = true
System.out.println(a > b && b < 10);  // false && true = false

// OR (||)
System.out.println(a > b || b < 10);  // false || true = true

// NOT (!)
System.out.println(!(a < b));         // !(true) = false
```
### ⚠️ Use in Conditions:

Logical operators are usually used in `if` statements, loops, and complex decisions:
```java
if (age >= 18 && citizen == true) {
    // Eligible to vote
}
```
### ✅ Summary

- Use **`&&`** when **all conditions must be true**
    
- Use **`||`** when **any condition can be true**
    
- Use **`!`** to **negate** a condition

[[Workspace/3.JAVA/📚If Else in Java\|next]]