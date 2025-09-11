---
{"dg-publish":true,"permalink":"/workspace/3-java/collection-dg/wrappers/","noteIcon":""}
---


- For every datatype we have  a wrapper class 
1) Byte
2) Short
3) Integer
4) Float
5) Double
6) Character
7) String
8) Boolean

	- Wrapper classes are used to convert primitive datatype to object & vice versa
	- We can perform `Boxing` and `Unboxing` with it.


### Boxing 

- The conversion of primitive datatype to non primitive datatype is known boxing 

### Unboxing 

- The conversion of non- primitive datatype to primitive datatype is known as unboxing 



### Example :
```java
  
public class Demo {  
  
    public static void main(String[] args) {  
        Integer a=10;  
        int i =a;  
        System.out.println("Implicit Unboxing :"+ i);  
  
        int j=a.intValue();  
        System.out.println("Explicit Unboxing :"+ j);  
    }  
}
```

### output 

```css
Implicit Unboxing :10
Explicit Unboxing :10
```


| Situation                | What to use                    |
| ------------------------ | ------------------------------ |
| `double → int`           | **Typecast** `(int)d`          |
| `"123" → Integer object` | `Integer.valueOf("123")`       |
| `"123" → int`            | `Integer.parseInt("123")`      |
| `Integer object → int`   | `intValue()`(or auto-unboxing) |
