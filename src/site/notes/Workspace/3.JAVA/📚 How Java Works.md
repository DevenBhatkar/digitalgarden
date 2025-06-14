---
{"dg-publish":true,"permalink":"/workspace/3-java/how-java-works/","noteIcon":""}
---

### 🧠 The Execution Flow

1. **JVM (Java Virtual Machine)**  
    Every machine — Windows, macOS, Linux — can have **JVM** installed.
    
    > JVM is the reason **Java is platform-independent** (Write Once, Run Anywhere).
    
2. But, JVM **doesn't understand Java code directly**.  
    So we cannot just write `.java` files and expect JVM to run them as-is.
    
3. **Compiler (`javac`) is needed**
    
    - Java code you write (`.java`) must be **compiled** into something the JVM understands — this is called **bytecode**.
        
    - This compiled code is saved in a `.class` file.
        
    - JVM reads and executes this **bytecode**, not your `.java` code.

### 🧱 The Layered Architecture

Here’s how things are stacked up on your machine:

![Pasted image 20250613190429.png](/img/user/Pasted%20image%2020250613190429.png)

- JVM is specific to the OS.  
    Example: A Windows JVM won’t run on macOS, and vice versa.
    
- So while **Java code is platform-independent**, **JVM is platform-dependent**.

### 🔁 Compilation Process

When you write Java code:

```java
System.out.println("Hello World");
```

You must:

1. **Compile it** using:
```
javac hello.java
```
- This creates a `hello.class` file — **bytecode**.
    
- **Run it** using:
```
java hello
```

> JVM runs `hello.class` and executes the program.

---

### 🧾 Summary Flow:

1. **You (the programmer)** write Java code (`.java`).
    
2. **Compiler (`javac`)** converts it to bytecode (`.class`).
    
3. **JVM** executes the bytecode.
    
4. **JVM needs to know which file to start with**, and that file must have a **`main` method**.
    
5. Execution begins from the `main` method.
    

---

### 🧩 Main Method is Mandatory

JVM **requires** the file you run to contain:
```java
public static void main(String[] args)
```
This is the **starting point** of the program.

[[Workspace/3.JAVA/📚 Variables in Java.\|next]]