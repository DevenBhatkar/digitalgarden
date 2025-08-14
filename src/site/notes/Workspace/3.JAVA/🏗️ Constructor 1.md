---
{"dg-publish":true,"permalink":"/workspace/3-java/constructor-1/","noteIcon":""}
---

## 🏗️ **Constructors in Java**

### 🔹 What is a Constructor?

- A **constructor** is a **non-static** special method in Java.
    
- Its **name is exactly the same as the class name**.
    
- It **does not have any return type**, not even `void`.
    
- A constructor is called **automatically** when an object is created.
    
- Every constructor consists of:
    
    1. Constructor Calling Statement
        
    2. PIL (Pre-Loading Instruction)
        
    3. IIB (Instance Initializer Block)
        
    4. UWS (User Written Statements)
        

---

### ❓ **Do all classes have a constructor?**

Yes.  
If a programmer **does not explicitly write** a constructor, the Java **compiler provides a default constructor** (no-argument constructor) during compilation.
### 🧪 Example 1: Constructor + Instance Initializer Block (IIB)

```java
class Rambo {
    // Instance Initializer Block (IIB)
    {
        System.out.println("I am IIB");
    }

    // No-argument constructor
    public Rambo() {
        // UWS (User Written Statement)
        System.out.println("I am Constructor");
    }

    public static void main(String[] args) {
        System.out.println("Main Start");

        // Creating an object → IIB runs first, then constructor
        Rambo ref = new Rambo();

        System.out.println("Main End");
    }
}
```


### 🔗 Output:

```css
Main Start
I am IIB
I am Constructor 
Main End
```

## 🧱 **Types of Constructors**

1. **Default Constructor**  
    Automatically provided by compiler if no constructor is written.
    
2. **No-Argument Constructor**  
    A constructor with **no parameters**, written explicitly by the programmer.
    
3. **Parameterized Constructor**  
    A constructor with one or more parameters.
    

---

### 🧪 Example 2: Parameterized Constructor

```java
class Rambo {
    // Parameterized constructor
    public Rambo(int a) {
        System.out.println("parameterized constructor");
    }

    public static void main(String[] args) {
        System.out.println("main start");

        // Object creation with an argument
        Rambo ref = new Rambo(10);

        System.out.println("main end");
    }
}
```

#### Output
```css
main start
parameterized constructor
main end
```


### ❓ Why use Parameterized Constructors?

- To **initialize non-static variables** during object creation.

### 🧪 Example 3: Initializing Student object with constructor
```java
class Student {
    int id;
    String name;

    // Parameterized constructor
    public Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public void printDetails() {
        System.out.println("id: " + this.id);
        System.out.println("name: " + this.name);
    }

    public static void main(String[] args) {
        Student s1 = new Student(1, "harsh");
        Student s2 = new Student(2, "ravi");
        Student s3 = new Student(3, "yogesh");

        s1.printDetails();
        s2.printDetails();
        s3.printDetails();
    }
}
```

#### Output

```css
id : 1
name : harsh
id : 2
name : ravi
id : 3
name : yogesh
```

### 🧪 Error Example: Missing matching constructor

```java
class Rambo {
    public Rambo(int a) {
        System.out.println("parameterized Constructor");
    }

    {
        System.out.println("New Object Created");
    }

    public static void main(String[] args) {
        System.out.println("Main Start");

        Rambo ref = new Rambo(10);   // ✅ valid
        Rambo obj = new Rambo();     // ❌ error: no constructor with 0 args

        System.out.println("main end");
    }
}
```

#### 🔻 Error Message:

```css
java: constructor Rambo in class Rambo cannot be applied to given types;
  required: int
  found:    no arguments
  reason: actual and formal argument lists differ in length
```

### ✅ Fix: Add no-arg constructor

