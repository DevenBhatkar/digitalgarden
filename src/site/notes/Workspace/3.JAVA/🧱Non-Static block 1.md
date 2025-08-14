---
{"dg-publish":true,"permalink":"/workspace/3-java/non-static-block-1/","noteIcon":""}
---

## 🧱 **Non-Static Block in Java**

### 🔹 What is a non-static block?

- A **non-static block** is a block of code **declared inside a class** (in the class area) **without the `static` keyword**.
    
- It is also called an **instance initializer block**.
    
- It runs **every time an object of the class is created**, **before the constructor**.

```java
{
    // Non-static block
}
```

### ❓ **Why do we need non-static blocks?**

We use non-static blocks to:

- Execute a set of statements **every time an object is created**.
    
- Avoid repeating code in multiple constructors.
    
- Initialize instance variables or run logic common to all constructors.
### 🧪 Example 1: Basic non-static block execution

```java
class Demo {
    // Non-static block: will run every time a new object is created
    {
        System.out.println("---New Object Created---");
    }

    public static void main(String[] args) {
        System.out.println("Main Start");

        // Creating a new object, so non-static block executes
        Demo d = new Demo();

        System.out.println("Main End");
    }
}
```

### 🔗 Output

```css
Main Start
---New Object Created---
Main End
```

>🔎 **Note:** The block runs **before the constructor**, even though there’s no constructor defined explicitly — the default constructor is used.
### 🧪 Example 2: Multiple classes with non-static blocks

```java
class Demo {
    // Non-static block in Demo class
    {
        System.out.println("---New Object Created---");
    }

    public static void main(String[] args) {
        System.out.println("Main Start");

        // Creating object of class Harsh
        Harsh ref = new Harsh();

        // Calling non-static method
        ref.test();

        System.out.println("Main End");
    }
}

class Harsh {
    // Non-static block in Harsh class
    {
        System.out.println("Hello Harsh class object");
    }

    public void test() {
        System.out.println("hii test");
        System.out.println("Bye test");
    }
}
```

### Output

```css
Main End
Hello Harsh class object
hii test
Bye test
Main End
```

---

## ✅ Summary:

| Feature                  | Non-static Block                                                     |
| ------------------------ | -------------------------------------------------------------------- |
| Declared in class area   | ✅ Yes                                                                |
| Uses `static` keyword    | ❌ No                                                                 |
| Runs when?               | Every time an object is created                                      |
| Runs before constructor? | ✅ Yes                                                                |
| Purpose                  | To run setup code for all constructors / object initialization logic |
