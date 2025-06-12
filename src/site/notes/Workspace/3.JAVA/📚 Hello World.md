---
{"dg-publish":true,"permalink":"/workspace/3-java/hello-world/","noteIcon":""}
---

### 👨‍💻 Step 1: Writing Java Code in a File

Initially tried this inside `hello.java`:
![Pasted image 20250612151334.png](/img/user/Pasted%20image%2020250612151334.png)


❌ **This gives an error** when you try to compile it using:

![Pasted image 20250612151422.png](/img/user/Pasted%20image%2020250612151422.png)
---

### 🧠 Why the Error?

Java code must follow a **structure**:

- Java uses the **JVM**, which **doesn't run `.java` files directly**.
    
- You must **compile `.java` files** using `javac` to generate **bytecode (`.class` file)**.
    
- That bytecode runs on the **JVM** using the `java` command.
    

---

### 🏗️ Step 4: Proper Structure of Java Code

![Pasted image 20250612151457.png](/img/user/Pasted%20image%2020250612151457.png)

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

![Pasted image 20250612151519.png](/img/user/Pasted%20image%2020250612151519.png)

This creates: `hello.class`

#### ▶️ To run:

![Pasted image 20250612151552.png](/img/user/Pasted%20image%2020250612151552.png)

**Output:**

![Pasted image 20250612151612.png](/img/user/Pasted%20image%2020250612151612.png)
---

### 🧾 Behind the Scenes (Simplified)

![Pasted image 20250612151638.png](/img/user/Pasted%20image%2020250612151638.png)

---

### 🔁 Summary: Tools Involved

|Tool|Full Form|Purpose|
|---|---|---|
|JVM|Java Virtual Machine|Runs `.class` (bytecode)|
|JRE|Java Runtime Environment|Contains JVM + libraries|
|JDK|Java Development Kit|Contains JRE + Compiler (`javac`)|

> 💡 You install **JDK** as a developer.  
> To **run** Java programs on another machine, just **JRE** is enough.