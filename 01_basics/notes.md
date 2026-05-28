### SQL Basics Notes

Learn databases, tables, and CRUD operations.




# 📘 SQL Basics Notes

---

# CREATE DATABASE

---

# What is CREATE DATABASE?

`CREATE DATABASE` is an SQL command used to create a new database.

A database is a container that stores:

* Tables
* Records
* Relationships
* Application data

---

# Why Do We Need Databases?

Applications need databases to store data permanently.

Examples:

* User accounts
* Products
* Orders
* Payments
* Books
* Transactions

Without databases, applications cannot store or manage data properly.

---

# SQL Syntax

```sql id="db001"
CREATE DATABASE library_db;
```

---

# Line-by-Line Explanation

## CREATE DATABASE

Used to create a new database.

---

## library_db

Database name.

---

# Naming Best Practices

✅ Good Names

```text id="db002"
library_db
ecommerce_db
hospital_db
auth_system_db
```

---

❌ Bad Names

```text id="db003"
mydb123
test
abc
```

Use meaningful names.

---

# Real-World Examples

| Application     | Database Name |
| --------------- | ------------- |
| Library System  | library_db    |
| Banking App     | banking_db    |
| E-commerce      | ecommerce_db  |
| Hospital System | hospital_db   |

---

# Visual Understanding

```text id="db004"
PostgreSQL Server
        │
        ▼
+------------------+
|   library_db     |
+------------------+
```

---

# CREATE TABLE

---

# What is CREATE TABLE?

`CREATE TABLE` is used to create a new table inside a database.

Tables store data in:

* Rows
* Columns

---

# Why Tables Are Important

Tables organize data properly.

Example:

* Users table
* Orders table
* Books table
* Payments table

---

# SQL Syntax

```sql id="db005"
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    name VARCHAR(100),
    course VARCHAR(50)
);
```

---

# Line-by-Line Explanation

## CREATE TABLE students

Creates a table named:

```text id="db006"
students
```

---

## student_id INT PRIMARY KEY

| Part        | Meaning           |
| ----------- | ----------------- |
| student_id  | Column name       |
| INT         | Integer type      |
| PRIMARY KEY | Unique identifier |

---

## name VARCHAR(100)

Stores text up to 100 characters.

---

## course VARCHAR(50)

Stores course name.

---

# Visual Table Structure

```text id="db007"
Students Table
+------------+---------+---------+
| student_id | name    | course  |
+------------+---------+---------+
```

---

# Real-World Example

## E-commerce Products Table

```sql id="db008"
CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100),
    price INT
);
```

---

# INSERT INTO

---

# What is INSERT?

`INSERT INTO` is used to add data into a table.

---

# Why INSERT is Important

Applications constantly insert data.

Examples:

* User registration
* New orders
* Payments
* Book issue records

---

# SQL Syntax

```sql id="db009"
INSERT INTO students
VALUES (1, 'Vishal', 'BTech');
```

---

# Line-by-Line Explanation

## INSERT INTO students

Insert data into:

```text id="db010"
students
```

table.

---

## VALUES

Actual data being inserted.

---

## (1, 'Vishal', 'BTech')

| Value  | Meaning    |
| ------ | ---------- |
| 1      | student_id |
| Vishal | name       |
| BTech  | course     |

---

# Insert Multiple Records

```sql id="db011"
INSERT INTO students
VALUES
(1, 'Vishal', 'BTech'),
(2, 'Rahul', 'MCA'),
(3, 'Aman', 'BCA');
```

---

# Visual Understanding

## Before INSERT

```text id="db012"
Students Table

EMPTY
```

---

## After INSERT

| student_id | name   | course |
| ---------- | ------ | ------ |
| 1          | Vishal | BTech  |
| 2          | Rahul  | MCA    |
| 3          | Aman   | BCA    |

---

# SELECT Query

---

# What is SELECT?

`SELECT` is used to retrieve data from tables.

It is one of the MOST used SQL commands.

---

# Why SELECT is Important

Applications constantly fetch data.

Examples:

* Show users
* Show products
* Show orders
* Show books
* Show transaction history

---

# Basic SELECT Query

```sql id="db013"
SELECT * FROM students;
```

---

# Line-by-Line Explanation

## SELECT

Fetch data.

---

## *

Means:

```text id="db014"
All columns
```

---

## FROM students

Retrieve data from:

```text id="db015"
students
```

