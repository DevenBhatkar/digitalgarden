---
{"dg-publish":true,"permalink":"/workspace/3-java/oops-1/object-class/","noteIcon":""}
---

**Definition:**

- The **`Object` class** is the **supermost class** for all Java classes.
    
- If any class does not explicitly extend another class, it **implicitly extends `Object`**.
    

**Location:**

- Present in the **`java.lang`** package.
    
- The `Object` class constructor **does not** have a `super()` calling statement (because it has no superclass).

### **Super Calling Statement**

- A **constructor calling statement** used to call the constructor of the **superclass**.
    
- Must be the **first statement** inside any constructor.
    
- Cannot use `super()` and `this()` in the **same constructor**.
    
- If the programmer does not write a `super()` statement, the compiler will automatically insert a **no-argument `super()` call**.

```java
class DhiruBhai {
    int a;
    int b;

    // Constructor with parameters
    public DhiruBhai(int a, int b) {
        this.a = a; // Assign local variable a to instance variable a
        this.b = b; // Assign local variable b to instance variable b
    }
}

// Child class
class Mukesh extends DhiruBhai {

    // Constructor in child class
    public Mukesh(int a, int b) {
        super(a, b); // Calls parent constructor with arguments
    }
}

public class Driver {
    public static void main(String[] args) {
        System.out.println("Main Start");

        // Creating object of Mukesh calls parent constructor first
        Mukesh m1 = new Mukesh(10, 20);

        // Accessing inherited fields
        System.out.println(m1.a);
        System.out.println(m1.b);

        System.out.println("Main End");
    }
}
```

### output

```css
Main Start
10
20
Main End
```

## **`this()` vs `super()`**

|Feature|`this()`|`super()`|
|---|---|---|
|**Purpose**|Calls another constructor of the **same class**|Calls constructor of the **superclass**|
|**Calling**|Must be called **explicitly**|Called **implicitly** if not written|
|**Position**|Must be first statement in the constructor|Must be first statement in the constructor|
|**Can coexist in same constructor?**|❌ No|❌ No|
|**Effect on PLI and IIB**|If `this()` is used, that constructor does **not** have Parameterized Loading Instance blocks (PLI) and Instance Initialization Blocks (IIB)|Superclass initialization still happens when using `super()`|

**Key Points to Remember:**

1. Every Java class **directly or indirectly** inherits from `Object`.
    
2. Constructor chaining **always starts from the topmost parent class**.
    
3. **`super()`** is inserted by the compiler automatically if not written.