---
{"dg-publish":true,"permalink":"/workspace/3-java/loops-in-java/","noteIcon":""}
---

### 🔍 1. **Why We Need Loops** 

- Imagine you want to print **"Hello" 100 times**.
    
- Without loops, you'd write `System.out.println("Hello");` a hundred times — not practical.
    
- Instead, we use **loops** to **repeat tasks automatically**.
    

🧠 **Loops reduce code repetition** and improve readability.

---

### 🔁 2. **While Loop** 

#### 📌 Syntax:

```java
while(condition) {
    // repeat this block
}
```
📍 Example from the video:

```java
int i = 1;
while(i <= 5) {
    System.out.println("Hello " + i);
    i++;
}
```

🧠 The **condition is checked first**.  
If it's true, the loop runs.  
If it's false at the start, the loop won't run at all.

---

### 🔁 3. **Do While Loop** 

#### 📌 Syntax:
```java
do {
    // execute this block
} while(condition);
```

📍 Example 
```java
int i = 1; 
do {
    System.out.println("Hello " + i);
    i++;
} while(i <= 5);
```

🧠 Difference:

- **do-while always runs at least once**, even if the condition is false.
### 🔁 4. **For Loop**

#### 📌 Syntax:

```java
for(initialization; condition; increment/decrement) {
    // repeat block
}
```

#### 📍 Example :


```java
for(int i = 1; i <= 5; i++) {
    System.out.println("Hello " + i);
}
```

🧠 The **for loop is compact** and great when you know **exactly how many times** to run the loop.

---

### ❓ 5. **Which Loop to Use?** 

|Use Case|Loop|
|---|---|
|You know how many times to repeat|`for` loop|
|You don’t know how many times, but want to keep checking a condition|`while` loop|
|You want to run at least once, even if the condition is false|`do-while` loop|

---

### 🔁 Summary:

|Loop Type|Condition Check|Runs At Least Once?|Best Use Case|
|---|---|---|---|
|`while`|Before|❌|Unknown number of repetitions|
|`do-while`|After|✅|Run once before checking condition|
|`for`|Before (compact)|❌|Known/fixed number of iterations|

---
