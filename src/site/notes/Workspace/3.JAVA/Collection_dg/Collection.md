---
{"dg-publish":true,"permalink":"/workspace/3-java/collection-dg/collection/","noteIcon":""}
---


- A group of object present inside another object in known as Collection 
- It has many inbuilt classes and interface 

### Collection framework

- It is a set of classes and interfaces which provides a to perform `CRUD` Operation , searching operation and sorting operation on group of object 
### Collection hierarchy  

![Pasted image 20250908143529.png](/img/user/Pasted%20image%2020250908143529.png)

- Iterable is the supermost interface in collection hierarchy
- Collection is a sub interface of iterable interface
- Collection interface has 3 sub-interfaces such as list , set , queue
- List interface has 3 implimenting classses such as ArrayList linkedlist and vector
- Stack is a subclass of vector 
- Set interface has 3 implementing classes -Hashset,LinkedHashset,TreeSet
- Queue interface has 2 implementing classes - `Priority Queue`,
>With the help of LinkedList Collection can achieve multiple inheritance


### Important method in each

1) To add an object
- add(Object)
- addAll(Collection)
- add(int index,object)
- add(int index,collection)

2) To remove objects
- remove(object)
- remove(int index)
- removeAll(Collection)
- clear()

3) To search objects
- contains(object)
- containAll(collection)


4) To access objects
- get(int index)
- iterator()
- listIterator()
- for each loop

5) other methods
- size() 


### Types of collection 

1) Generic 
	- Use to store fixed type of data
2) Non Generic
	- used to store Hetrogeneous type of data

```java
import java.util.ArrayList;  
import java.util.Arrays;  
import java.util.HashSet;  
import java.util.Set;  
  
//Write a java program to print all the elements of array  
public class Demo{  
  
    public static void main(String[] args)  
    {  
        int [] n ={12,13,12,13,15,16,17,18,19};  
  
        Set<Integer> x=new HashSet<>();  
  
  
        int num=0;  
        for (int i = 0; i <n.length ; i++)  
        {  
            int count=0;  
            for (int j = 1; j < n[i]; j++)  
            {  
                if(n[i]%j==0)  
                {  
                    count++;  
                }  
  
            }  
            if(count<=2)  
            {  
  
  
                x.add(n[i]);  
            }  
  
        }  
  
  
     int as=0;  
        for (int i:x)  
        {  
            as++;  
        }  
  
        System.out.println(x);  
        System.out.println();  
        System.out.println("There are "+as+" Prime numbers in array");  
  
  
  
  
    }  
  
}
```

