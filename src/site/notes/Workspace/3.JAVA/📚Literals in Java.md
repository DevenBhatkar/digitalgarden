---
{"dg-publish":true,"permalink":"/workspace/3-java/literals-in-java/","noteIcon":""}
---

### 📌 What are Literals?

> **Literals** are the **actual fixed values** that you assign to variables.

For example:
```java
int num=9;
```
Here, `9` is a **literal** — a hardcoded value directly written in the code.

---

### 🔢 Types of Literals :

#### ✅ **Integer Literals**

- Normal base-10 numbers like `9`, `100000`, etc.
    
- You can even use **underscores** to make large numbers readable:
```java
int bigNum = 1_00_000;
```
> Java ignores the underscores. It just helps **you** as a programmer to count digits easily.

#### ✅ **Binary Literals**

- You can write numbers in **binary format** using the prefix `0b`:
```java
int num = 0b101;  // Output: 5
```


#### ✅ **Hexadecimal Literals**

- Prefix `0x` is used for hexadecimal values:
```java
int hexNum = 0x7E;  // Output: 126
```
#### ✅ **Scientific Notation**

Used with floating point/double numbers using **E or e**:
```java
double val = 12e10;
```
> This means `12 × 10^10`. Java handles the formatting internally.

---

### 📉 Type Conversion with Literals

- You can assign integer values to float/double variables.
    
- If assigning an **integer to a `double`**, it’s allowed automatically.
```java
double d = 56;  // allowed
```
- But if you assign a **decimal to a float**, Java treats the value as `double` by default and throws an error:
```java
float f = 5.6;  // ❌ Error
float f = 5.6f; // ✅ Correct
```
> You need to add **`f`** to indicate it’s a float literal.

---

### ✅ Boolean Literals
```java
boolean b = true;  // valid
boolean b = 1;     // ❌ Error
```
> Java does **not** allow `0` or `1` for boolean — only `true` or `false`.

---

### 🔤 Character Literals

```java
char c = 'A';     // ✅ Single quotes only
char c = "A";     // ❌ Error (double quotes are for Strings)
```
You can perform operations like `c++`:
```java
char c = 'A';
c++;
System.out.println(c); // Output: B
```
> Characters can be incremented because they’re internally stored as numeric Unicode values.

---

### 📚 Summary

| Type        | Literal Example     | Notes                       |
| ----------- | ------------------- | --------------------------- |
| Integer     | `9`, `100`, `0b101` | Use underscores for clarity |
| Float       | `5.6f`              | Must add `f` suffix         |
| Double      | `12e10`, `5.6`      | Default for decimal         |
| Boolean     | `true`, `false`     | Only valid values           |
| Character   | `'A'`, `'8'`        | Single quotes only          |
| Hexadecimal | `0x7E`              | Base-16 numbers             |
| Binary      | `0b101`             | Base-2 numbers              |

[[Workspace/3.JAVA/📚Literals in Java\|next]]