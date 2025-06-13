---
{"dg-publish":true,"permalink":"/workspace/3-java/hello-world/","noteIcon":""}
---

### 👨‍💻 Step 1: Writing Java Code in a File

Initially tried this inside `hello.java`:
```java
System.out.println("Hello World");
```


❌ **This gives an error** when you try to compile it using:

```bash
javac hello.java
```
---

### 🧠 Why the Error?

Java code must follow a **structure**:

- Java uses the **JVM**, which **doesn't run `.java` files directly**.
    
- You must **compile `.java` files** using `javac` to generate **bytecode (`.class` file)**.
    
- That bytecode runs on the **JVM** using the `java` command.
    

---

### 🏗️ Step 4: Proper Structure of Java Code

```java
class hello {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

#### 🧱 Explanation:

|Part|Meaning|
|---|---|
|`class hello`|Every Java program must be in a class. The name can be anything.|
|`public static void main(String[] args)`|Java looks for this method as the **starting point** of your program.|
|`System.out.println("Hello World");`|Prints `Hello World` to the console.|
|`;`|Semicolon ends a statement in Java.|
|`{}`|Used to define blocks.|

---

### 🧪 Step 5: Compile and Run

#### ✅ To compile:

```java
javac hello.java
```

This creates: `hello.class`

#### ▶️ To run:

```
java hello
```

**Output:**

```
Hello World
```
---

### 🧾 Behind the Scenes (Simplified)

Your Code (.java)
   ⬇️ javac
Bytecode (.class)
   ⬇️ java
JVM Executes

---

### 🔁 Summary: Tools Involved

|Tool|Full Form|Purpose|
|---|---|---|
|JVM|Java Virtual Machine|Runs `.class` (bytecode)|
|JRE|Java Runtime Environment|Contains JVM + libraries|
|JDK|Java Development Kit|Contains JRE + Compiler (`javac`)|

> 💡 You install **JDK** as a developer.  
> To **run** Java programs on another machine, just **JRE** is enough.