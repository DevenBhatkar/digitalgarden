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
  
    System.out.println(indian_Hotel);  
      
      
    List<String>china=new ArrayList<>();  
      
    china.add("Triple rice");  
    china.add("EggRice");  
    china.add("soup");  
    china.add("ChopperRice");  
  
    System.out.println("China :"+china);  
  
    indian_Hotel.addAll(4,china);  
      
    indian_Hotel.remove("Jalebi Fafda");  
  
        System.out.println(indian_Hotel);  
          
          
        indian_Hotel.removeAll(gj);  
  
        System.out.println(indian_Hotel);  
          
      
          
          
  
    }  
  
}
```

### Output

```css
Mh :[vadapav, modak, Misal pav, Puran Poli]
UP :[Litti choka, malaiyo, Tomato Chatt, Champaran]
TN :[idli, Dosa, vada, Chutney]
GJ :[Dhokla, undhiu, Jalebi Fafda, Locho]
[Dhokla, undhiu, Jalebi Fafda, Locho, vadapav, modak, Misal pav, Puran Poli, idli, Dosa, vada, Chutney, Litti choka, malaiyo, Tomato Chatt, Champaran]
China :[Triple rice, EggRice, soup, ChopperRice]
[Dhokla, undhiu, Locho, Triple rice, EggRice, soup, ChopperRice, vadapav, modak, Misal pav, Puran Poli, idli, Dosa, vada, Chutney, Litti choka, malaiyo, Tomato Chatt, Champaran]
[Triple rice, EggRice, soup, ChopperRice, vadapav, modak, Misal pav, Puran Poli, idli, Dosa, vada, Chutney, Litti choka, malaiyo, Tomato Chatt, Champaran]
```


