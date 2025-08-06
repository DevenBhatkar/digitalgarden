---
{"dg-publish":true,"permalink":"/workspace/1-sql/data-types/","noteIcon":""}
---

## 📦 What are SQL Data Types?

**Data types** define the **kind of data** that can be stored in a column.  
Each column in a table must have a **data type**, so the database knows what kind of values to expect

Example:

- Name → `VARCHAR`
    
- Age → `NUMBER`
    
- Marks → `NUMBER(PRECISION,SCALE`)
    
- Join Date → `DATE`
    

---

## 🧱 Types of SQL Data Types (as per transcript):

### 1. 🅰️ **Character (Text) Data Types**

Used to store alphabets, words, strings (A-Z, a-z, names, cities).

|Type|Description|
|---|---|
|`CHAR(n)`|Fixed-length text. Reserves full space.|
|`VARCHAR(n)`|Variable-length text. Uses memory as needed.|

🔸 **Example:**

- `CHAR(10)` → Always reserves 10 bytes (even if only 3 letters are stored)
    
- `VARCHAR(10)` → Reserves only the space needed (saves memory)
    

✅ **Use `VARCHAR` in most cases.**

---

### 2. 🔢 **Numeric Data Types**

|Type|Description|
|---|---|
|`INT`|Normal whole numbers (e.g., 1, 100)|
|`TINYINT`|Smaller range of numbers|
|`MEDIUMINT`|Medium-sized integers|
|`BIGINT`|Very large integers|
|`FLOAT`|Decimal numbers with precision (e.g., 5.75)|
|`DOUBLE`|Bigger decimal numbers|
|`BIT(n)`|Store values in bits (binary: 0 or 1)|

---

### 3. 📅 **Date and Time Types**

|Type|Description|
|---|---|
|`DATE`|Stores date (YYYY-MM-DD)|
|`TIME`|Stores time (HH:MM:SS)|
|`DATETIME`|Stores both date and time|
|`YEAR`|Stores only the year (e.g., 2025)|

---

### 4. 📂 **Other Types**

|Type|Description|
|---|---|
|`BLOB`|Binary Large Object (for files, images, long strings)|
|`BOOLEAN`|True or False (internally stored as `TINYINT` 0 or 1)|

---

## ➕ What is Signed and Unsigned Data Type?

### ✳️ **Signed Data Type**

- Default in SQL
    
- Allows **both negative and positive numbers**
    
- Example: `-50`, `0`, `100`
    

### ➖➕ **Unsigned Data Type**

- Allows **only positive numbers**
    
- Gives **double the positive range**
    
- Example: `0`, `1`, `255` (but not -1)
    

---

### 🔁 Why use Unsigned?

If you're **sure a value can never be negative**, like:

- Age
    
- Salary
    
- Quantity
    
- Marks
    

... then use **`UNSIGNED`** to save space and allow larger positive numbers.

---

### 🧠 Example:

sql

CopyEdit

`age TINYINT UNSIGNED`

- Normal `TINYINT`: -128 to 127
    
- `TINYINT UNSIGNED`: 0 to 255 ✅
    

---

### ✅ Summary

> SQL has different data types to store strings, numbers, and dates.  
> Always define the right type for each column.  
> Use `UNSIGNED` when only positive values are allowed to extend the positive range.

[[Workspace/1.SQL/📚 SQL Commands\|Next]]