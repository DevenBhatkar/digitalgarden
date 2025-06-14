---
{"dg-publish":true,"permalink":"/workspace/1-sql/introduction/","noteIcon":""}
---


## 📌 What is a Database?

A **database** is a structured collection of data that is stored and accessed electronically. It allows easy storage, access, manipulation, and management of data.

- In simple terms, it's like a digital filing system.
    
- Data is stored in an organized format so it can be easily retrieved, managed, and updated.
    
- Used by tech companies like Google, Amazon, Facebook to store user data, logs, and transactions.
    
- Accessible and modifiable using specialized software like **DBMS** (Database Management Systems).
    

> 🧠 Think of it like your class teacher’s register, but stored on a computer.

---

## 🧠 What is a DBMS?

**DBMS** stands for **Database Management System**.

- It's a software application used to **create, manage, and interact with databases**.
    
- It acts as a **bridge** between the user and the database.
    
- Handles operations like:
    
    - Add data
        
    - Retrieve data
        
    - Update data
        
    - Delete data
        

> 📌 Examples: MySQL, Oracle, SQL Server

---

## 🧩 Types of Databases

### 1. **Relational Databases (RDBMS)**

- Store data in **tables (rows and columns)**.
    
- Tables can be related to each other using keys.
    
- Use **SQL** (Structured Query Language) for querying data.
    

> 🧱 Example: MySQL, Oracle, PostgreSQL, Microsoft SQL Server

### 2. **Non-Relational Databases (NoSQL)**

- Store data in formats like **JSON, key-value pairs, documents**, or **graphs**.
    
- Do **not use tables**.
    
- Suitable for unstructured or semi-structured data.
    
- Do not understand SQL — hence called _NoSQL_.
    

> 🧾 Example: MongoDB, Cassandra, CouchDB

---

## 🆚 RDBMS vs NoSQL

| Feature        | RDBMS                          | NoSQL                             |
| -------------- | ------------------------------ | --------------------------------- |
| Structure      | Table-based                    | Document / Key-value / Graph etc. |
| Query Language | SQL                            | Varies (No standard)              |
| Relationships  | Supports complex relationships | Often denormalized data           |
| Examples       | MySQL, Oracle                  | MongoDB, Redis                    |

### ✅ What is SQL?

**SQL** stands for **Structured Query Language**.  
It is a **special language** used to interact with **relational databases**.

---

### 🔍 Why do we use SQL?

- Computers don’t understand human languages like Hindi or English.
    
- So, we use SQL to **talk to databases** and **manage data** stored in them.
    
- SQL allows us to **create**, **read**, **update**, and **delete** data – these are called **CRUD operations**.
    

---

### 🧠 What kind of databases does SQL work with?

- SQL is used with **Relational Databases** (RDBMS), where data is stored in **tables**.
    
- Examples of relational databases:
    
    - MySQL
        
    - Oracle
        
    - Microsoft SQL Server
        

---

### 🗨️ Fun Fact:

- Some people call SQL **"Sequel"**.
    
- Originally, it was called **SEQUEL – Structured English Query Language**, developed by IBM.
    

---

### ✅ Summary:

> **SQL is a powerful language used to manage and communicate with relational databases by performing operations like creating, reading, updating, and deleting data in a structured format.**

[[Workspace/1.SQL/📚 SQL Structure\|Next]]