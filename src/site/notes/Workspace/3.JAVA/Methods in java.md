---
{"dg-publish":true,"permalink":"/workspace/3-java/methods-in-java/","noteIcon":""}
---

### 🧠 What are Methods in Java?

A **method** in Java is a block of code or a set of instructions used to perform a specific task.  
Methods are also referred to as **functions**.
### Key Components of a Method Declaration

- *Modifier:*  It specifies the method's access level (e.g., public, private, protected, or default).
- *Return Type*: The type of value returned, or void if no value is returned.
- *Method Name*: It follows Java naming conventions; it should start with a lowercase verb and use camel case for multiple words.
- **Parameters***: A list of input values (optional). Empty parentheses are used if no parameters are needed.
- ***Exception List***: The exceptions the method might throw (optional).
- **Method Body***: It contains the logic to be executed (optional in the case of abstract methods).

![methods_declaration.webp](/img/user/img/methods_declaration.webp)

### ✅ Rules for Creating a Method

- A method only runs when it is **called**.
    
- One method can be called **multiple times**.
    
- A class can contain **multiple methods**.
    
- You **cannot create a method inside another method**.
    
- Methods must be defined **inside a class** (not outside or nested inside another method).

### 💡 Example: Basic Method Usage

```java 
public class Demo {
    public static void main(String[] args) {
        System.out.println("Main Start");
        powerButton(); // calls powerButton method
        volumeButton(); // calls volumeButton method (calls powerButton inside)
        volumeButton(); // again calls volumeButton method
        System.out.println("Main End");
    }

    public static void powerButton() {
        System.out.println("Screen ON");
        System.out.println("Screen OFF");
    }

    public static void volumeButton() {
        System.out.println("Volume up");
        powerButton(); // calls powerButton inside volumeButton
        System.out.println("Volume down");
    }
}
/*
**Output Explanation:**

- `volumeButton()` internally calls `powerButton()` so for each call to volume, screen also turns ON and OFF.
*/
```


```java
public class Demo {
    public static void main(String[] args) {
        System.out.println("Main Start");         // Step 1
        powerButton();                            // Step 2: Calls powerButton() method
        volumeButton();                           // Step 3: Calls volumeButton() method
        volumeButton();                           // Step 4: Again calls volumeButton()
        System.out.println("Main End");           // Step 5
    }

    public static void powerButton() {
        System.out.println("Screen ON");          // This runs when powerButton is called
        System.out.println("Screen OFF");
    }

    public static void volumeButton() {
        System.out.println("Volume up");          // Step A
        powerButton();                            // Step B: Nested call to powerButton from inside volumeButton
        System.out.println("Volume down");        // Step C
    }
}
/*
OUTPUT-

Main Start
Screen ON
Screen OFF
Volume up
Screen ON
Screen OFF
Volume down
Volume up
Screen ON
Screen OFF
Volume down
Main End

*/
```

### write  a java program to create calculator class consist of 4 methods 1) to add 4 variable 2)to substrat 3 variable 3) to multiple 3 vsrisble 4) to divide 2 variable

```java
import java.util.Scanner;
public class Demo {
    public static void main(String[] args) {
        add();        // calls add method
        sub();        // calls sub method
        multiple();   // calls multiple method
        division();   // calls division method
    }

    public static void add() {
        System.out.println("----ADD-----");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        int d = sc.nextInt();
        int sum = a + b + c + d;
        System.out.println("Sum =" + sum);
    }

    public static void sub() {
        System.out.println("----SUB-----");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        int sub = a - b - c;
        System.out.println("Sub =" + sub);
    }

    public static void multiple() {
        System.out.println("----MULTIPLE-----");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        int pro = a * b * c;
        System.out.println("Product =" + pro);
    }

    public static void division() {
        System.out.println("----DIVISION-----");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int div = a / b;
        System.out.println("Result =" + div);
    }
}
```


### 📘 Types of Methods in Java

