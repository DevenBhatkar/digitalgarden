---
{"dg-publish":true,"permalink":"/workspace/3-java/collection-dg/iterator/","noteIcon":""}
---


- It is a `Cursor` , to activate iterator cursor in collection we have iterator method 
- Return type of iterator method is `iterator interface` 
- With the help of iterator we can access `next()`,`hasNext()`,`remove()'
- hasNext() is used to check weather the next element is present or not 
- next() is used to return next element of iteration 
- it will throw `NoSuchElementException` if next element is not present
- remove() is used to remove the element , return type of remove() is void


```java
import java.util.ArrayList;  
import java.util.Arrays;  
import java.util.Iterator;  
import java.util.List;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
        List <Integer> list=new ArrayList<>(Arrays.asList(10,15,13,14));  
  
  
        System.out.println(list);  
  
  
        Iterator<Integer> al = list.iterator();  
        System.out.println(list.iterator().hasNext());  
        
        System.out.println(al.next());  
        System.out.println(al.next());  
        System.out.println(al.next());  
        System.out.println(al.next());  
          
  
  
    }  
}
```


### all the elements of list using iterator method

```java
import java.util.ArrayList;  
import java.util.Arrays;  
import java.util.Iterator;  
import java.util.List;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
        List <Integer> list=new ArrayList<>(Arrays.asList(10,15,13,14));  
  
        Iterator<Integer> al = list.iterator();  
  
  
      while (al.hasNext())  
      {  
          System.out.println(al.next());  
      }  
  
    }  
}
```


### 

```java
import java.util.ArrayList;  
import java.util.Arrays;  
import java.util.Iterator;  
import java.util.List;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
        List <Integer> list=new ArrayList<>(Arrays.asList(10,15,13,14));  
  
        Iterator<Integer> al = list.iterator();  
  
  
      while (al.hasNext())  
      {  
//          al.remove();this will give Exception  
          System.out.println(al.next());  
          al.remove();  
          System.out.println(list);  
      }  
  
    }  
}
```





