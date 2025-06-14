---
{"dg-publish":true,"permalink":"/workspace/3-java/ternary-operator-in-java/","noteIcon":""}
---

### 📌 What is it?

The **ternary operator** is a **shortcut** for writing simple `if-else` conditions in **one line**.

---

### 🧪 Syntax:
```java
condition ? value_if_true : value_if_false;
```
✅ Example :

```java
int age = 18;
String result = (age >= 18) ? "You can vote" : "You cannot vote";
System.out.println(result);
```
> If `age >= 18` is true → result = `"You can vote"`  
> If false → result = `"You cannot vote"`

---

### 🧠 Summary:

- Ternary = short form of [[📚If Else in Java|`if-else`]]
    
- Saves space, makes simple conditions concise
    
- Best for assigning values, not complex logic
[[Workspace/3.JAVA/📚Switch Statement in Java\|next]]
