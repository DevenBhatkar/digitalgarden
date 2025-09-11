---
{"dg-publish":true,"permalink":"/workspace/3-java/collection-dg/list/characteristic-of-list/","noteIcon":""}
---


- It can store hetrogenious type of `data` or `objects`
- It is growable in type 
- It is dynamic in size 
- It has Index
- It maintains insertion order
- It can store duplicate object 
- It can store null object 
- Random access is allowed 


### Example: Using different method in one program

```java
import java.util.ArrayList;  
import java.util.List;  
  
public class Demo{  
  
    public static void main(String[] args)  
    {  
  
    List<String>mh=new ArrayList<>();  
    mh.add("vadapav");  
    mh.add("modak");  
    mh.add("Misal pav");  
    mh.add("Puran Poli");  
    System.out.println("Mh :"+mh);  
  
    List<String>up=new ArrayList<>();  
    up.add("Litti choka");  
    up.add("malaiyo");  
    up.add("Tomato Chatt");  
    up.add("Champaran");  
    System.out.println("UP :"+up);  
  
    List<String>tn=new ArrayList<>();  
  
    tn.add("idli");  
    tn.add("Dosa");  
    tn.add("vada");  
    tn.add("Chutney");  
    System.out.println("TN :"+tn);  
  
    List<String>gj=new ArrayList<>();  
  
    gj.add("Dhokla");  
    gj.add("undhiu");  
    gj.add("Jalebi Fafda");  
    gj.add("Locho");  
  
    System.out.println("GJ :"+gj);  
  
    List<String>indian_Hotel=new ArrayList<>();  
  
  
    indian_Hotel.addAll(gj);  
    indian_Hotel.addAll(mh);  
    indian_Hotel.addAll(tn);  
    indian_Hotel.addAll(up);  
  
        System.out.println("Indian Hotel"+indian_Hotel);  
  
  
    List<String>china=new ArrayList<>();  
  
    china.add("Triple rice");  
    china.add("EggRice");  
    china.add("soup");  
    china.add("ChopperRice");  
  
    System.out.println("China :"+china);  
  
    indian_Hotel.addAll(4,china);  
  
    indian_Hotel.remove("Jalebi Fafda");  
  
        System.out.println("Indian Hotel"+indian_Hotel);  
  
  
        indian_Hotel.removeAll(gj);  
  
        System.out.println(indian_Hotel);  
  
  
        indian_Hotel.clear();  
  
        System.out.println("Indian Hotel :"+indian_Hotel);  
  
  
  
  
    }  
  
}
```

### Output: 

```css
Mh :[vadapav, modak, Misal pav, Puran Poli]
UP :[Litti choka, malaiyo, Tomato Chatt, Champaran]
TN :[idli, Dosa, vada, Chutney]
GJ :[Dhokla, undhiu, Jalebi Fafda, Locho]
Indian Hotel[Dhokla, undhiu, Jalebi Fafda, Locho, vadapav, modak, Misal pav, Puran Poli, idli, Dosa, vada, Chutney, Litti choka, malaiyo, Tomato Chatt, Champaran]
China :[Triple rice, EggRice, soup, ChopperRice]
Indian Hotel[Dhokla, undhiu, Locho, Triple rice, EggRice, soup, ChopperRice, vadapav, modak, Misal pav, Puran Poli, idli, Dosa, vada, Chutney, Litti choka, malaiyo, Tomato Chatt, Champaran]
[Triple rice, EggRice, soup, ChopperRice, vadapav, modak, Misal pav, Puran Poli, idli, Dosa, vada, Chutney, Litti choka, malaiyo, Tomato Chatt, Champaran]
Indian Hotel :[]
```




### Write a  java program to add given object in arraylist and print them one by one using arraylist


