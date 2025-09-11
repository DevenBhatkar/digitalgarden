---
{"dg-publish":true,"permalink":"/workspace/3-java/collection-dg/for-each/","noteIcon":""}
---

-  It is used to iterate over all the elements of Collection or Array.
- It has 2 segments Each segment is seperated using `:` 
- In 2nd segment we pass reference variable of collection or Array
- In 1st segment we create a variable based on reference variable 
- We cannot stop for-Each loop, Because it does not have condition.
- We cannot perform insertion and deletion operation using for-Each loop
- If we try to perform insertion and deletion operation than it will throw `ConcurrentModificationException`

```java
for(datatype variable:Reference of collection or array)
{
	statement
}
```



### Example :

```java
import java.util.ArrayList;  
import java.util.List;  
import java.util.Objects;  
  
public class Demo {  
    public static void main(String[] args)  
    {  
        List a1 =new ArrayList();  
  
        a1.add(10);  
        a1.add(12.2);  
        a1.add('a');  
        a1.add("qsp");  
        a1.add(false);  
        a1.add(null);  
        a1.add(12.2);  
  
        System.out.println(a1);  
  
  
        for (Object obj: a1 )  
        {  
            a1.add(10);//this will throw `ConcurrentModificationException`  
            a1.remove(10);//this will throw `ConcurrentModificationException`  
        }  
  
    }  
}
```

### Difference between for and for-each

|Feature|`for` loop|`for-each` loop|
|---|---|---|
|**Index access**|Available|Not available|
|**Modification**|Can update elements via index|Cannot reassign elements (but can modify object fields)|
|**Traversal control**|Full (forward, backward, skip steps)|Sequential only (forward)|
|**Readability**|Slightly verbose|Cleaner, simpler|
|**Use case**|When you need index or updates|When you only need to read|

### Difference between for-each and iterator

|Feature|For-each loop|Iterator|
|---|---|---|
|**Read elements**|Yes|Yes|
|**Remove elements**|❌ Not possible safely|✅ Possible using `remove()`|
|**Access index**|❌ No|❌ No (need ListIterator for index)|
|**Code simplicity**|Very simple|More verbose|
|**Use case**|Reading elements|Removing elements during traversal, or finer control|