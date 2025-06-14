---
{"dg-publish":true,"permalink":"/workspace/1-sql/sql-commands/","noteIcon":""}
---

 ## **🧾 1. DDL (Data Definition Language)**

**Used to define the structure of the database.
This includes creating, modifying, or deleting tables and databases.

### 🛠️ Common DDL Commands:

|Command|Purpose|
|---|---|
|`CREATE`|Create a new database or table|
|`DROP`|Delete an existing table or database|
|`ALTER`|Modify structure of an existing table|
|`RENAME`|Rename a table|
|`TRUNCATE`|Remove all records from a table (faster than DELETE)|

📌 These commands **define or redefine the schema** (structure).

---

## 📖 2. **DQL (Data Query Language)**

**Used to fetch data** from the database.

### 🔍 Common DQL Command:

|Command|Purpose|
|---|---|
|`SELECT`|Retrieve data from one or more tables|

🟢 This is a **read-only** command — it **doesn’t modify data**.

---

## ✏️ 3. **DML (Data Manipulation Language)**

**Used to modify data** inside tables (but not the structure).

### 🔄 Common DML Commands:

|Command|Purpose|
|---|---|
|`INSERT`|Add new data/records|
|`UPDATE`|Modify existing data|
|`DELETE`|Remove specific data|

⚠️ These commands **change the actual data stored** in tables.

---

## 🔐 4. **DCL (Data Control Language)**

**Used to control access and permissions** to the data.

### 🧑‍💼 Common DCL Commands:

|Command|Purpose|
|---|---|
|`GRANT`|Give access rights to a user|
|`REVOKE`|Take back access rights from a user|

✅ Useful in real-world multi-user systems.

---

## 💼 5. **TCL (Transaction Control Language)**

**Used to manage transactions** in a database (group of SQL operations that must be executed together).

### 🔁 Common TCL Commands:

|Command|Purpose|
|---|---|
|`COMMIT`|Save all changes made in the transaction|
|`ROLLBACK`|Undo changes if there's an error|
|`SAVEPOINT`|Set a point to rollback to|

💡 Useful when doing **bulk changes** and need control over success/failure.

---

## 🧠 Summary Table:

| Type | Full Form                    | Purpose             | Key Commands                          |
| ---- | ---------------------------- | ------------------- | ------------------------------------- |
| DDL  | Data Definition Language     | Define structure    | `CREATE`, `DROP`, `ALTER`, `TRUNCATE` |
| DQL  | Data Query Language          | Query data          | `SELECT`                              |
| DML  | Data Manipulation Language   | Modify data         | `INSERT`, `UPDATE`, `DELETE`          |
| DCL  | Data Control Language        | Access control      | `GRANT`, `REVOKE`                     |
| TCL  | Transaction Control Language | Transaction control | `COMMIT`, `ROLLBACK`, `SAVEPOINT`     |
[[Workspace/1.SQL/📚 Basic Database and Table Queries in SQL\|Next]]