```java
import java.util.ArrayList;  
import java.util.List;  
  
public class Demo {  
  
    public static void main(String[] args) {  
  
  
        List<Character> obj=new ArrayList<>();  
  
        obj.add('a');  
        obj.add('z');  
        obj.add('b');  
        obj.add('f');  
        obj.add('d');  
        obj.add('e');  
        obj.add('g');  
        obj.add('m');  
        obj.add('n');  
  
  
        for (int i = 0; i < obj.size(); i++)  
        {  
            System.out.print(obj.get(i));  
            System.out.print(" ");  
        }  
  
    }  
}
```

### Output

```css
a z b f d e g m n 
```


### Write a  program to remove odd number 


```java
import java.util.*;  
public class Demo {  
  
    public static void main(String[] args)  
    {  
        List<Integer>list=new ArrayList<>();  
  
       list.add(10);  
       list.add(15);  
       list.add(17);  
       list.add(14);  
       list.add(12);  
       list.add(12);  
       list.add(19);  
       list.add(13);  
       list.add(14);  
  
        for (int i = 0; i < list.size(); i++) {  
  
            if (list.get(i)%2 !=0)  
            {  
                list.remove(i);  
                i--;  
            }  
  
        }  
        System.out.println(list);  
    }  
}

// In this program we done decrement cause when we remove a number the index change since the size of ArrayList in dynamic
```



### Write a java program to add all the elements of String Array into list

```java
import java.util.ArrayList;  
  
public class Demo {  
  
    public static void main(String[] args)  
    {  
     String []names={"Deven","Ravi","Suraj","Devansh"};  
  
        ArrayList<String>list=new ArrayList<>();  
  
        for (String i:names)  
        {  
            list.add(i);  
        }  
  
        System.out.println(list);  
  
  
    }  
}
```


### How to store hetro type of data in array

```java

import java.util.Arrays;  
  
public class Demo {  
    public static void main(String[] args) {  
        Object[] arr = new Object[5];  
  
        arr[0] = 10;  
        arr[1] = "Deven";  
        arr[2] = 1.1;  
        arr[3] = true;  
        arr[4] = 'a';  
  
        System.out.println(Arrays.toString(arr));  
  
    }  
}
```

### Write a Java program that performs the following operations on an ArrayList of Strings:
- Create an ArrayList named cities.
- Add the following city names to the list: "Delhi", "Mumbai", "Chennai", "Kolkata".
- Insert the city "Bangalore" at index 2.
- Display all the cities in the list.
- Check whether the city "Mumbai" exists in the list and print a message:
	If found, print: "Mumbai is present in the list."
	Otherwise, print: "Mumbai is not present in the list."
- Sort the list of cities in alphabetical order and display the sorted list.
- Clear the list and print the final size of the ArrayList.


```java
import java.util.ArrayList;  
import java.util.Arrays;  
import java.util.Collections;  
import java.util.List;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
        List<String>cities=new ArrayList<>();  
  
        cities.add("Delhi");  
        cities.add("Mumbai");  
        cities.add("Chennai");  
        cities.add("Kolkata");  
  
        cities.add(2,"Bangalore");  
  
        System.out.println(cities);  
  
        String city="Mumbai";  
        if(cities.contains(city))  
        {  
            System.out.println(city+" is present in the list");  
        }  
        else  
        {  
            System.out.println(city+" is not present in the list");  
        }  
  
        System.out.println("--------------------");  
        System.out.println();  
        Collections.sort(cities);  
  
        System.out.println("Sorted List");  
  
        System.out.println(cities);  
  
        cities.clear();  
        System.out.println(cities.size());  
  
  
  
    }  
}
```

### Output

```css
[Delhi, Mumbai, Bangalore, Chennai, Kolkata]
Mumbai is present in the list
--------------------

Sorted List
[Bangalore, Chennai, Delhi, Kolkata, Mumbai]
0
```


