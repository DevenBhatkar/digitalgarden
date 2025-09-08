---
{"dg-publish":true,"permalink":"/java-suj/oops/inheritance/","noteIcon":""}
---

**Definition:**  
Inheritance is the process by which a **child class acquires all the states (fields) and behaviors (methods)** of a parent class.  
It is also called an **“is-a” relationship**.
### **How to Achieve Inheritance?**

- **`extends` keyword** → for class-to-class inheritance.
    
- **`implements` keyword** → for interface-to-class implementation.
#### Example without inheritance

```java
class Dhirubhai {
    String paisa = "Andha paisa....";
    String company = "Reliance";

    public void speak() {
        System.out.println("Paisa bolta hai.....");
    }

    public void thinking() {
        System.out.println("Jaaha soch waha paisa....");
    }
}

class Mukesh {
    // Empty class - no fields or methods inherited from Dhirubhai
}

public class Driver {
    public static void main(String[] args) {
        Mukesh m = new Mukesh();

        // ❌ These lines will cause errors because Mukesh has no such members
        System.out.println(m.company); 
        System.out.println(m.paisa);

        m.speak();
        m.thinking();
    }
}
```

#### output 

```css
java: cannot find symbol
  symbol:   variable company
  location: variable m of type Mukesh

**Reason:**  
Since `Mukesh` does not inherit from `Dhirubhai`, it cannot access its fields or methods.
```

#### Example with Inheritance

```java
class Dhirubhai {
    String paisa = "Andha paisa....";
    String company = "Reliance";

    public void speak() {
        System.out.println("Paisa bolta hai.....");
    }

    public void think() {
        System.out.println("Jaaha soch waha paisa....");
    }
}

// 'extends' means Mukesh inherits from Dhirubhai
class Mukesh extends Dhirubhai {
    // Empty class, but it inherits all fields & methods from Dhirubhai
}

public class Driver {
    public static void main(String[] args) {
        Mukesh m = new Mukesh();

        // Accessing inherited fields
        System.out.println(m.company);
        System.out.println(m.paisa);

        // Accessing inherited methods
        m.speak();
        m.think();
    }
}
```

#### output 

```css
reliance
Andha paisa....
paisa bolta hai.....
Jaaha soch waha paisa....
```


>NOTE 💡: 
>Parent class is also known as `super class` or `base class`
>Child class is `sub class` or `derived`  

## **Can We Inherit Static Members?**

✅ Yes.  
**Rule:**  
When loading classes:

1. **Superclass static members** load first.
    
2. Then **Subclass static members** load.

#### Example 

```java
class Dhirubhai {
    static int a = 10;

    public static void test() {
        System.out.println("Parent class static member");
    }

    static {
        System.out.println("Parent class SIB");
    }
}

class Mukesh extends Dhirubhai {
    static int b = 20;

    public static void demo() {
        System.out.println("Child static");
    }
}

public class Driver {
    public static void main(String[] args) {
        System.out.println("Main Start");

        // Creating object triggers class loading
        Mukesh ref = new Mukesh();

        // Accessing inherited static and subclass static members
        System.out.println(ref.a); // from parent
        System.out.println(ref.b); // from child
        ref.test(); // parent static method
        ref.demo(); // child static method

        System.out.println("Main end");
    }
}
```

#### output

```css
Main Start
Parent class SIB
10
20
Parent class static member
Child static 
Main end
```
## **Can We Inherit Non-Static Members?**

✅ Yes.  
**Object Loading Order:**

1. **`Object` class** (topmost superclass) loads first.
    
2. **Superclass non-static members** load.
    
3. **Subclass non-static members** load.
    

This happens due to **constructor chaining** using the `super` calling statement (Java automatically calls the superclass constructor before executing the subclass constructor).
### Object class


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/java-suj/oops/object-class/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




**Definition:**+

- The *Object class* is the *supermost*class for all Java classes.
    
- If any class does not explicitly extend another class, it **implicitly extends `Object`.
    

**Location:**

- Present in the *java.lang* package.
    
- The `Object` class constructor **does not** have a `super()` calling statement (because it has no superclass).

### **Super Calling Statement**

- A **constructor calling statement** used to call the constructor of the **superclass**.
    
- Must be the **first statement** inside any constructor.
    
- Cannot use `super()` and `this()` in the **same constructor**.
    
- If the programmer does not write a `super()` statement, the compiler will automatically insert a *no-argument `super()` call*.

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

## *`this()`* vs *`super()`*

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
    
3. *`super()`* is inserted by the compiler automatically if not written.

</div></div>


### 
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




1) Single level Inheritance
2) multilevel inheritance
3) heararical inheritance
4) multiple inheritance
5) Hybrid Inhertitance

![Pasted image 20250818122329.png|500](/img/user/Pasted%20image%2020250818122329.png)


### Single level inheritance

- One subclass is having only one super class is know as single level inheritance

### Multi level inheritance

- A subclass is having more than one super class at different level is known as *multi-level inheritance*

### Example:

```java
public class Demo {  
    public static void main(String[] args)   
    {  
        Son s=new Son();  
  
        System.out.println(s.grandMoney);  
        System.out.println(s.fatherMoney);
        System.out.println(s.sonMoney);   
    }  
}  
  
class Grandfather  
{  
    int grandMoney=1000;  
}  
  
class Father extends Grandfather  
{  
    int fatherMoney=1000;  
}  
  
class Son extends Father  
{  
    int sonMoney;  
}
```

### Output

```css
1000
1000
0
```


### Herarical inheritance

- One super class is having more than one subclass at same level is know as *herarical inheritance*

### Example:

```java
public class Demo {  
    public static void main(String[] args)  
    {  
        Father f= new Father();  
        System.out.println(f.fatherMoney);  
  
        Son s=new Son();  
        System.out.println(s.sonMoney);  
  
        Daughter d= new Daughter();  
        System.out.println(d.daughterMoney);  
  
          
  
  
    }  
}  
  
class Father  
{  
    int fatherMoney=1000;  
}  
  
class Son extends Father  
{  
    int sonMoney;  
}  
class Daughter extends Father  
{  
    int daughterMoney;  
}
```

### Output

```css
1000
0
0
```



</div></div>

