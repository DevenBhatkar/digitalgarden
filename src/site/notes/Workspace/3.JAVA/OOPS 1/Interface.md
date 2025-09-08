---
{"dg-publish":true,"permalink":"/workspace/3-java/oops-1/interface/","noteIcon":""}
---



### Type of Interface

1) Normal
- A interface which can contain one or more than one abstract method in known as , normal or regular interface
2) Marker Interface
- A interface which does not have any abstract method
3) Functional Interface
- A interface which has only one abstract method in known functional interface
- For functional interface we use *@functionalInterface* Annotation
- Runnable is a functional interface which has *run()* 


```java
//Write a java program to achive hybrid inheritance  
  
interface GrandFather  
{  
    int gf=10;  
}  
interface GrandMother  
{  
    int gm=20;  
}  
  
class Father implements GrandFather,GrandMother  
{  
    int f=30;  
}  
class Son extends Father  
{  
    int s=40;  
}  
class Daughter extends Father  
{  
    int d=50;  
}  
  
public class Demo {  
    public static void main(String[] args)  
    {  
       GrandFather grandFather =new Son();  
        System.out.println(grandFather.gf);  
          
        GrandMother grandMother=new Daughter();  
  
        System.out.println(grandMother.gm);  
          
          
  
  
    }  
}
```