### Write a Java program that performs the following using an ArrayList of integers:
- Add the following numbers to the list: 10, 5, 20, 15, 25.
- Insert the number 12 at index 2.
- Print all elements of the list.
- Check if the number 15 exists in the list and print an appropriate message.
- Sort the list in ascending order.
- Remove the number 5 from the list.
- Print the final list and its size.

```java
import java.util.ArrayList;  
import java.util.Arrays;  
import java.util.Collections;  
import java.util.List;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
        List<Integer>list=new ArrayList<>();  
  
        list.add(10);  
        list.add(5);  
        list.add(20);  
        list.add(15);  
        list.add(25);  
  
        System.out.println(list);  
        System.out.println();  
        list.add(2,12);  
        System.out.println(list);  
  
        int number=15;  
        if (list.contains(number))  
        {  
            System.out.println(number+" exists in the list");  
        }  
        else  
        {  
            System.out.println(number+" does not exists in the list");  
        }  
  
        Collections.sort(list);  
        System.out.println();  
  
        System.out.println("Sorted list is");  
        System.out.println(list);  
  
  
        list.remove(Integer.valueOf(5));  
  
  
  
        System.out.println(list);  
  
        System.out.println("And its size is "+ list.size());  

    }  
}
```

### OUTPUT

```css
[10, 5, 20, 15, 25]

[10, 5, 12, 20, 15, 25]
15 exists in the list

Sorted list is
[5, 10, 12, 15, 20, 25]
[10, 12, 15, 20, 25]
And its size is 5
```

### You are given a Java program that defines two classes: Employee and Company.
- The Employee class has attributes for employee ID, name, and salary. It also contains a static method to create new Employee objects and a method to display employee details.
- The Company class maintains a list of employees and displays their details.

```java
import java.util.ArrayList;  
import java.util.List;  
  
public class Employees  
{  
    int empId;  
    String name;  
    double salary;  
  
    public Employees(int id,String name,double salary)  
    {  
        this.empId=id;  
        this.name=name;  
        this.salary=salary;  
    }  
  
  
    public static Employees createEmployee(int empId, String name, double salary)  
    {  
        return new Employees(empId, name, salary);  
    }  
    public void showDetails()  
    {  
        System.out.println(empId);  
        System.out.println(name);  
        System.out.println(salary);  
    }  
}  
  
class Company  
{  
  
  
  
    public static void main(String[] args) {  
  
        List <Employees>emp=new ArrayList<>();  
  
        emp.add(Employees.createEmployee(123,"deven",20000.0));  
        emp.add(Employees.createEmployee(234,"sujal",30000.0));  
        emp.add(Employees.createEmployee(235,"sutal",60000.0));  
  
  
        for (int i = 0; i <emp.size() ; i++)  
        {  
            emp.get(i).showDetails();  
            System.out.println("+++++++++++");  
        }  
  
    }  
     
}
```


### Output

```css
123
deven
20000.0
+++++++++++
234
sujal
30000.0
+++++++++++
235
sutal
60000.0
+++++++++++

```


### Write a program to sort given list in asending and desc


```java
import java.util.*;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
  
        List <Integer>list=new ArrayList<>(Arrays.asList(22,3,4,2,32,23,34465,567,56));  
  
        Collections.sort(list);  
        System.out.println("Asd "+list);  
  
        Collections.reverse(list);  
  
        System.out.println("DESC "+list);  
  
  
    }  
}
```

### OUTPUT

```css
Asd [2, 3, 4, 22, 23, 32, 56, 567, 34465]
DESC [34465, 567, 56, 32, 23, 22, 4, 3, 2]
```


>If we try to perform sorting operation on Hetrogeneous type of data we'll get `ClassCastException`, as for it depends on the first type of data


>set method is used to update the value at specific index


```java
import java.util.*;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
  
        List <Integer>list=new ArrayList<>(Arrays.asList(1,2,3,4,5));  
  
        list.set(1,3);  
  
        System.out.println(list);  
  
    }  
}
```

### Output

```css
[1, 3, 3, 4, 5]
```