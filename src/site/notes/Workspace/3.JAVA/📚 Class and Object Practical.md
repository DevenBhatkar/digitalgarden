---
{"dg-publish":true,"permalink":"/workspace/3-java/class-and-object-practical/","noteIcon":""}
---


### 🧱 Step 1: Create a Class

The class created in the practical is:

```java
class Student {
    int age;
    String name;

    public void printInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```

- `Student` is the class name.
    
- It has two variables:
    
    - `int age`
        
    - `String name`
        
- It has one method:
    
    - `printInfo()` which prints the student’s name and age.
        

---

### 🛠️ Step 2: Create the `main` Method

In a separate class or within the same file, the `main` method is written to create and use `Student` objects:

```java
public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();   // Creating object s1
        s1.age = 21;
        s1.name = "Navin";
        s1.printInfo();               // Output: Name: Navin, Age: 21

        Student s2 = new Student();   // Creating object s2
        s2.age = 25;
        s2.name = "Ravi";
        s2.printInfo();               // Output: Name: Ravi, Age: 25
    }
}
```

### ⚙️ Behind the Scenes:

- `Student s1 = new Student();`  
    This line:
    
    - Creates a **new object** (`s1`) of type `Student`.
        
    - Uses the `new` keyword to allocate memory.
        
    - Calls the **default constructor** (no arguments).
        
- `s1.age = 21;`  
    Assigns the value `21` to the `age` variable of object `s1`.
    
- `s1.printInfo();`  
    Calls the method to print student details.
    

---

### 📚 Key Points Covered:

- You can **create multiple objects** from the same class.
    
- Each object has its own copy of instance variables.
    
- The **method is shared**, but each object uses its own data.
    
- The `main` method is where execution begins, and it’s used to **create and use objects**.
    

---

### 🧾 Summary:

|Concept|Description|
|---|---|
|Class|Defines structure and behavior|
|Object|Real instance of the class|
|new|Allocates memory and calls constructor|
|. (dot operator)|Used to access members of a class|
|main()|Starting point of the program|