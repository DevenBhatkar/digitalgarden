---
{"dg-publish":true,"permalink":"/workspace/3-java/object-class-dg/to-string/","noteIcon":""}
---

- It is present inside Object class
- It will return address of an object in string format 
- Whenever we are trying to print address of an object internally , It will call toString() of object class
### Example:
```java
public class Demo
{
	public static void main (String []args)
	{
		Demo ref=new Demo();
		sout("implicitly :"+ref);
		sout("Explicitly :"+ref.toString());
	}
}
```

### Output
```css
implicitly :Demo@6acbcfc0
Explicitly :Demo@6acbcfc0
```

why do we need to override toString()?
> 	To print data of an object rather then printing address of an object

### Example:

```java
public class Demo {  
    int id;  
    String name;  
  
    Demo(int id, String name) {  
        this.id = id;  
        this.name = name;  
    }  
  
    // Overriding toString()  
    @Override  
    public String toString() {  
        return "Demo[id=" + id + ", name=" + name + "]";  
    }  
  
    public static void main(String[] args) {  
        Demo ref=new Demo(10,"deven");  
        System.out.println(ref);  
    }  
}
```

### Output

```css
public class Demo {  
    int id;  
    String name;  
  
    Demo(int id, String name) {  
        this.id = id;  
        this.name = name;  
    }  
  
    // Overriding toString()  
    @Override  
    public String toString() {  
        return "Demo[id=" + id + ", name=" + name + "]";  
    }  
  
    public static void main(String[] args) {  
        Demo ref=new Demo(10,"deven");  
        System.out.println(ref);  
    }  
}
```



