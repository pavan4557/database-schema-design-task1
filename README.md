# database-schema-design-task1
# SQL Developer Internship - Task 1: Database Setup & Schema Design

## 📌 Objective
The objective of this task is to learn **how to create databases, tables, and define relationships** using SQL.  
This includes understanding **DDL commands, ER diagrams, normalization, keys, and constraints**.

---

## 🛠 Tools Used
- MySQL Workbench  
- PostgreSQL (pgAdmin)  
- SQLiteStudio  

---

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

## 🚀 Example Schema (E-Commerce Domain)

```sql
CREATE DATABASE ecommerce;

USE ecommerce;

CREATE TABLE Customers (
    customer_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    phone VARCHAR(15),
    address VARCHAR(255)
);

CREATE TABLE Products (
    product_id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    price DECIMAL(10,2) NOT NULL,
    stock INT DEFAULT 0
);

CREATE TABLE Orders (
    order_id INT AUTO_INCREMENT PRIMARY KEY,
    customer_id INT,
    order_date DATE,
    FOREIGN KEY (customer_id) REFERENCES Customers(customer_id)
);

CREATE TABLE OrderDetails (
    order_id INT,
    product_id INT,
    quantity INT NOT NULL,
    PRIMARY KEY (order_id, product_id),
    FOREIGN KEY (order_id) REFERENCES Orders(order_id),
    FOREIGN KEY (product_id) REFERENCES Products(product_id)
);
