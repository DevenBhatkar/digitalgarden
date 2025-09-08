---
{"dg-publish":true,"permalink":"/workspace/3-java/object-class-dg/equals/","noteIcon":""}
---


- It is used to compare address of 2 object 
- Returntype is boolean 
- To compare data of to Object rather then comparing address of 

### Write a java program to compare data rather than address

```java
public class Demo extends Object {  
  
    int id;  
    String name;  
  
    public Demo(int id,String name)  
    {  
        this.id=id;  
        this.name=name;  
    }  
  
  
  
    @Override  
    public boolean equals(Object obj)  
    {  
        Demo ref =(Demo)obj;  
        return  this.id== ref.id && this.name== ref.name;  
    }  
  
    public static void main(String[] args)  
    {  
  
        Demo ref1=new Demo(1,"deeven");  
        Demo ref2=new Demo(1,"even");  
  
        System.out.println(ref1.equals(ref2));  
    }  
  
}
```

### output

```css
true
```