```java
class Rambo {
    public Rambo(int a) {
        System.out.println("parameterized Constructor");
    }

    // Added no-arg constructor
    public Rambo() {
        System.out.println("New Object Created");
    }

    public static void main(String[] args) {
        System.out.println("Main Start");

        Rambo ref = new Rambo(10);  // uses parameterized constructor
        Rambo obj = new Rambo();    // uses no-arg constructor

        System.out.println("main end");
    }
}

```

### Constructor Overloading

A class is have more the one constructor with same name but different formal argument, either they are differ in length or datatype is called Constructor overloading 

- we use constructor overloading new object of one class with different parameters
#### ### 🧪 Example 1: Constructor Overloading with Different Types

```java
class Instagram {
    public Instagram(String email) {
        // Constructor 1
    }

    public Instagram(long contactNo) {
        // Constructor 2
    }

    // IIB runs for every object
    {
        System.out.println("New Object Created");
    }

    public static void main(String[] args) {
        System.out.println("Main Start");

        Instagram obj1 = new Instagram("QsP@gmail.com");
        Instagram obj2 = new Instagram(4597612357L);

        System.out.println("Main end");
    }
}
```

```css
Main Start
New Object Created
New Object Created
Main end
```

#### 🧪 Example 2: Overloading Based on Purpose

```java
class Rambo {
    String name;
    double percentage;

    // Various constructors for flexibility
    public Rambo(int id) {
        System.out.println("Constructor with id");
    }

    public Rambo() {
        System.out.println("New Object Created");
    }

    {
        System.out.println("New obj Created");  // IIB
    }

    public static void main(String[] args) {
        System.out.println("Main Start");

        Rambo ref = new Rambo(10);
        Rambo obj = new Rambo();

        System.out.println("main end");
    }
}

```

#### 🔗 Output: 
```css
Main Start
New obj Created
parameterized Constructor
New obj Created
New Object Created
main end
```
### WAJP to create Student class consist of 3 variable such as int id ,
String name, double percentage,//
create no argument constructor to initialize default values ,//
create one formal agument constructor to initialize id , //
create one formal argument constructor to initialize name, //
create 1 formal arguement constructor to initialize percentage, //
create 2 formal arguement constructor to create id and name ,//
create 2 formal argument constructor , id and percentage , //
create 2 formal argument to initialize name and percentage,//
create 3 formal argument construstor to initialize id name and percentage, //
create object using each constructor ,
create non static method method to print details of all object , achive constructor 


```java
class Student {
    int id;
    String name;
    double per;

    // Multiple constructors

    public Student() {
        id = 3;
        name = "deven";
        per = 88.8;
    }

    public Student(int id) {
        this.id = id;
    }

    public Student(String name) {
        this.name = name;
    }

    public Student(double per) {
        this.per = per;
    }

    public Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public Student(int id, double per) {
        this.id = id;
        this.per = per;
    }

    public Student(String name, double per) {
        this.name = name;
        this.per = per;
    }

    public Student(int id, String name, double per) {
        this.id = id;
        this.name = name;
        this.per = per;
    }

    // Non-static method to print object details
    public void printDetails() {
        System.out.println("id : " + id);
        System.out.println("name : " + name);
        System.out.println("per : " + per);
    }

    public static void main(String[] args) {
        Student s1 = new Student(123);
        Student s2 = new Student(123, "deven");
        Student s3 = new Student(123, "deven", 34.45);
        Student s4 = new Student("deven", 34.45);
        Student s5 = new Student(34.45);
        Student s6 = new Student("name");
        Student s7 = new Student(123, 89.5);

        s1.printDetails();
        s2.printDetails();
        s3.printDetails();
        s4.printDetails();
        s5.printDetails();
        s6.printDetails();
        s7.printDetails();
    }
}
```

```css
id : 123
name : 123
per : 123
id : 123
name : 123
per : 123
id : 123
name : 123
per : 123
id : 0
name : 0
per : 0
id : 0
name : 0
per : 0
id : 0
name : 0
per : 0
id : 123
name : 123
per : 123
```

>> ⚠️ **Note:** For constructors with missing arguments, default values are used:

- `int` → 0
    
- `String` → null
    
- `double` → 0.0
