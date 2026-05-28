# 📘 RDBMS Notes

---

# What is RDBMS?

RDBMS stands for **Relational Database Management System**.

It is a type of DBMS that stores data in the form of:

* Tables
* Rows
* Columns

and manages relationships between tables.

RDBMS helps to:

* Store structured data
* Connect related data
* Reduce duplication
* Maintain data consistency
* Manage large applications efficiently

---

# Why Do We Need RDBMS?

RDBMS is needed because modern applications contain connected data.

Example:

* Users and Orders
* Students and Courses
* Customers and Transactions

Without relationships:

* Data becomes unorganized
* Duplicate data increases
* Searching becomes difficult
* Data consistency becomes weak

RDBMS solves these problems using relational tables.

---

# Why RDBMS Was Created

Traditional DBMS systems had limitations:

* Weak relationships
* Poor scalability
* Difficult data management
* Duplicate data problems

Industries needed:

* Structured databases
* Connected tables
* Better data integrity
* Enterprise-level scalability

This led to the development of:

# 👉 RDBMS

---

# Core Idea of RDBMS

RDBMS stores data inside tables.

These tables are connected using:

* Primary Keys
* Foreign Keys

This creates relationships between data.

---

# Important Components of RDBMS

| Component    | Meaning                    |
| ------------ | -------------------------- |
| Table        | Collection of related data |
| Row          | Single record              |
| Column       | Field or attribute         |
| Primary Key  | Uniquely identifies a row  |
| Foreign Key  | Connects tables            |
| Relationship | Connection between tables  |

---

# Difference Between DBMS and RDBMS

| DBMS                       | RDBMS                        |
| -------------------------- | ---------------------------- |
| General database system    | Relational database system   |
| Data may not be relational | Data is relational           |
| Less structured            | Highly structured            |
| No strong relationships    | Supports relationships       |
| Lower scalability          | Enterprise-level scalability |
| Smaller systems            | Large-scale applications     |

---

# Real-World Example — Library Management System

## Students Table

| student_id | name   |
| ---------- | ------ |
| 1          | Vishal |
| 2          | Rahul  |

---

## Books Table

| book_id | title  |
| ------- | ------ |
| 101     | DBMS   |
| 102     | Python |

---

## Issued Books Table

| issue_id | student_id | book_id |
| -------- | ---------- | ------- |
| 1        | 1          | 101     |

---

# Understanding Relationships

In the Issued Books table:

```text
student_id = 1
```

connects to:

```text
Vishal
```

And:

```text
book_id = 101
```

connects to:

```text
DBMS
```

This connection between tables is called a:

# 👉 Relationship

---

# Types of Relationships

## 1. One-to-One (1:1)

One record connects to one record.

### Example

* One user → One passport

---

## 2. One-to-Many (1:M)

One record connects to many records.

### Example

* One customer → Many orders

---

## 3. Many-to-Many (M:M)

Many records connect to many records.

### Example

* Students ↔ Courses

---

# Visual Understanding

## Simple Relational Structure

```text
Students Table
+------------+--------+
| student_id | name   |
+------------+--------+
| 1          | Vishal |
| 2          | Rahul  |
+------------+--------+

Books Table
+---------+--------+
| book_id | title  |
+---------+--------+
| 101     | DBMS   |
| 102     | Python |
+---------+--------+

Issued Books Table
+----------+------------+---------+
| issue_id | student_id | book_id |
+----------+------------+---------+
| 1        | 1          | 101     |
+----------+------------+---------+
```

---

# Industry Insight

Most modern applications use RDBMS.

Examples:

* Banking Systems
* E-commerce Platforms
* Social Media Apps
* Hospital Systems
* Authentication Systems

Without RDBMS:

* Data consistency becomes difficult
* Relationships break
* Applications become unreliable

---

# Popular RDBMS Software

| Software        | Usage                             |
| --------------- | --------------------------------- |
| PostgreSQL      | Backend & enterprise applications |
| MySQL           | Web applications                  |
| Oracle Database | Banking systems                   |
| SQL Server      | Enterprise software               |

---

# Why PostgreSQL is Important

PostgreSQL is a powerful RDBMS used in:

* Backend engineering
* Enterprise systems
* Large-scale applications

It supports:

* Advanced SQL
* Transactions
* JSON data
* Indexing
* Scalability
* High performance

---

# Why RDBMS is Important in Backend Development

Backend applications constantly manage related data.

Example:

* User accounts
* Orders
* Payments
* Authentication
* Bookings

RDBMS helps backend developers:

* Organize data properly
* Build scalable systems
* Manage relationships
* Ensure data consistency
* Handle transactions securely

---

# Backend Architecture Example

```text
Frontend (React / Mobile App)
             │
             ▼
Backend API (FastAPI / Node.js)
             │
             ▼
RDBMS
(PostgreSQL / MySQL)
             │
             ▼
Database Tables
```

---

# Real-World Use of RDBMS in Banking

Banks use RDBMS to manage:

* Customer accounts
* Transactions
* Loan systems
* ATM operations
* Payment systems

Example:

When money is transferred:

1. Amount is deducted from one account
2. Added to another account
3. Transaction history is updated
4. Data consistency is maintained

RDBMS ensures:

* Accuracy
* Security
* Reliability

---

# Important Interview Questions

## 1. What is RDBMS?

**Answer:**
RDBMS (Relational Database Management System) is a type of DBMS that stores data in relational tables and manages relationships between those tables.

---

## 2. What is the Difference Between DBMS and RDBMS?

| DBMS                          | RDBMS                      |
| ----------------------------- | -------------------------- |
| General database system       | Relational database system |
| May not support relationships | Supports relationships     |
| Less structured               | Highly structured          |

---

## 3. What is a Relationship in RDBMS?

A relationship connects tables using keys such as:

* Primary Key
* Foreign Key

---

## 4. What is a Table?

A table stores related data in:

* Rows
* Columns

---

## 5. What is a Row?

A row represents a single record in a table.

### Example

| id | name   |
| -- | ------ |
| 1  | Vishal |

---

## 6. What is a Column?

A column represents a field or attribute.

### Examples

* name
* email
* age

---

## 7. What is a Primary Key?

A primary key uniquely identifies each row in a table.

### Example

```text
student_id
```

---

## 8. What is a Foreign Key?

A foreign key connects two tables.

### Example

```text
Students Table ← Orders Table
```

---

## 9. Why Do Industries Prefer RDBMS?

Because it provides:

* Relationships
* Security
* Scalability
* Data consistency
* Transaction support

---

## 10. Which RDBMS Tools Have You Used?

### Examples

* PostgreSQL
* MySQL
* SQL Server

---

# Common Beginner Mistakes

* Confusing DBMS and RDBMS
* Ignoring relationships
* Forgetting Primary Keys
* Storing duplicate data
* Designing tables incorrectly
* Not understanding Foreign Keys

---

# Quick Revision Notes

* RDBMS = Relational Database Management System
* Stores data in tables
* Supports relationships
* Uses Primary Keys and Foreign Keys
* Helps manage structured data
* Used in modern backend applications
* PostgreSQL is a popular RDBMS
* Essential for scalable applications

---

# Next Topic

👉 What is SQL?

We will learn:

* SQL basics
* SQL command categories
* How SQL communicates with databases
* Real-world query understanding
