---
{"dg-publish":true,"permalink":"/workspace/3-java/class-and-object-theory/","noteIcon":""}
---

### 📌 What is a Class?

A **class** is a **blueprint** or **template** used to define objects.  
It groups **data (variables)** and **behaviors (methods)** together in a structured way.

### 🧸 What is an Object?

An **object** is a **real instance** of a class — it occupies memory and can be used to access variables and methods defined in the class.

---

### 🔧 Example:

```java
class Pen {
    String color;
    String type; // ballpoint or gel

    public void write() {
        System.out.println("Writing something...");
    }
}
```

- `Pen` is a class.
    
- It has two variables: `color`, `type`.
    
- It has a method: `write()`.
    

You can now create an object:

```java
Pen pen1 = new Pen();      // Create an object
pen1.color = "blue";       // Assign value
pen1.type = "gel";         // Assign value
pen1.write();              // Output: Writing something...
```

### ✅ Summary:

|Concept|Description|
|---|---|
|Class|A user-defined type that acts as a blueprint for objects|
|Object|A real-world entity created from a class|
