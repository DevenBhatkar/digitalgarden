---
{"dg-publish":true,"permalink":"/workspace/3-java/data-types-in-java/","noteIcon":""}
---

### 📂 Types of Data Types:

Java data types are divided into two broad categories:
1. Primitive Data Types
2. Non-Primitive (covered later)
``

### 🔢 **Primitive Data Types**

#### There are 4 major categories of primitive types:

|Category|Types|
|---|---|
|Integer|byte, short, int, long|
|Float|float, double|
|Character|char|
|Boolean|boolean|


### 📌 Integer Types

|Type|Size|Example|
|---|---|---|
|byte|1 byte|`byte b = 8;`|
|short|2 bytes|`short s = 558;`|
|int|4 bytes|`int num = 100;`|
|long|8 bytes|`long l = 10000L;` (suffix `L` is required)|

> Use **`byte`** if you're working with very small values (like -128 to 127).


### 📌 Floating-Point Types

|Type|Size|Example|
|---|---|---|
|float|4 bytes|`float f = 5.8f;` (`f` required)|
|double|8 bytes|`double d = 5.8;`|

- Java assumes decimal numbers are `double` by default.  
    Use `f` for float values.
    

---

### 🔤 Character Type

| Type | Size    | Notes                                         |
| ---- | ------- | --------------------------------------------- |
| char | 2 bytes | Unicode support. Use **single quotes**: `'A'` |
```java
char c = 'k';
```
Double quotes are for Strings, single quotes for characters.

### ✅ Boolean Type

| Type    | Values                 |
| ------- | ---------------------- |
| boolean | `true` or `false` only |
```java
boolean isActive = true;
```
You **cannot use `0` or `1`** for boolean in Java.

### ❗ Common Errors from the Video:

- Trying to store a number outside the range of the type (e.g., `byte b = 129;`) will cause a **lossy conversion error**.
    
- Trying to store decimal in a `float` without `f` will also cause an error.