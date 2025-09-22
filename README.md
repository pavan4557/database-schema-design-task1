# database-schema-design-task1
# SQL Developer Internship - Task 1: Database Setup & Schema Design

## 📌 Objective
The objective of this task is to learn **how to create databases, tables, and define relationships** using SQL.  
This includes understanding **DDL commands, ER diagrams, normalization, keys, and constraints**.

---

## 🛠 Tools Used
- MySQL Workbench

Interview Question Answers
What is normalization?
Normalization is the process of organizing data to reduce redundancy and improve data integrity by dividing data into related tables.

Explain primary vs foreign key.
A primary key uniquely identifies each record in a table. A foreign key is a column that creates a link between two tables by referencing a primary key in another table.

What are constraints?
Constraints are rules enforced on data columns to maintain accuracy and integrity, e.g., NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY.

What is a surrogate key?
A surrogate key is an artificially created unique key, usually an auto-incremented integer, used instead of natural keys.

How do you avoid data redundancy?
By normalizing the database and splitting data into multiple related tables, avoiding duplicate data storage.

What is an ER diagram?
Entity-Relationship diagram visually represents tables/entities and their relationships in the database.

Types of relationships in DBMS?
One-to-One, One-to-Many, Many-to-Many.

Explain the purpose of AUTO_INCREMENT.
AUTO_INCREMENT automatically generates unique sequential values for primary keys on inserts.

Default storage engine in MySQL?
InnoDB.

What is a composite key?
A key made up of two or more columns that uniquely identify a record.
## 📂 Deliverables
1. **SQL Script (`schema.sql`)**
   - Contains CREATE DATABASE and CREATE TABLE commands
   - Defines Primary Keys & Foreign Keys
   - Adds necessary constraints  

2. **ER Diagram**
   - Visual representation of entities and their relationships  

3. **README File**
   - Explanation of database schema
   - Key concepts covered  

---

## 📑 Key Concepts Covered
- **DDL Commands**: `CREATE`, `ALTER`, `DROP`  
- **Normalization**: Organizing data to avoid redundancy  
- **Primary Key vs Foreign Key**  
- **Constraints**: `NOT NULL`, `UNIQUE`, `CHECK`, `DEFAULT`  
- **Composite Key** and **Surrogate Key**  
- **AUTO_INCREMENT** usage  
- **ER Diagram** and types of relationships (`1:1`, `1:M`, `M:N`)  

---

    FOREIGN KEY (order_id) REFERENCES Orders(order_id),
    FOREIGN KEY (product_id) REFERENCES Products(product_id)