table.

---

# Output

| student_id | name   | course |
| ---------- | ------ | ------ |
| 1          | Vishal | BTech  |
| 2          | Rahul  | MCA    |
| 3          | Aman   | BCA    |

---

# Select Specific Columns

```sql id="db016"
SELECT name, course FROM students;
```

---

# Output

| name   | course |
| ------ | ------ |
| Vishal | BTech  |
| Rahul  | MCA    |
| Aman   | BCA    |

---

# WHERE Clause

---

# What is WHERE?

`WHERE` filters records.

---

# SQL Syntax

```sql id="db017"
SELECT * FROM students
WHERE student_id = 1;
```

---

# Output

| student_id | name   | course |
| ---------- | ------ | ------ |
| 1          | Vishal | BTech  |

---

# ORDER BY

---

# What is ORDER BY?

Used to sort data.

---

# Ascending Order

```sql id="db018"
SELECT * FROM students
ORDER BY name ASC;
```

---

# Descending Order

```sql id="db019"
SELECT * FROM students
ORDER BY name DESC;
```

---

# LIMIT

---

# What is LIMIT?

Limits the number of rows returned.

---

# SQL Syntax

```sql id="db020"
SELECT * FROM students
LIMIT 2;
```

---

# Output

Only first 2 rows will be shown.

---

# DISTINCT

---

# What is DISTINCT?

Removes duplicate values.

---

# Example

```sql id="db021"
SELECT DISTINCT course FROM students;
```

---

# Output

| course |
| ------ |
| BTech  |
| MCA    |
| BCA    |

---

# Backend Engineering Connection

Backend applications constantly use these queries.

Examples:

| Query           | Real Usage            |
| --------------- | --------------------- |
| CREATE DATABASE | New application setup |
| CREATE TABLE    | Schema design         |
| INSERT          | User registration     |
| SELECT          | Fetching data         |
| WHERE           | Authentication        |
| ORDER BY        | Sorting products      |
| LIMIT           | Pagination            |
| DISTINCT        | Unique filtering      |

---

# Industry Insight

Almost every backend API internally executes SQL queries.

Example:

* Login systems
* Payment systems
* Booking systems
* Analytics dashboards

All depend heavily on SQL.

---

# Important Interview Questions

## 1. What is CREATE DATABASE?

Used to create a new database.

---

## 2. Difference Between Database and Table?

| Database        | Table                   |
| --------------- | ----------------------- |
| Container       | Stores records          |
| Contains tables | Contains rows & columns |

---

## 3. What is INSERT INTO?

Used to insert records into a table.

---

## 4. What is SELECT?

Used to retrieve data from tables.

---

## 5. What is WHERE Clause?

Used to filter records.

---

## 6. What is LIMIT?

Restricts the number of rows returned.

---

## 7. What is DISTINCT?

Removes duplicate values.

---

# Common Beginner Mistakes

* Forgetting semicolon `;`
* Using duplicate Primary Keys
* Confusing database and table
* Using wrong column names
* Forgetting WHERE clause
* Using SELECT * unnecessarily

---

# Quick Revision Notes

* CREATE DATABASE → Creates database
* CREATE TABLE → Creates table
* INSERT INTO → Adds records
* SELECT → Fetches data
* WHERE → Filters data
* ORDER BY → Sorts data
* LIMIT → Restricts output
* DISTINCT → Removes duplicates

---

# Practice Queries

## Create Database

```sql id="db022"
CREATE DATABASE college_db;
```

---

## Create Table

```sql id="db023"
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    name VARCHAR(100),
    course VARCHAR(50)
);
```

---

## Insert Data

```sql id="db024"
INSERT INTO students
VALUES
(1, 'Vishal', 'BTech'),
(2, 'Rahul', 'MCA');
```

---

## Fetch All Data

```sql id="db025"
SELECT * FROM students;
```

---

## Filter Data

```sql id="db026"
SELECT * FROM students
WHERE student_id = 1;
```

---

# Mini Tasks

1. Create a database named:

```text id="db027"
hospital_db
```

2. Create a table:

```text id="db028"
patients
```

3. Insert 3 patient records.

4. Fetch all records.

5. Fetch only patient names.

---

# Next Topic

👉 Foreign Key & Relationships

We will learn:

* Connecting tables
* Real-world database relationships
* One-to-Many relationships
* Backend architecture
* SQL relationship design
