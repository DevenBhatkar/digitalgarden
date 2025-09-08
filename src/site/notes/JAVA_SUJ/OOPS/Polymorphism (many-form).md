---
{"dg-publish":true,"permalink":"/java-suj/oops/polymorphism-many-form/","noteIcon":""}
---


- An ability of an object to exibite more than one form is know as polymorphism 
- One name but different behaviors is known as polymorphism 
👉 **Example: A person in different roles**

- The **same person** can behave differently depending on the situation.
    
- At home → he is a **father/son**.
    
- At office → he is an **employee**.
    
- With friends → he is a **friend**.
    

So, **one person (same object) shows different behaviors (methods/roles)** depending on the context.  
That’s **Polymorphism = "many forms"**.


### Types of polymorphism 

### What is binding ?

- Binding means linking a method call to the actual method code.


#### 1.`Compile time `or `compile time binding` or `static binding`

- It can be achived using method overloding .
	- Constructor overload
	- variable shadowing
	- method shadowing
#### 2.*Runtime polymorphism* or *Runtime binding* or *Dynamic binding*

- Can be achived by method overriding  



## Compile time polymorphism 

- The binding happens during compile time is known as compile time polymorphism
- It can be achived using method overloading

### What is variable shadowing 

- A subclass and superclass is having static or non static variable with same name is known as variable shadowing - 
- Which variable to be called is decided during compile time, based on reference variable type
```java

```


### Method shadowing 

- A subclass and superclass is having static method with same name,access specifier,returntype,and formal argument is known as method shadowing 
- Which method to be called  is decided during compile time , based on reference variable type

```java
import java.util.Scanner;  
  
  
class Father  
{  
    public static void test()  
    {  
        System.out.println("Father class test method");  
    }  
    public static String demo(int a,int b)  
    {  
        int ans=a+b;  
        return "Father class demo mwthod :"+ans;  
    }  
}  
class Son extends Father  
{  
    public static void test()  
    {  
        System.out.println("Son class test method");  
    }  
    public static String demo(int a ,int b)  
    {  
        int ans =a+b;  
        return "Son class demo method :"+ ans;  
    }  
  
}  
  
public class Demo {  
    public static void main(String[] args)  
    {  
        Father ref1=new Father();  
        ref1.test();  
        System.out.println(ref1.demo(10,20));  
        System.out.println("------------------");  
        Son ref2=new Son();  
        ref2.test();  
        System.out.println(ref2.demo(20,30));  
        System.out.println("-----------------");  
  
  
        //upcasting  
       Father ref3=new Son();  
       ref3.test();  
        System.out.println(ref3.demo(30,40));  
        System.out.println("-----------------");  
  
        //downcasting  
  
        Son ref4=(Son)ref3;  
  
        ref4.test();  
  
        System.out.println(ref4.demo(10,20));  
  
        System.out.println("-------------------");  
    }  
}
```

### Output

```css
Father class test method
Father class demo mwthod :30
================
Son class test method
Son class demo method :50
===================
Father class test method
Father class demo mwthod :70
-----------------
Son class test method
Son class demo method :30
------------------------
```



### Runtime polymorphism 

- The binding happens during run time is known as runtime polymorphism
- It is achieved using *method Overinding*

### Method overiding 


- A subclass and super class is having non static method with same name ,access specifier ,return type and formal arguments is known as *method overrindng *
- Which method to be callled is decided during *runtime* based on object creation 
```java

import java.util.Scanner;  
  
  
class Father  
{  
    public  void test()  
    {  
        System.out.println("Father class test method");  
    }  
    public  String demo(int a,int b)  
    {  
        int ans=a+b;  
        return "Father class demo mwthod :"+ans;  
    }  
}  
class Son extends Father  
{  
    public  void test()  
    {  
        System.out.println("Son class test method");  
    }  
    public     String demo(int a ,int b)  
    {  
        int ans =a+b;  
        return "Son class demo method :"+ ans;  
    }  
  
}  
  
public class Demo {  
    public  void main(String[] args)  
    {  
        Father ref1=new Father();  
        ref1.test();  
        System.out.println(ref1.demo(10,20));  
        System.out.println("------------------");  
        Son ref2=new Son();  
        ref2.test();  
        System.out.println(ref2.demo(20,30));  
        System.out.println("-----------------");  
  
  
        //upcasting  
       Father ref3=new Son();  
       ref3.test();  
        System.out.println(ref3.demo(30,40));  
        System.out.println("-----------------");  
  
        //downcasting  
  
        Son ref4=(Son)ref3;  
  
        ref4.test();  
  
        System.out.println(ref4.demo(10,20));  
  
        System.out.println("-------------------");  
    }  
}
```

