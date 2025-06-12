---
{"dg-publish":true,"permalink":"/workspace/1-sql/basic-database-and-table-queries-in-sql/","noteIcon":""}
---

### 📌 **1. Creating a Database**

Use the `CREATE DATABASE` command to make a new database.
![Pasted image 20250608150156.png](/img/user/img/Pasted%20image%2020250608150156.png)📝 This creates a database named **xyz**.

🔒 Best Practice:
![Pasted image 20250608150214.png](/img/user/img/Pasted%20image%2020250608150214.png)✔️ Prevents error if it already exists.

---

### 📌 **2. Using a Database**

Before creating tables or inserting data, **select the database** you want to use:

![Pasted image 20250608150234.png](/img/user/img/Pasted%20image%2020250608150234.png)This tells SQL to work inside the `xyz` database.

---

### 📌 **3. Creating a Table**

Tables are used to store data in rows and columns. Use the `CREATE TABLE` command:
![Pasted image 20250608150257.png](/img/user/img/Pasted%20image%2020250608150257.png)
📌 Breakdown:

- `id`: Integer type, set as **Primary Key** (must be unique)
    
- `name`: Text field of max 30 characters (`VARCHAR`)
    
- `salary`: Integer field
    

---

### 📌 **4. Inserting Data into Table**

Use `INSERT INTO` to add records (rows) into a table.
![Pasted image 20250608150337.png](/img/user/img/Pasted%20image%2020250608150337.png)✅ This inserts 3 employees into the table at once.

---

### 📌 **5. Retrieving Data from Table**

Use the `SELECT` command to view data:

![Pasted image 20250608150357.png](/img/user/img/Pasted%20image%2020250608150357.png)- `*` means **select all columns**
    
- You’ll get a table like:
    

|id|name|salary|
|---|---|---|
|101|bob|30000|
|102|rahul|35000|
|103|warner|50000|

---

### ✅ Summary:

|Command|Use|
|---|---|
|`CREATE DATABASE`|Create a new database|
|`USE`|Select database to work in|
|`CREATE TABLE`|Create a new table structure|
|`INSERT INTO`|Add records into the table|
|`SELECT * FROM table`|View all data in a table|
