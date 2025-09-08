---
{"dg-publish":true,"permalink":"/workspace/3-java/collection-dg/array-introduction/","noteIcon":""}
---


#### What is Array?

- It is a continuos block of memory used to store homogeneos type of data. 
- To access the element of array we use *index* 
- *index value* starts from `0`till `n-1`
- where  n is `length of array`
- To find length of array we have length variable 
- if we try to cross index of array we get `ArrayindexOutofBound` exception 
- Array is fixed in size
- Array can store default values 

#### How to create an array ?

- Using array literals 
- When we know the values of array then we'll use this syntax 👇

```css
datatype [] variable ={value1,value2};
```

- Using new keyword
- When we don't know the values of array but we know the size of array then we'll use this syntax 👇
```css
datatype [] variable=new datatypes[size]
```


```java
public class Demo{  
  
    public static void main(String[] args)   
    {  
        String [] name ={"ravi","magesh","Bhavesh","kiran"};  
        System.out.println(name);//this will print address  
        System.out.println(name[0]);  
        System.out.println(name[1]);  
        System.out.println(name[2]);  
//        System.out.println(name[7]);///this give arrayoutbound  
        System.out.println(name.length);//this will print the length  
                  
String[]a=new String[];  
  
        System.out.println(a);  
        System.out.println(a[1]);//this will print default value if no vlaue added  
        System.out.println(a[2]);  
             
    }  
  
} 
```

### Output

```css
[Ljava.lang.String;@6acbcfc0
ravi
magesh
Bhavesh
4
[Ljava.lang.String;@5f184fc6
null
null

```


### write a program to print all 

```java
import java.util.Arrays;  
  
//Write a java program to print all the elements of array  
public class Demo{  
  
    public static void main(String[] args)  
    {  
        String [] name ={"ravi","magesh","Bhavesh","kiran"};  
  
  
        for (int i = 0; i < name.length; i++)  
        {  
            System.out.println(name[i]);  
        }  
  
        System.out.println();  
        System.out.println("==============");  
        for (String i:name)  
        {  
            System.out.println(i);  
        }  
        System.out.println();  
        System.out.println("==============");  
        System.out.println(Arrays.toString(name));  
    }  
  
}
```

### Output

```java
ravi
magesh
Bhavesh
kiran

==============
ravi
magesh
Bhavesh
kiran

==============
[ravi, magesh, Bhavesh, kiran]
```

### Disadvantage of arrray

- It is fixed in size 
- Can only store homogenes type of data
- Not good for insertion and deletion 
- Lack of inbuilt functionality