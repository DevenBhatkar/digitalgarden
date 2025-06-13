---
{"dg-publish":true,"permalink":"/workspace/3-java/if-else-in-java/","noteIcon":""}
---

### 📌 Purpose:

`if-else` is used to **make decisions** in Java based on **true/false conditions**.

---

### 🧪 Example :

```java
int age = 18;

if(age >= 18) {
    System.out.println("You can vote");
} else {
    System.out.println("You cannot vote");
}
```

> ✅ If condition is **true**, it runs the `if` block  
> ❌ If condition is **false**, it runs the `else` block

---

### ✅ Summary:

- Only **one** block will execute.
    
- `if` = condition is true
    
- `else` = condition is false
    

---

## 🧭 **If Else If in Java**

### 📌 Purpose:

Used when you need to **check multiple conditions** in a sequence.

---

### 🧪 Example :

```java
int marks = 65;

if(marks >= 90) {
    System.out.println("Grade A");
} else if(marks >= 70) {
    System.out.println("Grade B");
} else if(marks >= 60) {
    System.out.println("Grade C");
} else {
    System.out.println("Grade D");
}
```

> Checks each condition from top to bottom  
> First condition that returns `true` gets executed — rest are ignored.

---

### ✅ Summary:

- Use `if-else-if` when you have **more than two possible outcomes**
    
- Only **one matching block** runs

[[Workspace/3.JAVA/📚If Else in Java\|next]]