1. **No-argument (non-parameterized) methods**  
    Methods that do not take any input parameters.
```java
public static void add() {
    int a = 10, b = 20;
    System.out.println(a + b);
}
```
    
2. **Argument (parameterized) methods**  
    Methods that accept input arguments (values passed during the call).
```java
public static void add(int a, int b) {
    int sum = a + b;
    System.out.println(sum);
}
```
### 🧪 Example: No-Argument Method

```java
class Demo {  
        public static void main (String [] args) {  
            System.out.println("Main Start");  
  
            add();  
            add();  
            add();  
            System.out.println("Main End");  
  
  
        }  
        public static void add()  
        {  
            int a =10, b=20;;  
            int sum=a+b;  
            System.out.println(sum);  
              
        }  
  
}
```


### [[Argumented or parameterized method\|Argumented or parameterized method]]

A method which has formal arguments is know as parameterized method.

##### what is formal argument

A variable declared inside method declaration is know as formal argument 

##### Actual argument 

The values passed inside method calling statement is know as actual argument 

parameterized methods are used to make methods more flexible , reuseable and dynamic


### 🔄 Formal vs Actual Arguments

- **Formal Arguments**: Variables defined in the method signature.
    
- **Actual Arguments**: Values passed during method call.

Example:
```java
class Demo {  
        public static void main (String [] args) {  
            System.out.println("Main Start");  
  
            add(10,20);  
            add(243,23);  
            add(324,23);  
            System.out.println("Main End");  
  
  
        }  
        public static void add(int a , int b)  
        {  
            int sum=a+b;  
            System.out.println(sum);  
  
        }  
  
}
```

#### write a  java program calculor class consist of 4 paramterized methods 1)multiple 4 variable,2)To subtract 4 variable 3) To divide 3 variable 4) to add 5 variable 
```java
import java.util.Scanner;

class Demo {
    public static void main(String[] args) {
        // STEP 1: Program execution starts here
        System.out.println("Main Start");

        // STEP 2: Calling add method with 4 integer arguments
        add(10, 20, 30, 40);

        // STEP 5: Calling multiple method with 4 integer arguments
        multiple(3, 3, 3, 5);

        // STEP 8: Calling sub method with 4 integer arguments
        sub(4, 3, 5, 6);

        // STEP 11: Calling division method with 3 integer arguments
        division(2, 34, 5);

        // STEP 14: Calling add5 method with 5 integer arguments
        add5(1, 23, 4, 5, 3);

        // STEP 17: Final statement after all methods are executed
        System.out.println("Main End");
    }

    // STEP 3: add method definition
    public static void add(int a, int b, int c, int d) {
        System.out.println("----ADD-----");

        // STEP 4: Calculating and printing sum
        int sum = a + b + c + d;
        System.out.println(a + "+" + b + "+" + c + "+" + d + "=" + sum);
    }

    // STEP 15: add5 method definition
    public static void add5(int a, int b, int c, int d, int e) {
        System.out.println("----ADD5-----");

        // STEP 16: Calculating and printing sum

```

#### When we get compile time error during parameterized method
- When we passed wrong number of argument 
- When we passed wrong datatypes


```java
import java.util.Scanner;  
class Demo  
{  
        public static void main (String [] args)  
        {  
            Scanner sc= new Scanner (System.in);  
            System.out.print("Enter your name : ");  
  
            String name=sc.next();  
            System.out.print("Enter your Marks : ");  
  
            int marks= sc.nextInt();  
                calculateGrad(name,marks);  
  
  
  
        }  
    public static void calculateGrad(String name, int marks)  
    {  
        if (marks >= 90) {  
            System.out.println("Student : " + name +" "+ marks + " Grade A");  
        } else if (marks >= 70 && marks <= 89) {  
            System.out.println("Student : " + name +" "+marks + " Grade B ");  
        } else if (marks >= 50 && marks <= 69) {  
            System.out.println("Student : " + name +" "+ marks + " Grade C");  
        } else {  
            System.out.println("Student : " + name + " "+marks + " Grade F");  
        }  
    }  
}
```

