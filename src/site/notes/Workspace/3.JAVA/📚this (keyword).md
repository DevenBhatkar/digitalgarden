---
{"dg-publish":true,"permalink":"/workspace/3-java/this-keyword/","noteIcon":""}
---

## ✅ **Understanding `this` keyword in Java**

### 🔹 When local and instance variables have the same name:

If a **non-static (instance) variable** and a **local variable** (inside a method) have the **same name**, and you reference the name directly inside a **non-static method**, the **local variable** takes precedence.

To refer to the instance variable instead, use the `this` keyword.

---

## 🔹 What is `this`?

- `this` is a **keyword** in Java.
    
- It is a **non-static reference variable**.
    
- It holds the **memory address of the current object**.
    
- It is **only accessible inside non-static contexts** (i.e., inside instance methods or constructors).
    

---

### 🧪 Example 1: Understanding `this` in non-static context
```java
class Rambo {
    public void test() {
        // Non-static context: belongs to the object
        System.out.println("test start");

        // Prints the current object's reference
        System.out.println("this: " + this);

        System.out.println("test end");
    }

    public static void main(String[] args) {
        // Static context: belongs to the class

        System.out.println("main start");

        // Creating 3 objects of Rambo
        Rambo ref1 = new Rambo();
        Rambo ref2 = new Rambo();
        Rambo ref3 = new Rambo();

        // Printing object references
        System.out.println("REF1: " + ref1);
        System.out.println("REF2: " + ref2);
        System.out.println("REF3: " + ref3);

        // Calling test() using ref2
        ref2.test();

        System.out.println("main end");
    }
}
```

##### 🔗OUTPUT

```css
main start
REF1 : Rambo@27716f4
REF2 : Rambo@8efb846
REF3 : Rambo@2a84aee7
test start
this :Rambo@8efb846
test end
main end 
```

### 🔹How to use non-static members inside non-static context?

1) **Directly**
2) **Using `this` keyword** (✅ recommended for clarity and to resolve ambiguity)

#### 🧪 Example 2: Accessing instance variables

```java
class Rambo {
    // Instance (non-static) variable
    int a = 10;

    public void test() {
        // Non-static method can access instance variables

        System.out.println("test start");

        // Accessing directly
        System.out.println("Directly: " + a);

        // Accessing using this keyword
        System.out.println("With 'this': " + this.a);

        System.out.println("test end");
    }

    public static void main(String[] args) {
        System.out.println("main start");

        // Creating object
        Rambo ref1 = new Rambo();

        // Calling instance method
        ref1.test();

        System.out.println("main end");
    }
}
```

### 🔗OUTPUT

```css
main start
test start
Directly: 10
With 'this': 10
test end
main end
```

## 🔹 How to use static members inside non-static context?

1. **Directly**
    
2. **Using Class Name** ✅ (recommended)
    
3. **Using `this` keyword** (allowed, but not preferred)

> ❗ While `this` can technically be used to access static members, it is discouraged because static members belong to the class, not to any particular object.

##### 🧪 Example 3: Accessing static variable from non-static context

```java
class Rambo {
    // Static (class-level) variable
    static int a = 10;

    public void test() {
        // Non-static method accessing static members

        System.out.println("test start");

        // Accessing directly
        System.out.println("Directly: " + a);

        // Accessing using class name (✅ preferred)
        System.out.println("With ClassName: " + Rambo.a);

        // Accessing using this (⚠️ not preferred)
        System.out.println("With 'this': " + this.a); // Works, but avoid it

        System.out.println("test end");
    }

    public static void main(String[] args) {
        System.out.println("main start");

        // Creating object
        Rambo ref1 = new Rambo();

        // Calling instance method
        ref1.test();

        System.out.println("main end");
    }
}
```

### 🔗 Output

```css
main start
test start
Directly: 10
With ClassName: 10
With 'this': 10
test end
main end
```


---

### 🔍 Summary

|Context|Accessing Instance Variable|Accessing Static Variable|
|---|---|---|
|Non-static method|✅ Directly  <br>✅ `this.variable`|✅ Directly  <br>✅ `ClassName.variable`  <br>⚠️ `this.variable` (not preferred)|
|Static method|❌ Can't access directly  <br>❌ `this` not allowed|✅ Directly  <br>✅ `ClassName.variable`
