---
{"dg-publish":true,"permalink":"/workspace/3-java/object-class-dg/hash-code/","noteIcon":""}
---


 - It is present inside Object class
 - hashCode() return unique integer value for Object
 - Return type of hashCode() is *int*
### Example:
```java
public class Demo {  
    public static void main(String[] args) {  
  
        Demo ref=new Demo();  
        System.out.println(ref.hashCode());  
        System.out.println(Integer.toHexString(ref.hashCode()));  
        System.out.println(ref.getClass());  
        System.out.println(ref.getClass());  
        System.out.println(ref.getClass().getName());  
        System.out.println(ref.toString());  
        //internal working of toString() Method  
        System.out.println(ref.getClass().getName()+"@"+Integer.toHexString(ref.hashCode()));  
  
    }  
  
}
```

### Output

```css
1791741888
6acbcfc0
class Demo
class Demo 
Demo
Demo@6acbcfc0
Demo@6acbcfc0
```