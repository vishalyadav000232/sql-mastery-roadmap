# PostgreSQL CLI Commands Cheat Sheet

---

# 1. PostgreSQL Installation Check

```bash
psql --version
```

Check installed PostgreSQL version.

---

# 2. Login into PostgreSQL

```bash
psql -U postgres
```

Login using postgres user.

---

# 3. Login with Database

```bash
psql -U postgres -d mydb
```

Connect directly to a specific database.

---

# 4. Exit PostgreSQL

```bash
\q
```

Quit PostgreSQL shell.

---

# 5. Show All Databases

```sql
\l
```

OR

```sql
\list
```

---

# 6. Create Database

```sql
CREATE DATABASE company_db;
```

---

# 7. Delete Database

```sql
DROP DATABASE company_db;
```

---

# 8. Connect to Database

```sql
\c company_db
```

---

# 9. Show Current Database

```sql
SELECT current_database();
```

---

# 10. Show Current User

```sql
SELECT current_user;
```

---

# 11. Show All Tables

```sql
\dt
```

---

# 12. Describe Table Structure

```sql
\d students
```

---

# 13. Create Table

```sql
CREATE TABLE students (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    age INT
);
```

---

# 14. Insert Data

```sql
INSERT INTO students(name, age)
VALUES ('Vishal', 22);
```

---

# 15. View Data

```sql
SELECT * FROM students;
```

---

# 16. Filter Data

```sql
SELECT * FROM students
WHERE age > 20;
```

---

# 17. Update Data

```sql
UPDATE students
SET age = 23
WHERE id = 1;
```

---

# 18. Delete Data

```sql
DELETE FROM students
WHERE id = 1;
```

---

# 19. Delete All Rows

```sql
TRUNCATE TABLE students;
```

---

# 20. Delete Table

```sql
DROP TABLE students;
```

---

# 21. Rename Table

```sql
ALTER TABLE students
RENAME TO college_students;
```

---

# 22. Add New Column

```sql
ALTER TABLE students
ADD email VARCHAR(100);
```

---

# 23. Remove Column

```sql
ALTER TABLE students
DROP COLUMN email;
```

---

# 24. Rename Column

```sql
ALTER TABLE students
RENAME COLUMN name TO full_name;
```

---

# 25. Show All Users

```sql
\du
```

---

# 26. Create User

```sql
CREATE USER vishal
WITH PASSWORD '1234';
```

---

# 27. Grant Permissions

```sql
GRANT ALL PRIVILEGES
ON DATABASE company_db
TO vishal;
```

---

# 28. Revoke Permissions

```sql
REVOKE ALL PRIVILEGES
ON DATABASE company_db
FROM vishal;
```

---

# 29. Backup Database

```bash
pg_dump -U postgres company_db > backup.sql
```

---

# 30. Restore Database

```bash
psql -U postgres company_db < backup.sql
```

---

# 31. Export Table Data

```sql
COPY students TO '/tmp/students.csv'
DELIMITER ','
CSV HEADER;
```

---

# 32. Import CSV Data

```sql
COPY students(name, age)
FROM '/tmp/students.csv'
DELIMITER ','
CSV HEADER;
```

---

# 33. Show Running Queries

```sql
SELECT * FROM pg_stat_activity;
```

---

# 34. Kill Query

```sql
SELECT pg_terminate_backend(pid);
```

---

# 35. Show Database Size

```sql
SELECT pg_size_pretty(
    pg_database_size('company_db')
);
```

---

# 36. Show Table Size

```sql
SELECT pg_size_pretty(
    pg_total_relation_size('students')
);
```

---

# 37. Start Transaction

```sql
BEGIN;
```

---

# 38. Commit Transaction

```sql
COMMIT;
```

---

# 39. Rollback Transaction

```sql
ROLLBACK;
```

---

# 40. Create Index

```sql
CREATE INDEX idx_students_name
ON students(name);
```

---

# 41. Remove Index

```sql
DROP INDEX idx_students_name;
```

---

# 42. Inner Join Example

```sql
SELECT s.name, b.book_name
FROM students s
INNER JOIN books b
ON s.id = b.student_id;
```

---

# 43. Count Rows

```sql
SELECT COUNT(*) FROM students;
```

---

# 44. Average Value

```sql
SELECT AVG(age) FROM students;
```

---

# 45. Group By

```sql
SELECT age, COUNT(*)
FROM students
GROUP BY age;
```

---

# 46. Order By

```sql
SELECT * FROM students
ORDER BY age DESC;
```

---

# 47. Limit Rows

```sql
SELECT * FROM students
LIMIT 5;
```

---

# 48. PostgreSQL Service Start

## Linux

```bash
sudo systemctl start postgresql
```

---

# 49. PostgreSQL Service Stop

```bash
sudo systemctl stop postgresql
```

---

# 50. PostgreSQL Service Status

```bash
sudo systemctl status postgresql
```

---

# Important PostgreSQL Shortcuts

| Command | Meaning |
|---|---|
| \l | List databases |
| \c | Connect database |
| \dt | Show tables |
| \d table_name | Describe table |
| \du | Show users |
| \q | Quit PostgreSQL |

---

# Backend Developer Important Commands

| Purpose | Command |
|---|---|
| Create DB | CREATE DATABASE |
| Create Table | CREATE TABLE |
| Insert Data | INSERT |
| Fetch Data | SELECT |
| Update Data | UPDATE |
| Delete Data | DELETE |
| Relationships | FOREIGN KEY |
| Performance | INDEX |
| Safety | TRANSACTION |

---

# Real-World Industry Commands

| Industry Use | PostgreSQL Feature |
|---|---|
| Banking | Transactions |
| E-commerce | Joins |
| Analytics | Aggregate Functions |
| Authentication | Users & Roles |
| High Performance | Indexes |
| Backup Systems | pg_dump |

---