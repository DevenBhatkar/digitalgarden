---
{"dg-publish":true,"permalink":"/workspace/3-java/constructor-chaining/","noteIcon":""}
---

### What is Constructor Chaining?

Constructor chaining is the process in which **one constructor calls another constructor** in the same class or superclass. It helps avoid code duplication and promotes better code reuse.

---

## 🔧 How to Achieve Constructor Chaining

Constructor chaining can be achieved using:

1. `this()` calling statement — for calling a constructor from the **same class**
    
2. `super()` calling statement — for calling a constructor from the **superclass**
    

---

## 1️⃣ `this()` Calling Statement

- It is used to call another constructor in the **same class**
    
- It **must be the first statement** inside the constructor
    
- A constructor can contain **only one** `this()` call
    
- If a class has `n` constructors, we can write **maximum `n-1` `this()` calls**
    
- If a constructor has `this()`, it **cannot have PLI (parameterless instance initializer)** or **IIB (instance initialization block)**
    
- **Constructor recursion** is not allowed (because it would lead to an infinite loop of constructor calls)
    

---

## ✅ Example 1
```java
class Student {
    int id;
    String name;
    double per;

    // Default constructor
    public Student() {
        this.id = 0;
        this.name = "Unknown";
        this.per = 0.0;
    }

    // Constructor with 1 parameter
    public Student(int id) {
        this();               // Calls default constructor
        this.id = id;         // Then assigns id
    }

    // Constructor with 2 parameters
    public Student(int id, String name) {
        this(id);             // Calls constructor with 1 parameter
        this.name = name;     // Then assigns name
    }

    // Constructor with 3 parameters
    public Student(int id, String name, double per) {
        this(id, name);       // Calls constructor with 2 parameters
        this.per = per;       // Then assigns percentage
    }

    // Method to print student details
    public void printDetails() {
        System.out.println("id : " + this.id);
        System.out.println("name : " + this.name);
        System.out.println("percentage : " + this.per);
    }

    // Instance Initialization Block (IIB)
    {
        System.out.println("New Object Created");
    }

    public static void main(String[] args) {
        Student s1 = new Student(1, "harsh", 84.79);
        s1.printDetails();
    }
}
```

#### OUTPUT

```css
New Object Created
id : 1
name : harsh
percentage : 84.79
```

### Example 2:

```java
class Laptop {
    String brand;
    int ramsize;
    double price;

    public Laptop() {
        this.brand = " ";
        this.ramsize = 0;
        this.price = 0.0;
    }

    public Laptop(String brand) {
        this();              // Calls default constructor
        this.brand = brand;
    }

    public Laptop(String brand, int ramsize) {
        this(brand);         // Calls constructor with 1 parameter
        this.ramsize = ramsize;
    }

    public Laptop(String brand, int ramsize, double price) {
        this(brand, ramsize); // Calls constructor with 2 parameters
        this.price = price;
    }

    public void printDetails() {
        System.out.println("brand : " + this.brand);
        System.out.println("ramsize : " + this.ramsize);
        System.out.println("price : " + this.price);
    }

    public static void main(String[] args) {
        Laptop l1 = new Laptop("acer", 16, 50000.0);
        l1.printDetails();
    }
}
```

#### OUTPUT

```css
brand : acer
ramsize : 16
price : 50000.0
```

#### ✅ Example 3 (No Chaining, Just Constructor)

```java
class Employee {
    int id;
    String name;
    double sal;

    public Employee(int id, String name, double sal) {
        this.id = id;
        this.name = name;
        this.sal = sal;
    }

    public static void printDetails(Employee emp) {
        System.out.println("id : " + emp.id);
        System.out.println("name : " + emp.name);
        System.out.println("salary : " + emp.sal);
    }

    public static void main(String[] args) {
        Employee e1 = new Employee(101, "deven", 25555);
        Employee e2 = new Employee(102, "deven2", 25554);
        Employee e3 = new Employee(103, "deven3", 25553);
        Employee e4 = new Employee(104, "deven4", 25552);

        printDetails(e1);
        printDetails(e2);
        printDetails(e3);
        printDetails(e4);
    }
}
```

#### OUTPUT

```java
id : 101
name : deven
salary : 25555.0
id : 102
name : deven2
salary : 25554.0
id : 103
name : deven3
salary : 25553.0
id : 104
name : deven4
salary : 25552.0
```