### For Tracing 

```java  
import java.sql.SQLOutput;  
class Demo  
{  
    public static void ravi (int a)  
    {  
        System.out.println("hii ravi");  
        System.out.println(a);  
        yogesh ("java", a );  
        System.out.println("java");  
        harsh();  
        System.out.println("bye ravi");   
    }  
    public static void harsh()  
    {  
        System.out.println("hii harsh");  
        int a = 10, b=20;  
        System.out.println(a+b);  
        System.out.println(a*b);  
        yogesh("Python",b);  
        System.out.println("bye harsh");  
  
    }  
    public static void yogesh(String s,int a )  
    {  
        System.out.println("hii yogesh");  
        if (a<=10){  
            System.out.println("Hello"+s);  
        }  
        else  
        {  
            System.out.println("byee" + s);  
  
        }  
        System.out.println(a);  
        System.out.println("bye yogesh");  
    }  
  
    public static void main(String[] args)  
    {  
        System.out.println("main start");  
        harsh();  
        System.out.println("Python");  
        yogesh("sql",5);  
        System.out.println("sql");  
        ravi(7);  
        System.out.println("main end");  
  
    }  
}

/*main start
hii harsh
30
200
hii yogesh
byeePython
20
bye yogesh
bye harsh
Python
hii yogesh
Hellosql
5
bye yogesh
sql
hii ravi
7
hii yogesh
Hellojava
7
bye yogesh
java
hii harsh
30
200
hii yogesh
byeePython
20
bye yogesh
bye harsh
bye ravi
main end
*/
```

## 🔄 **Return Type and `return` Keyword**

- The `return` keyword sends a value back to the calling method.
    
- You **must define the return type** in the method declaration.
    
- Only **one value** can be returned.
    
- Anything written **after `return`** in a method block **won’t be executed**.

#### Return statement
- Return is a keyword
- It is a control transfer statement, it is used to return any value to caller method .
- Return must be the last the statement inside any block .
- one block can have only one return statement, if we write anything after return statement than we'll get compile time error.
- with the help of return statement we can return only single data.

Example:
```java
class Demo {
    public static void main(String[] args) {
        System.out.println("Main Start");
        add(10, 20);                          // Method called, result printed inside method
        System.out.println(add(25, 35));      // Result returned and printed in main
        int ans = add(12, 21);                // Returned value stored in variable
        System.out.println(ans);              // Variable value printed
        System.out.println("Main End");
    }

    public static int add(int a, int b) {
        int ans = a + b;
        return ans;                           // Value returned to the calling point
    }
}

```

### write a  java program to create calculator program consist of 4 parameterized 1)add 4 variable 2) multiplication 4 variavble 3)to return division of 2 variable 4) substractioin of 4

```java
class Demo {
    public static void main(String[] args) {
        System.out.println("Main Start");

        System.out.println(add(25, 35, 30, 40));  // Call method and print return value
        System.out.println(mul(25, 35, 30, 40));
        System.out.println(div(25, 35, 30, 40));
        System.out.println(sub(25, 35, 30, 40));

        System.out.println("Main End");
    }

    public static int add(int a, int b, int c, int d) {
        int ans = a + b + c + d;
        return ans;                           // Return sum
    }

    public static int mul(int a, int b, int c, int d) {
        int ans = a * b * c * d;
        return ans;                           // Return product
    }

    public static int div(int a, int b, int c, int d) {
        int ans = a / b / c / d;              // Performs division step by step
        return ans;
    }

    public static int sub(int a, int b, int c, int d) {
        int ans = a - b - c - d;              // Subtracts all values from left to right
        return ans;
    }
}
```

### Method Overloading

