# database-schema-design-task1
# SQL Developer Internship - Task 1: Database Setup & Schema Design

## 📌 Objective
The objective of this task is to learn **how to create databases, tables, and define relationships** using SQL.  
This includes understanding **DDL commands, ER diagrams, normalization, keys, and constraints**.

---

## 🛠 Tools Used
- MySQL Workbench
- # Library Database Schema Design

## Objective
To design and implement a relational database schema for a library management system with tables, constraints, and relationships.

## Tools Used
MySQL Workbench (can be run on other SQL tools like pgAdmin or SQLiteStudio).

## Database Schema
Includes tables for Categories, Authors, Books, Members, and Loans, with primary and foreign keys to enforce relationships.

## Instructions
Run the provided SQL script library_schema.sql to create and populate the database schema.

## ER Diagram
(If created: include ER diagram image or link here)

## Interview Questions
Answers to key questions related to normalization, keys, constraints, ER diagrams, and DBMS concepts.

## Notes
This schema supports basic library functionalities such as managing books, authors, member loans, and categories.

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

