---
{"dg-publish":true,"permalink":"/java-suj/oops/types-of-inheritance/","noteIcon":""}
---


1) Single level Inheritance
2) multilevel inheritance
3) heararical inheritance
4) multiple inheritance
5) Hybrid Inhertitance

![Pasted image 20250818122329.png|500](/img/user/Pasted%20image%2020250818122329.png)


### Single level inheritance

- One subclass is having only one super class is know as single level inheritance

### Multi level inheritance

- A subclass is having more than one super class at different level is known as *multi-level inheritance*

### Example:

```java
public class Demo {  
    public static void main(String[] args)   
    {  
        Son s=new Son();  
  
        System.out.println(s.grandMoney);  
        System.out.println(s.fatherMoney);
        System.out.println(s.sonMoney);   
    }  
}  
  
class Grandfather  
{  
    int grandMoney=1000;  
}  
  
class Father extends Grandfather  
{  
    int fatherMoney=1000;  
}  
  
class Son extends Father  
{  
    int sonMoney;  
}
```

### Output

```css
1000
1000
0
```


### Herarical inheritance

- One super class is having more than one subclass at same level is know as *herarical inheritance*

### Example:

```java
public class Demo {  
    public static void main(String[] args)  
    {  
        Father f= new Father();  
        System.out.println(f.fatherMoney);  
  
        Son s=new Son();  
        System.out.println(s.sonMoney);  
  
        Daughter d= new Daughter();  
        System.out.println(d.daughterMoney);  
  
          
  
  
    }  
}  
  
class Father  
{  
    int fatherMoney=1000;  
}  
  
class Son extends Father  
{  
    int sonMoney;  
}  
class Daughter extends Father  
{  
    int daughterMoney;  
}
```

### Output

```css
1000
0
0
```