- A class is having more than 1 method with same name but different formal arguments (Either they're differ in length or datatype) is known as method Overloading 
- Method overloading is used to perform same functionality with different argument 

Example:

```java
import java.util.Scanner;  
class Demo  
{  
    public static void main (String [] args)  
    {  
        System.out.println("Main Start");  
  
       add(1,2,3,4);  
       add(1,2,3,4,5);  
       add(1,2);  
       add("hello","world");  
  
        System.out.println("Main End");  
  
  
    }  
    public static  int add (int a,int b,int c,int d)  
    {  
        System.out.println("----ADD4-----");  
        int sum = a+b+c+d;  
  
        System.out.println(a+"+"+b+"+"+c+"+"+d+"="+sum);  
         return sum;  
    }  
    public static void add (int a,int b,int c,int d,int e)  
    {  
        System.out.println("----ADD5-----");  
        int sum = a+b+c+d+e;  
  
        System.out.println(a+"+"+b+"+"+c+"+"+d+"+"+e+"="+sum);  
    }  
  
    public static void add (int a,int b)  
    {  
        System.out.println("----ADD2-----");  
  
        int sum = a+b;  
  
        System.out.println(a+"+"+b+"="+sum);  
    }  
  
    public static void add (String a,String b)  
    {  
        System.out.println("----ADD STRING-----");  
  
  
        String  sum = (a +b);  
  
        System.out.println(sum);  
    }  
}
```


### Q1. Write a Java program that demonstrates method overloading by creating a class AreaCalculator with overloaded methods named calculateArea. The methods should calculate the area of different shapes:

calculateArea(int side): Returns the area of a square.
calculateArea(double radius): Returns the area of a circle.
calculateArea(int length, int breadth): Returns the area of a rectangle.
```java
import java.util.Scanner;  
class Demo  
{  
    public static void main (String [] args)  
    {  
        System.out.println("Main Start");  
        calculateArea(4);  
        calculateArea(4);  
        calculateArea(4,6);  
  
  
  
        System.out.println("Main End");  
  
  
    }  
    public static  int calculateArea(int a)  
    {  
        int sq=0;  
  
        if (a !=0)  
        {  
            sq = a*a;  
  
        }  
  
        System.out.println(a+"*"+a+"="+sq);  
         return sq ;  
    }  
  
    public static  double calculateArea(double r)  
    {  
        double circle=0;  
  
        if (r !=0)  
        {  
            circle = 2*3.14*r*r;  
  
        }  
  
        System.out.println(r+"*"+r+"="+circle);  
        return circle ;  
    }  
    public static  double  calculateArea(int a , int b)  
    {  
        double rec=0;  
  
        if (a !=0 && b!=0)  
        {  
            rec = a*b;  
  
        }  
  
        System.out.println(a+"*"+a+"="+rec);  
        return rec ;  
    }  
}
```

### Q2. Write a java program to create calculator class consist of methods such as:
 - To subtract 3 variable
 - To subtract 4 variable
 - To subtract 5 variable
 - To subtract 2 variable
 - To Multiply 3 variable
 - To Multiply 4 variable
 - To Multiply 5 variable
 - To Multiply 2 variable
 - To divide 2 variable.

```java
import java.util.Scanner;  
class Demo  
{  
    public static void main (String [] args)  
    {  
        System.out.println("Main Start");  
  
        sub(2,4,5);  
        sub(2,4,5,5);  
        sub(2,4,5,5,6);  
        sub(2,4);  
        mul(2,3,5);  
        mul(2,3,5,6);  
        mul(2,3,5,6,1);  
        mul(2,3);  
        division(4,2);  
  
  
  
  
        System.out.println("Main End");  
  
  
    }  
    public static  int sub (int a,int b,int c)  
    {  
        System.out.println("----sub3-----");  
        int sub = a-b-c;  
  
        System.out.println(sub);  
        return sub;  
    }  
    public static int sub (int a,int b,int c,int d)  
    {  
        System.out.println("----sub4-----");  
        int sub = a-b-c-d;  
  
        System.out.println(sub);  
        return sub;  
    }  
  
    public static void sub (int a,int b,int c,int d,int e)  
    {  
        System.out.println("----sub5-----");  
  
        int sub = a-b-c-d-e;  
  
        System.out.println(sub);  
    }  
    public static int sub (int a,int b)  
    {  
        System.out.println("----sub2-----");  
  
        int sub = a-b;  
  
        System.out.println(sub);  
        return sub;  
    }  
    public static int mul (int a,int b,int c)  
    {  
        System.out.println("----mul3-----");  
  
        int mul = a*b*c;  
  
        System.out.println(mul);  
  
        return mul;  
    }  
    public static int mul (int a,int b,int c,int d)  
    {  
        System.out.println("----mul4-----");  
  
        int mul = a*b*c*d;  
  
        System.out.println(mul);  
  
        return mul;  
    }  
    public static int mul (int a,int b,int c,int d,int e)  
    {  
        System.out.println("----mul5-----");  
  
        int mul = a*b*c*d*e;  
  
        System.out.println(mul);  
  
        return mul;  
    }  
public static int mul (int a,int b)  
    {  
        System.out.println("----mul2-----");  
  
        int mul = a*b;  
  
        System.out.println(mul);  
  
        return mul;  
    }  
    public static int division (int a,int b)  
    {  
        System.out.println("----div2-----");  
  
        int div = a/b;  
  
        System.out.println(div);  
  
        return div;  
    }  
  
  
  
}
```

### Create an overloaded method greet() that:

Prints "Hello!" if no argument is passed
Prints "Hello, name!" if a string argument is passed
Prints "Hello, name! You are age years old." if both name and age are passed



```java
import java.util.Scanner;  
class Demo  
{  
    public static void main (String [] args)  
    {  
        System.out.println("Main Start");  
  
        greet();  
        greet("Deven");  
        greet("Deven",22);  
        System.out.println("Main End");  
    }  
  
    public static String greet()  
    {  
  
        String greet = "Hello !";  
        System.out.println(greet);  
  
         return greet;  
    }  
    public static String greet(String name)  
    {  
  
        String greet = "Hello ! "+name;  
        System.out.println(greet);  
  
        return greet;  
    }  
    public static String greet(String name,int age)  
    {  
  
        String greet = "Hello ! "+name+" you are "+age+" years old";  
        System.out.println(greet);  
  
        return greet;  
    }  
}
```


### Method recurrsion 

- A method calling itself is know as method recurssion , during method recurrsion we can get StackOverflowError
- It is a  alternative of loops

Example: 
```java
class Demo  
{  
    public static void stack()  
    {  
        System.out.println("hi");  
        stack();  
        System.out.println("bye");  
    }  
  
    public static void main(String[] args) {  
  
        System.out.println("main Start");  
        stack();  
        System.out.println(("Main end"));  
          
    }  
}
```

![Pasted image 20250723120431.png](/img/user/img/Pasted%20image%2020250723120431.png)
###  write a  java program to print numbers from the range 1 to 10 20 without using loop

```java
class Demo {
    public static int stack(int a) {
        System.out.println(a);
        a++;
        if (a <= 20) {
            stack(a);                 // Recursive call with next value
        }
        return a;
    }

    public static void main(String[] args) {
        System.out.println("main Start");
        stack(1);                      // Starts recursion from 1
        System.out.println("main End");
    }
}
```

###  write a  java program to print odd numbers from the range 50 to 25 without using loops 
```java 
class Demo {
    public static int stack(int a) {
        if (a % 2 != 0) {
            System.out.println(a);     // Print if odd
        }
        if (a > 25) {
            stack(--a);               // Recursive call with decremented value
        }
        return a;
    }

    public static void main(String[] args) {
        System.out.println("main Start");
        stack(50);                     // Starts from 50 down to 25
        System.out.println("main End");
    }
}
```

