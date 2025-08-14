---
{"dg-publish":true,"permalink":"/workspace/3-java/fundamental-of-oop/","noteIcon":""}
---

###  1. Static Member

A **member** (variable/method/block) that is declared in the class area with the **`static`** keyword is called a **static member**.

#### 🔹 Static Variable
 
- Declared inside the **class area** (also called **global area**).
    
- Prefixed with `static` keyword.
    
- It's a type of **global variable**.
    
- Stored in **class static area** (memory space for static members).
    
- Class static area is **named after the class**.
    
- Can be accessed directly in static context.
    

> 💡 Static method block is also called **static context**.

#### 🔸 Example:

```java
class Demo {
    static int a;

    public static void main(String[] args) {
        // static context -> class static area
        System.out.println("Main Start");
        System.out.println(a);      // prints default value 0
        System.out.println("main end");
    }
}
```

![Pasted image 20250724115829.png](/img/user/img/Pasted%20image%2020250724115829.png)
### 2. Global Variable

A **variable** declared inside the **class/global area** is called a **global variable**.

#### 🔹 Types of Global Variables:

- `static` variable
    
- `non-static` variable
    

#### 🔹 Properties:

- **Assigned default values automatically** (even if not initialized).
    
- Cannot declare **two global variables with the same name**.
    

#### 🔸 Default Values of Global Variables:

|Data Type|Default Value|
|---|---|
|byte|0|
|short|0|
|int|0|
|long|0L|
|float|0.0f|
|double|0.0|
|char|'\u0000' (blank)|
|boolean|false|
|String|null|
#### 🔸 Example 1 (Duplicate global variable – ❌ error):

```java
class Demo  
{  
  
    // class area or Global Area  
    static int a=10;//global variable  
    static int a=25;// Compile time error variable a is already defined  
    static String a="harsh";// Compile time error variable a is already defined  
    public static void main(String[] args) {  
        // static context -> Class static area  
        System.out.println("Main Start");  
        System.out.println(a);  
        System.out.println("main end");  
  
  
    }  
}
```

🔸 Example 2 (Using global variables inside global and local areas):
```java
class Demo {
    static int a = 10;    // global variable
    static int b = a;     // using one global variable inside another

    public static void main(String[] args) {
        System.out.println("Main Start");
        System.out.println(a);   // 10
        System.out.println(b);   // 10
        int c = a;               // using global variable inside method (local)
        System.out.println(c);   // 10
        System.out.println("main end");
    }
}
```
✅ Output:
```css
Main Start
10
10
10
main end
```

### 3. Static Method

A **method** declared inside the class area with the `static` keyword is called a **static method**.

#### 🔹 Properties:

- Can be called without creating an object.
    
- Belongs to the **class**, not to instances.
    
- If there’s a **local variable** and a **static variable** with the same name, the **local variable takes priority** inside static context.
    
- To access static variable in such a case, use `ClassName.variable`.

🔸 Example:
```java  
class Demo {
    static int a = 10;

    public static void main(String[] args) {
        System.out.println("Main Start");
        System.out.println(a);        // static variable a = 10
        int a = 25;                   // local variable (shadows static a)
        System.out.println(a);        // prints 25 (local variable)
        System.out.println(Demo.a);   // prints 10 (static variable using class name)
        System.out.println("main end");
    }
}
```

✅ Output:
```css
Main Start
10
25
10
main end
```

### 4. Static Block

A **block** of code declared with `static { ... }` inside the class is called a **static block** or **static initializer block**.

#### 🔹 Properties:

- Runs **only once** when the class is loaded (before `main()` method).
    
- It has:
    
    - No name
        
    - No return type
        
    - No access modifier
        
    - No arguments
        
- Cannot be called explicitly.
    
- Used to run logic that **must execute before `main()`**, or during class loading.
#### Why do we need static block ? 

-  To execute some set of statement mandatory after class loading process.
- To execute some set of statement mandatory before execution of main method

Example 1:
```java
class Demo {
    static {
        System.out.println("Welcome to Instagram"); // executes before main()
    }

    public static void main(String[] args) {
        System.out.println("Main Start");
        reels();
        System.out.println("main end");
    }

    public static void reels() {
        System.out.println("reels start");
        System.out.println("reels end");
    }
}
```

✅ Output:
```css
Welcome to Instagram
Main Start
reels start
reels end
main end
```

🔸 Example 2 (Multiple Classes & Static Blocks):

```java
class Demo {
    static {
        System.out.println("Welcome to Demo");
    }

    public static void main(String[] args) {
        System.out.println("Main Start");
        Demo2.deven();  // calling static method from another class
        System.out.println("main end");
    }

    public static void reels() {
        System.out.println("reels start");
        System.out.println("reels end");
    }
}

class Demo2 {
    static {
        System.out.println("Welcome to Demo2 class");
    }

    public static void deven() {
        System.out.println("hi");
        System.out.println("bye");
    }
}
```

✅ Output:
```css
Welcome to Demo
Main Start
Welcome to Demo2 class
hi
bye
main end
```


### ✅ Final Notes:

- To use static methods or variables of **another class**, use `ClassName.memberName`.
    
- You can create **multiple classes in one Java file**.
    
- You can create a class **without a `main()` method**, but it can’t be executed directly.
    
- Static block is useful to write code that must run **before main method** or once during class load.
