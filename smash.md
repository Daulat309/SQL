# Complete SQL Learning Course: Beginner to Advanced

**Beginner → Advanced | Backend Development & Placement Preparation**

This course covers SQL from the fundamentals to advanced database concepts, with practical queries, explanations, interview-relevant concepts, and exercises.

> **Course baseline:** MySQL 8.0 syntax. Most concepts also apply to PostgreSQL; important differences are pointed out where relevant.

By the end, you should be able to design relational databases, write complex SQL queries, work with transactions and indexes, optimize queries, and use SQL confidently with Java and Spring Boot.

---

## Table of Contents

1. [Course Roadmap](#1-course-roadmap)
2. [Suggested 30-Day Learning Schedule](#2-suggested-30-day-learning-schedule)
3. [Part 1 — Database Fundamentals](#part-1--database-fundamentals)
4. [Part 2 — Creating Databases and Tables](#part-2--creating-databases-and-tables)
5. [Part 3 — DML and DQL](#part-3--dml-and-dql)
6. [Part 4 — Filtering, Operators and Sorting](#part-4--filtering-operators-and-sorting)
7. [Part 5 — Constraints and Keys](#part-5--constraints-and-keys)
8. [Part 6 — Aggregate Functions and GROUP BY](#part-6--aggregate-functions-and-group-by)
9. [Part 7 — SQL JOIN Operations](#part-7--sql-join-operations)
10. [Part 8 — Subqueries](#part-8--subqueries)
11. [Part 9 — Set Operators and Conditional Logic](#part-9--set-operators-and-conditional-logic)
12. [Part 10 — CTEs](#part-10--ctes-common-table-expressions)
13. [Part 11 — Window Functions](#part-11--window-functions)
14. [Part 12 — Views and Database Objects](#part-12--views-and-database-objects)
15. [Part 13 — Indexing and Query Optimization](#part-13--indexing-and-query-optimization)
16. [Part 14 — Transactions and ACID](#part-14--transactions-and-acid-properties)
17. [Part 15 — Database Normalization](#part-15--database-normalization)
18. [Part 16 — Stored Procedures, Functions and Triggers](#part-16--stored-procedures-functions-and-triggers)
19. [Part 17 — Database Security and Administration](#part-17--database-security-and-administration)
20. [Part 18 — Important SQL Concepts for Interviews](#part-18--important-sql-concepts-for-interviews)
21. [Part 19 — MySQL vs PostgreSQL](#part-19--mysql-vs-postgresql)
22. [Part 20 — SQL with Java and Spring Boot](#part-20--sql-with-java-and-spring-boot)
23. [Part 21 — SQL Interview Preparation](#part-21--sql-interview-preparation)
24. [Part 22 — Important Built-in SQL Functions](#part-22--important-built-in-sql-functions)
25. [Part 23 — Advanced SQL Patterns for Backend Applications](#part-23--advanced-sql-patterns-for-backend-applications)
26. [Part 24 — Capstone Project](#part-24--capstone-project)
27. [Part 25 — Final Learning Checklist](#part-25--final-learning-checklist)

---

## 1. Course Roadmap

| Module | Topics | Level |
|---|---|---|
| 1 | Database fundamentals and SQL introduction | Beginner |
| 2 | Database creation, tables and data types | Beginner |
| 3 | DDL, DML, DQL and TCL commands | Beginner |
| 4 | SELECT, filtering, sorting and limiting | Beginner |
| 5 | SQL operators and pattern matching | Beginner |
| 6 | Constraints, keys and relationships | Beginner |
| 7 | Aggregate functions and GROUP BY | Intermediate |
| 8 | Joins: INNER, LEFT, RIGHT, CROSS, SELF | Intermediate |
| 9 | Subqueries and correlated subqueries | Intermediate |
| 10 | Set operators | Intermediate |
| 11 | CASE, NULL handling and conditional logic | Intermediate |
| 12 | Common Table Expressions (CTEs) | Advanced |
| 13 | Window functions | Advanced |
| 14 | Views and materialized views | Advanced |
| 15 | Indexes and query optimization | Advanced |
| 16 | Transactions, ACID and concurrency | Advanced |
| 17 | Normalization and database design | Advanced |
| 18 | Stored procedures, functions and triggers | Advanced |
| 19 | Security and database administration basics | Advanced |
| 20 | SQL interview problems and real-world projects | Practice |

## 2. Suggested 30-Day Learning Schedule

| Days | Learning target |
|---|---|
| 1–3 | Database fundamentals, SQL commands, tables and data types |
| 4–6 | SELECT, WHERE, operators, sorting and filtering |
| 7–9 | Constraints, primary keys, foreign keys and relationships |
| 10–12 | Aggregate functions and GROUP BY |
| 13–15 | All major JOIN operations |
| 16–18 | Subqueries, correlated queries and set operators |
| 19–21 | CASE, NULL, CTEs and window functions |
| 22–24 | Indexes, execution plans and query optimization |
| 25–26 | Transactions, ACID, locks and isolation levels |
| 27–28 | Normalization, views, procedures and triggers |
| 29–30 | Interview practice and mini-project |

**How to study each topic:** Understand the concept → execute the example → modify the query → solve the practice problems without looking at the solution.

---

# Part 1 — Database Fundamentals

## 3. What is a database?

A database is an organized collection of data that can be stored, accessed, modified and managed efficiently.

For example, a college database might store:

- Student details
- Faculty details
- Courses
- Attendance
- Examination results

Without a database, maintaining this information in separate files becomes difficult as the data grows.

## 4. What is a DBMS?

A **Database Management System (DBMS)** is software used to create, store, retrieve, update and manage databases.

Examples:

- MySQL
- PostgreSQL
- Oracle Database
- Microsoft SQL Server
- SQLite

### DBMS vs RDBMS

| DBMS | RDBMS |
|---|---|
| General database management system | Relational database management system |
| May use different data models | Stores data in related tables |
| Relationships depend on the system | Relationships can be enforced using foreign keys |
| May not support relational constraints | Supports relational constraints |

MySQL and PostgreSQL are examples of RDBMSs.

## 5. What is SQL?

**SQL (Structured Query Language)** is a language used to communicate with relational databases.

SQL is used to:

1. Create databases and tables.
2. Insert records.
3. Retrieve records.
4. Update and delete records.
5. Define relationships and constraints.
6. Manage transactions.
7. Optimize data retrieval.

Example:

```sql
SELECT * FROM students;
```

This retrieves every column and row from the `students` table.

## 6. How SQL works

A simplified query-processing flow:

1. The client sends an SQL query.
2. The database parses and validates the query.
3. The optimizer chooses an execution strategy.
4. The execution engine processes the query.
5. The database returns the result.

This is particularly relevant when you work with Java, JDBC and Spring Data JPA.

## 7. SQL command categories

SQL commands are commonly grouped into five categories.

| Category | Full form | Purpose |
|---|---|---|
| DDL | Data Definition Language | Defines database structure |
| DML | Data Manipulation Language | Inserts, updates and deletes data |
| DQL | Data Query Language | Retrieves data |
| DCL | Data Control Language | Controls permissions |
| TCL | Transaction Control Language | Manages transactions |

Examples:

| Category | Commands |
|---|---|
| DDL | `CREATE`, `ALTER`, `DROP`, `TRUNCATE` |
| DML | `INSERT`, `UPDATE`, `DELETE` |
| DQL | `SELECT` |
| DCL | `GRANT`, `REVOKE` |
| TCL | `COMMIT`, `ROLLBACK`, `SAVEPOINT` |

---

# Part 2 — Creating Databases and Tables

## 8. Create a database

A database is a container for related tables and other database objects.

```sql
CREATE DATABASE company_db;

-- Select the database
USE company_db;

-- List available databases
SHOW DATABASES;

-- Delete a database
DROP DATABASE company_db;
```

> **Important:** `DROP DATABASE` permanently removes the database and its objects. Do not execute it on production data without appropriate safeguards.

## 9. SQL data types

A data type determines what kind of value a column can store.

### Numeric data types

| Data type | Purpose | Example |
|---|---|---|
| `INT` | Integer | 100 |
| `BIGINT` | Large integer | 9876543210 |
| `SMALLINT` | Small integer | 100 |
| `DECIMAL(10,2)` | Exact decimal | 12500.50 |
| `FLOAT` | Approximate decimal | 10.25 |
| `DOUBLE` | Higher-precision approximate decimal | 123.456789 |

**What does `DECIMAL(10,2)` mean?**

- `10` = Maximum total digits.
- `2` = Digits after the decimal point.
- Therefore, up to 8 digits can be before the decimal point.

Example:

```sql
salary DECIMAL(10,2)
```

This is suitable for storing salary and financial values because decimal arithmetic is exact within the declared precision.

### String data types

| Data type | Purpose |
|---|---|
| `CHAR(10)` | Fixed-length string |
| `VARCHAR(100)` | Variable-length string |
| `TEXT` | Large text |
| `LONGTEXT` | Very large text |

Example:

```sql
name VARCHAR(100),
gender CHAR(1),
description TEXT
```

### Date and time data types

| Data type | Example |
|---|---|
| `DATE` | 2026-11-09 |
| `TIME` | 14:30:00 |
| `DATETIME` | 2026-11-09 14:30:00 |
| `TIMESTAMP` | 2026-11-09 14:30:00 |

### Other data types

- `BOOLEAN`: Boolean-style values; in MySQL, this is an alias for `TINYINT(1)`.
- `JSON`: Stores JSON data.
- `BLOB`: Stores binary data.

> **Interview point:** Use `DECIMAL` rather than `FLOAT` for financial values, because floating-point numbers can introduce precision errors.

## 10. Create tables

We will use a **company database** throughout the course to practise SQL.

### Table structure

**departments**

| dept_id (PK) | dept_name |
|---|---|
| 1 | Engineering |
| 2 | HR |
| 3 | Sales |

**employees**

| emp_id (PK) | emp_name | salary | dept_id (FK) |
|---|---|---|---|
| 101 | Amit | 75000 | 1 |
| 102 | Rahul | 60000 | 1 |
| 103 | Priya | 50000 | 2 |
| 104 | Neha | 80000 | 3 |
| 105 | Karan | 65000 | 1 |

PK = Primary Key · FK = Foreign Key

First, create the `departments` table:

```sql
CREATE TABLE departments (
    dept_id INT PRIMARY KEY AUTO_INCREMENT,
    dept_name VARCHAR(100) NOT NULL UNIQUE
);
```

Create the `employees` table:

```sql
CREATE TABLE employees (
    emp_id INT PRIMARY KEY AUTO_INCREMENT,
    emp_name VARCHAR(100) NOT NULL,
    email VARCHAR(150) UNIQUE,
    salary DECIMAL(10,2),
    dept_id INT,
    manager_id INT,
    hire_date DATE,
    city VARCHAR(50),
    FOREIGN KEY (dept_id)
        REFERENCES departments(dept_id),
    FOREIGN KEY (manager_id)
        REFERENCES employees(emp_id)
);
```

Notice two relationships:

- `dept_id` connects an employee to a department.
- `manager_id` connects an employee to another employee.

The second relationship is called a **self-referencing foreign key**.

### Insert sample data

```sql
INSERT INTO departments (dept_id, dept_name)
VALUES
(1, 'Engineering'),
(2, 'HR'),
(3, 'Sales'),
(4, 'Marketing'),
(5, 'Finance');
```

```sql
INSERT INTO employees
(emp_id, emp_name, email, salary, dept_id,
 manager_id, hire_date, city)
VALUES
(101, 'Amit', 'amit@company.com', 75000, 1, NULL, '2023-01-15', 'Pune'),
(102, 'Rahul', 'rahul@company.com', 60000, 1, 101, '2023-05-20', 'Mumbai'),
(103, 'Priya', 'priya@company.com', 50000, 2, NULL, '2024-02-10', 'Pune'),
(104, 'Neha', 'neha@company.com', 80000, 3, NULL, '2022-08-12', 'Delhi'),
(105, 'Karan', 'karan@company.com', 65000, 1, 101, '2024-06-01', 'Pune'),
(106, 'Sneha', 'sneha@company.com', 55000, 2, 103, '2025-01-11', 'Mumbai'),
(107, 'Rohit', 'rohit@company.com', 90000, NULL, NULL, '2021-03-15', 'Bangalore'),
(108, 'Anjali', 'anjali@company.com', 70000, 3, 104, '2023-09-09', 'Delhi');
```

Check the inserted records:

```sql
SELECT * FROM departments;
SELECT * FROM employees;
```

These two tables will be used for almost every example in this course.

## 11. DDL commands

DDL commands define or change the database structure.

### A. CREATE

Creates a database object.

```sql
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(100)
);
```

### B. ALTER

Changes the structure of an existing table.

Add a column:

```sql
ALTER TABLE employees
ADD age INT;
```

Modify a column in MySQL:

```sql
ALTER TABLE employees
MODIFY emp_name VARCHAR(150);
```

Rename a column in MySQL:

```sql
ALTER TABLE employees
RENAME COLUMN emp_name TO employee_name;
```

Delete a column:

```sql
ALTER TABLE employees
DROP COLUMN age;
```

### C. DROP

Deletes the entire table, including its structure and data.

```sql
DROP TABLE students;
```

### D. TRUNCATE

Removes all records while retaining the table structure.

```sql
TRUNCATE TABLE employees;
```

### DELETE vs TRUNCATE vs DROP

| Feature | DELETE | TRUNCATE | DROP |
|---|---|---|---|
| Removes rows | Yes | All rows | All rows |
| Removes structure | No | No | Yes |
| WHERE supported | Yes | No | No |
| Can remove selected rows | Yes | No | No |
| Resets auto-increment in MySQL | No | Yes | Table removed |
| Typical use | Selective removal | Empty a table | Remove a table |

> In MySQL, `TRUNCATE` is DDL-like and causes an implicit commit. It is not generally rollback-able like a transactional `DELETE`.

---

# Part 3 — DML and DQL

## 12. INSERT command

`INSERT` adds new records to a table.

### Insert one record

```sql
INSERT INTO employees
(emp_id, emp_name, salary, dept_id, city)
VALUES
(109, 'Vikas', 45000, 1, 'Pune');
```

### Insert multiple records

```sql
INSERT INTO departments (dept_id, dept_name)
VALUES
(6, 'Support'),
(7, 'Research');
```

### Insert records from another table

```sql
INSERT INTO employee_backup
SELECT *
FROM employees;
```

The destination table must have a compatible column structure. In production, explicitly listing destination columns is safer.

## 13. UPDATE command

`UPDATE` modifies existing records.

```sql
UPDATE employees
SET salary = 70000
WHERE emp_id = 102;
```

Increase salaries by 10%:

```sql
UPDATE employees
SET salary = salary * 1.10
WHERE dept_id = 1;
```

Update multiple columns:

```sql
UPDATE employees
SET salary = 85000,
    city = 'Pune'
WHERE emp_id = 104;
```

> **Important:** Always check the `WHERE` condition before executing an update. Without it, every row may be updated.

```sql
-- Check the target records first
SELECT *
FROM employees
WHERE emp_id = 102;
```

## 14. DELETE command

`DELETE` removes records from a table.

Delete one employee:

```sql
DELETE FROM employees
WHERE emp_id = 109;
```

Delete employees earning less than ₹40,000:

```sql
DELETE FROM employees
WHERE salary < 40000;
```

Delete all rows:

```sql
DELETE FROM employees;
```

The table structure remains intact.

## 15. SELECT command

`SELECT` retrieves records from a database.

### Retrieve all columns

```sql
SELECT * FROM employees;
```

### Retrieve selected columns

```sql
SELECT emp_name, salary
FROM employees;
```

### Retrieve distinct values

```sql
SELECT DISTINCT city
FROM employees;
```

This returns each city only once.

### Column aliases

```sql
SELECT
    emp_name AS employee,
    salary AS monthly_salary
FROM employees;
```

Aliases make result columns easier to understand.

---

# Part 4 — Filtering, Operators and Sorting

## 16. WHERE clause

`WHERE` filters rows based on a condition.

Employees earning more than ₹60,000:

```sql
SELECT *
FROM employees
WHERE salary > 60000;
```

Employees working in the Engineering department:

```sql
SELECT *
FROM employees
WHERE dept_id = 1;
```

### Comparison operators

| Operator | Meaning |
|---|---|
| `=` | Equal |
| `!=` or `<>` | Not equal |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal |
| `<=` | Less than or equal |

Example:

```sql
SELECT *
FROM employees
WHERE salary >= 60000;
```

## 17. Logical operators

### AND

Both conditions must be true.

```sql
SELECT *
FROM employees
WHERE salary > 60000
AND city = 'Pune';
```

### OR

At least one condition must be true.

```sql
SELECT *
FROM employees
WHERE city = 'Pune'
OR city = 'Mumbai';
```

### NOT

Negates a condition.

```sql
SELECT *
FROM employees
WHERE NOT dept_id = 1;
```

> Use parentheses when combining multiple `AND` and `OR` conditions to make the intended logic explicit.

## 18. BETWEEN operator

Checks whether a value falls within an inclusive range.

```sql
SELECT *
FROM employees
WHERE salary BETWEEN 50000 AND 75000;
```

Equivalent:

```sql
SELECT *
FROM employees
WHERE salary >= 50000
AND salary <= 75000;
```

Both endpoints are included.

## 19. IN operator

Checks whether a value matches any value in a specified list.

```sql
SELECT *
FROM employees
WHERE city IN ('Pune', 'Mumbai', 'Delhi');
```

Equivalent to:

```sql
WHERE city = 'Pune'
OR city = 'Mumbai'
OR city = 'Delhi'
```

### NOT IN

```sql
SELECT *
FROM employees
WHERE city NOT IN ('Pune', 'Mumbai');
```

> **Interview point:** `NOT IN` can behave unexpectedly if its list or subquery contains `NULL`. In many cases, `NOT EXISTS` is safer.

## 20. LIKE operator

Searches for text patterns using wildcards.

| Wildcard | Meaning |
|---|---|
| `%` | Zero or more characters |
| `_` | Exactly one character |

Names starting with A:

```sql
SELECT *
FROM employees
WHERE emp_name LIKE 'A%';
```

Names ending with a:

```sql
SELECT *
FROM employees
WHERE emp_name LIKE '%a';
```

Names containing `oh`:

```sql
SELECT *
FROM employees
WHERE emp_name LIKE '%oh%';
```

Names with exactly four characters:

```sql
SELECT *
FROM employees
WHERE emp_name LIKE '____';
```

## 21. IS NULL and IS NOT NULL

`NULL` represents a missing or unknown value.

Employees without a department:

```sql
SELECT *
FROM employees
WHERE dept_id IS NULL;
```

Employees with a department:

```sql
SELECT *
FROM employees
WHERE dept_id IS NOT NULL;
```

You should **not** write:

```sql
WHERE dept_id = NULL;
```

Use `IS NULL` instead.

### NULL-related concepts

```sql
SELECT
    emp_name,
    IFNULL(salary, 0) AS salary
FROM employees;
```

`IFNULL()` is MySQL-specific. The more portable alternative is:

```sql
SELECT
    emp_name,
    COALESCE(salary, 0) AS salary
FROM employees;
```

`COALESCE()` returns the first non-NULL value.

## 22. ORDER BY

Sorts the result.

Ascending order:

```sql
SELECT *
FROM employees
ORDER BY salary ASC;
```

Descending order:

```sql
SELECT *
FROM employees
ORDER BY salary DESC;
```

Multiple-column sorting:

```sql
SELECT *
FROM employees
ORDER BY dept_id ASC, salary DESC;
```

This sorts by department first, then by salary within each department.

## 23. LIMIT and OFFSET

`LIMIT` restricts the number of returned rows.

```sql
SELECT *
FROM employees
LIMIT 5;
```

Skip the first 5 records and return the next 3:

```sql
SELECT *
FROM employees
LIMIT 3 OFFSET 5;
```

### Find the second-highest distinct salary

```sql
SELECT DISTINCT salary
FROM employees
ORDER BY salary DESC
LIMIT 1 OFFSET 1;
```

This is a frequently asked SQL interview problem. We will also solve it using subqueries and window functions later.

---

# Part 5 — Constraints and Keys

## 24. What are SQL constraints?

Constraints are rules applied to table columns to maintain data integrity.

| Constraint | Purpose |
|---|---|
| `PRIMARY KEY` | Uniquely identifies a row |
| `FOREIGN KEY` | Enforces a relationship with another table |
| `UNIQUE` | Prevents duplicate values |
| `NOT NULL` | Prevents NULL values |
| `CHECK` | Validates a condition |
| `DEFAULT` | Supplies a default value |

### A. PRIMARY KEY

A primary key uniquely identifies each row.

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(100)
);
```

Properties:

- Must contain unique values.
- Cannot contain NULL.
- A table has one primary-key constraint, which may contain multiple columns.

### B. FOREIGN KEY

A foreign key creates a relationship with another table.

```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    FOREIGN KEY (customer_id)
        REFERENCES customers(customer_id)
);
```

The referenced customer must exist for a valid foreign-key value, unless the foreign-key column is NULL and the constraint permits it.

### C. UNIQUE

Prevents duplicate values.

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    email VARCHAR(150) UNIQUE
);
```

**Primary key vs UNIQUE:**

| Primary Key | UNIQUE |
|---|---|
| Identifies each row | Prevents duplicate values |
| Cannot be NULL | NULL behavior depends on DBMS |
| One constraint per table | Multiple constraints per table |
| Creates a unique index in MySQL | Creates a unique index in MySQL |

MySQL permits multiple NULL values in a unique index, subject to the column definition.

### D. NOT NULL

```sql
CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL
);
```

The `product_name` column must have a value.

### E. CHECK

```sql
CREATE TABLE accounts (
    account_id INT PRIMARY KEY,
    balance DECIMAL(10,2),
    CHECK (balance >= 0)
);
```

The database rejects rows that violate the check constraint. MySQL enforces CHECK constraints in modern versions (8.0.16 and later).

### F. DEFAULT

```sql
CREATE TABLE employees_demo (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    city VARCHAR(50) DEFAULT 'Pune'
);
```

When `city` is omitted during insertion, it defaults to `Pune`.

## 25. Types of keys in DBMS

| Key | Meaning |
|---|---|
| Super Key | Any set of attributes that uniquely identifies a row |
| Candidate Key | Minimal super key |
| Primary Key | Candidate key selected as the main identifier |
| Alternate Key | Candidate key not selected as primary |
| Foreign Key | Attribute referencing another table's key |
| Composite Key | Key consisting of multiple columns |

Example:

```sql
CREATE TABLE enrollment (
    student_id INT,
    course_id INT,
    enrollment_date DATE,
    PRIMARY KEY (student_id, course_id)
);
```

Here, `(student_id, course_id)` is a composite primary key. The same student cannot enroll in the same course twice, assuming this key design.

---

# Part 6 — Aggregate Functions and GROUP BY

## 26. Aggregate functions

Aggregate functions perform calculations on multiple rows and return a single result per group or for the complete result set.

| Function | Purpose |
|---|---|
| `COUNT()` | Counts rows or non-NULL values |
| `SUM()` | Calculates total |
| `AVG()` | Calculates average |
| `MIN()` | Finds minimum |
| `MAX()` | Finds maximum |

### A. COUNT()

Count all employees:

```sql
SELECT COUNT(*)
FROM employees;
```

Count employees with a non-NULL salary:

```sql
SELECT COUNT(salary)
FROM employees;
```

Count unique cities:

```sql
SELECT COUNT(DISTINCT city)
FROM employees;
```

Important difference:

- `COUNT(*)` counts rows.
- `COUNT(column)` counts only rows where that column is not NULL.
- `COUNT(DISTINCT column)` counts unique non-NULL values.

### B. SUM()

```sql
SELECT SUM(salary)
FROM employees;
```

### C. AVG()

```sql
SELECT AVG(salary)
FROM employees;
```

### D. MIN() and MAX()

```sql
SELECT
    MIN(salary) AS minimum_salary,
    MAX(salary) AS maximum_salary
FROM employees;
```

## 27. GROUP BY

`GROUP BY` groups rows having the same value in one or more columns.

Example: Count employees in each department.

```sql
SELECT dept_id, COUNT(*) AS employee_count
FROM employees
GROUP BY dept_id;
```

Expected result:

| dept_id | employee_count |
|---|---|
| 1 | 3 |
| 2 | 2 |
| 3 | 2 |
| NULL | 1 |

Find average salary in each department:

```sql
SELECT
    dept_id,
    AVG(salary) AS average_salary
FROM employees
GROUP BY dept_id;
```

Find total salary for each city:

```sql
SELECT city, SUM(salary) AS total_salary
FROM employees
GROUP BY city;
```

### GROUP BY multiple columns

```sql
SELECT
    dept_id,
    city,
    COUNT(*) AS employee_count
FROM employees
GROUP BY dept_id, city;
```

This creates groups based on each unique department-city combination.

## 28. HAVING clause

`HAVING` filters groups after aggregation.

Find departments with more than two employees:

```sql
SELECT dept_id, COUNT(*) AS total_employees
FROM employees
GROUP BY dept_id
HAVING COUNT(*) > 2;
```

Find departments whose average salary is above ₹60,000:

```sql
SELECT dept_id, AVG(salary) AS avg_salary
FROM employees
GROUP BY dept_id
HAVING AVG(salary) > 60000;
```

### WHERE vs HAVING

| WHERE | HAVING |
|---|---|
| Filters individual rows | Filters groups |
| Applied before GROUP BY | Applied after GROUP BY |
| Commonly used without aggregate functions | Commonly used with aggregate functions |

Example:

```sql
SELECT dept_id, AVG(salary) AS avg_salary
FROM employees
WHERE salary > 40000
GROUP BY dept_id
HAVING AVG(salary) > 60000;
```

Here:

1. `WHERE` removes employees earning ₹40,000 or less.
2. `GROUP BY` groups the remaining employees.
3. `AVG()` calculates the average salary per department.
4. `HAVING` retains groups whose average exceeds ₹60,000.

---

# Part 7 — SQL JOIN Operations

## 29. What is a JOIN?

A JOIN combines rows from two or more tables using a related column.

For example, the `employees` table stores `dept_id`, while the `departments` table stores `dept_name`. A JOIN allows us to retrieve employee and department details together.

## 30. INNER JOIN

Returns only the rows that have matching values in both tables.

```sql
SELECT
    e.emp_name,
    d.dept_name
FROM employees e
INNER JOIN departments d
    ON e.dept_id = d.dept_id;
```

Here, `e` and `d` are table aliases.

Employees without a department and departments without employees will not appear.

## 31. LEFT JOIN (LEFT OUTER JOIN)

Returns:

- All rows from the left table.
- Matching rows from the right table.
- NULL values for right-table columns when there is no match.

```sql
SELECT
    e.emp_name,
    d.dept_name
FROM employees e
LEFT JOIN departments d
    ON e.dept_id = d.dept_id;
```

Every employee appears, including Rohit, whose department is NULL.

### Important interview query

Find employees who do not belong to any valid department:

```sql
SELECT e.*
FROM employees e
LEFT JOIN departments d
    ON e.dept_id = d.dept_id
WHERE d.dept_id IS NULL;
```

## 32. RIGHT JOIN (RIGHT OUTER JOIN)

Returns all rows from the right table and matching rows from the left table.

```sql
SELECT
    e.emp_name,
    d.dept_name
FROM employees e
RIGHT JOIN departments d
    ON e.dept_id = d.dept_id;
```

All departments appear, including departments without employees.

## 33. FULL OUTER JOIN

Returns matching and unmatched rows from both tables.

MySQL does not support `FULL OUTER JOIN` directly. You can simulate it using `LEFT JOIN`, `RIGHT JOIN` and `UNION`.

```sql
SELECT e.emp_name, d.dept_name
FROM employees e
LEFT JOIN departments d
    ON e.dept_id = d.dept_id

UNION

SELECT e.emp_name, d.dept_name
FROM employees e
RIGHT JOIN departments d
    ON e.dept_id = d.dept_id;
```

## 34. CROSS JOIN

Returns the Cartesian product of two tables.

If table A contains 3 rows and table B contains 4 rows, the result has 3 × 4 = 12 rows.

```sql
SELECT
    e.emp_name,
    d.dept_name
FROM employees e
CROSS JOIN departments d;
```

This is useful when every combination is needed, such as generating all product-colour combinations.

## 35. SELF JOIN

A self join joins a table with itself.

For example, each employee has a manager, and the manager is also an employee.

Find employee names and their manager names:

```sql
SELECT
    e.emp_name AS employee,
    m.emp_name AS manager
FROM employees e
LEFT JOIN employees m
    ON e.manager_id = m.emp_id;
```

Here:

- `e` refers to the employee.
- `m` refers to the manager.

### JOIN comparison

| JOIN type | Matching rows | Unmatched left | Unmatched right |
|---|---|---|---|
| INNER JOIN | Yes | No | No |
| LEFT JOIN | Yes | Yes | No |
| RIGHT JOIN | Yes | No | Yes |
| FULL OUTER JOIN | Yes | Yes | Yes |
| CROSS JOIN | All combinations | N/A | N/A |
| SELF JOIN | Depends on condition | Depends | Depends |

## 36. Joining three tables

Suppose you have an additional `projects` table.

```sql
CREATE TABLE projects (
    project_id INT PRIMARY KEY,
    project_name VARCHAR(100)
);

CREATE TABLE employee_projects (
    emp_id INT,
    project_id INT,
    hours_worked INT,
    PRIMARY KEY (emp_id, project_id),
    FOREIGN KEY (emp_id) REFERENCES employees(emp_id),
    FOREIGN KEY (project_id) REFERENCES projects(project_id)
);
```

Find employees, departments and assigned projects:

```sql
SELECT
    e.emp_name,
    d.dept_name,
    p.project_name
FROM employees e
JOIN departments d
    ON e.dept_id = d.dept_id
JOIN employee_projects ep
    ON e.emp_id = ep.emp_id
JOIN projects p
    ON ep.project_id = p.project_id;
```

This type of multi-table query is common in backend applications and placement interviews.

---

# Part 8 — Subqueries

## 37. What is a subquery?

A subquery is a query nested inside another SQL query.

Example: Find employees earning more than the overall average salary.

```sql
SELECT *
FROM employees
WHERE salary > (
    SELECT AVG(salary)
    FROM employees
);
```

The inner query calculates the average salary. The outer query finds employees earning above that average.

## 38. Types of subqueries

### A. Scalar subquery

Returns a single value.

```sql
SELECT emp_name, salary
FROM employees
WHERE salary = (
    SELECT MAX(salary)
    FROM employees
);
```

This retrieves the employee or employees earning the maximum salary.

### B. Multiple-row subquery

Returns multiple rows.

```sql
SELECT *
FROM employees
WHERE dept_id IN (
    SELECT dept_id
    FROM departments
    WHERE dept_name IN ('Engineering', 'Sales')
);
```

### C. Correlated subquery

A correlated subquery depends on the current row of the outer query.

Find employees earning more than their department's average salary:

```sql
SELECT e.emp_name, e.salary, e.dept_id
FROM employees e
WHERE e.salary > (
    SELECT AVG(e2.salary)
    FROM employees e2
    WHERE e2.dept_id = e.dept_id
);
```

The inner query uses `e.dept_id` from the outer query. Conceptually, the subquery is evaluated with reference to each outer row.

## 39. EXISTS and NOT EXISTS

`EXISTS` checks whether a subquery returns at least one row.

Find departments having employees:

```sql
SELECT d.dept_name
FROM departments d
WHERE EXISTS (
    SELECT 1
    FROM employees e
    WHERE e.dept_id = d.dept_id
);
```

Find departments without employees:

```sql
SELECT d.dept_name
FROM departments d
WHERE NOT EXISTS (
    SELECT 1
    FROM employees e
    WHERE e.dept_id = d.dept_id
);
```

`SELECT 1` is commonly used because the database only needs to determine whether a matching row exists.

### IN vs EXISTS

| IN | EXISTS |
|---|---|
| Checks membership in a set | Checks whether matching rows exist |
| Can work with a list or subquery | Works with a subquery |
| NULL handling can be surprising, especially with `NOT IN` | Often easier to reason about for correlated existence checks |
| Optimizer may transform it into a semi-join | Optimizer may also transform it into a semi-join |

> Do not assume `EXISTS` is always faster than `IN`. Actual performance depends on the query, indexes, database engine and optimizer.

## 40. Second-highest salary using different approaches

Assume salary values are: `90000, 80000, 80000, 70000, 60000`

### Method 1: LIMIT and OFFSET

```sql
SELECT DISTINCT salary
FROM employees
ORDER BY salary DESC
LIMIT 1 OFFSET 1;
```

### Method 2: Subquery

```sql
SELECT MAX(salary)
FROM employees
WHERE salary < (
    SELECT MAX(salary)
    FROM employees
);
```

### Method 3: DENSE_RANK

```sql
SELECT salary
FROM (
    SELECT
        salary,
        DENSE_RANK() OVER (
            ORDER BY salary DESC
        ) AS rnk
    FROM employees
) ranked
WHERE rnk = 2;
```

All three approaches account for duplicate highest salaries and return the second-highest distinct salary.

---

# Part 9 — Set Operators and Conditional Logic

## 41. UNION

Combines the results of multiple `SELECT` queries and removes duplicate rows.

```sql
SELECT city FROM employees
UNION
SELECT dept_name FROM departments;
```

For a set operation:

- Each `SELECT` must return the same number of columns.
- Corresponding columns must have compatible data types.
- Result column names generally come from the first `SELECT`.

## 42. UNION ALL

Combines results while retaining duplicates.

```sql
SELECT city FROM employees
UNION ALL
SELECT city FROM employees;
```

### UNION vs UNION ALL

| UNION | UNION ALL |
|---|---|
| Removes duplicate rows | Retains duplicate rows |
| Usually requires duplicate elimination | Avoids that extra operation |
| Use when uniqueness is required | Use when all input rows are required |

## 43. CASE statement

`CASE` allows conditional logic inside a query.

Example: Categorize employees based on their salary.

```sql
SELECT
    emp_name,
    salary,
    CASE
        WHEN salary >= 80000 THEN 'High'
        WHEN salary >= 60000 THEN 'Medium'
        ELSE 'Low'
    END AS salary_category
FROM employees;
```

### Simple CASE

```sql
SELECT
    emp_name,
    CASE dept_id
        WHEN 1 THEN 'Engineering'
        WHEN 2 THEN 'HR'
        WHEN 3 THEN 'Sales'
        ELSE 'Other'
    END AS department
FROM employees;
```

### Conditional aggregation

Count employees by salary category:

```sql
SELECT
    SUM(CASE WHEN salary >= 80000 THEN 1 ELSE 0 END)
        AS high_salary_count,
    SUM(CASE WHEN salary < 80000 THEN 1 ELSE 0 END)
        AS other_salary_count
FROM employees;
```

Conditional aggregation is a very useful technique for reporting and analytics.

## 44. NULL-handling functions

| Function | Purpose |
|---|---|
| `COALESCE()` | Returns first non-NULL expression |
| `IFNULL()` | Replaces NULL with another value in MySQL |
| `NULLIF()` | Returns NULL when two expressions are equal |

Examples:

```sql
SELECT COALESCE(NULL, NULL, 'Default');
```

Result: `Default`.

```sql
SELECT NULLIF(100, 100);
```

Result: `NULL`.

> Avoid using `= NULL` or `!= NULL`. SQL uses three-valued logic: TRUE, FALSE and UNKNOWN. This also affects expressions involving NULL in filters and comparisons.

---

# Part 10 — CTEs (Common Table Expressions)

## 45. What is a CTE?

A Common Table Expression (CTE) is a named temporary result set that you can reference inside a SQL statement. It is declared using `WITH`.

Syntax:

```sql
WITH cte_name AS (
    SELECT column1, column2
    FROM table_name
    WHERE condition
)
SELECT *
FROM cte_name;
```

### Example 1: Employees earning more than ₹60,000

```sql
WITH high_salary_employees AS (
    SELECT *
    FROM employees
    WHERE salary > 60000
)
SELECT *
FROM high_salary_employees;
```

### Example 2: Department-wise average salary

```sql
WITH department_salary AS (
    SELECT
        dept_id,
        AVG(salary) AS avg_salary
    FROM employees
    GROUP BY dept_id
)
SELECT *
FROM department_salary
WHERE avg_salary > 60000;
```

### Example 3: Multiple CTEs

```sql
WITH department_count AS (
    SELECT dept_id, COUNT(*) AS total
    FROM employees
    GROUP BY dept_id
),
department_average AS (
    SELECT dept_id, AVG(salary) AS avg_salary
    FROM employees
    GROUP BY dept_id
)
SELECT
    dc.dept_id,
    dc.total,
    da.avg_salary
FROM department_count dc
JOIN department_average da
    ON dc.dept_id = da.dept_id;
```

### CTE vs Subquery vs Temporary Table

| CTE | Subquery | Temporary table |
|---|---|---|
| Defined using `WITH` | Nested inside another query | Created using `CREATE TEMPORARY TABLE` |
| Scoped to one SQL statement | Scoped to containing query | Usually lasts for the database session |
| Improves readability for complex queries | Useful for compact queries | Useful for reusing intermediate data across statements |
| May be inlined or materialized depending on optimizer | Optimized by the database | Stores intermediate results |

## 46. Recursive CTE

A recursive CTE refers to itself and is useful for hierarchical data.

Examples:

- Employee-manager hierarchy.
- Organization structure.
- Category trees.
- Graph traversal.

Find all employees reporting directly or indirectly to employee 101:

```sql
WITH RECURSIVE employee_hierarchy AS (
    -- Anchor query
    SELECT emp_id, emp_name, manager_id
    FROM employees
    WHERE emp_id = 101

    UNION ALL

    -- Recursive query
    SELECT e.emp_id, e.emp_name, e.manager_id
    FROM employees e
    JOIN employee_hierarchy eh
        ON e.manager_id = eh.emp_id
)
SELECT *
FROM employee_hierarchy;
```

How it works:

1. The anchor query selects the starting employee.
2. The recursive query finds employees reporting to the previous result.
3. The process repeats until no additional matching rows are found.

A recursive CTE should have a well-defined stopping condition or traversal limit to avoid runaway recursion.

---

# Part 11 — Window Functions

## 47. What is a window function?

A window function performs calculations across a set of related rows **without collapsing them** into a single row per group. This is a major topic for SQL interviews and analytics queries.

### GROUP BY vs Window Functions

| GROUP BY | Window function |
|---|---|
| Combines rows into groups | Keeps individual rows |
| Usually returns fewer rows | Normally preserves the input rows |
| Used for aggregate results | Used for ranking, running totals and comparisons |

For example:

```sql
SELECT dept_id, AVG(salary)
FROM employees
GROUP BY dept_id;
```

Returns one row per department.

But:

```sql
SELECT
    emp_name,
    dept_id,
    salary,
    AVG(salary) OVER (
        PARTITION BY dept_id
    ) AS dept_avg_salary
FROM employees;
```

Returns each employee along with their department's average salary.

## 48. ROW_NUMBER()

Assigns a unique sequential number to each row within a window.

```sql
SELECT
    emp_name,
    salary,
    ROW_NUMBER() OVER (
        ORDER BY salary DESC
    ) AS row_num
FROM employees;
```

Example ranking:

| Employee | Salary | Row number |
|---|---|---|
| Rohit | 90000 | 1 |
| Neha | 80000 | 2 |
| Amit | 75000 | 3 |

Even when salary values tie, `ROW_NUMBER()` assigns different numbers. Add a unique tie-breaker to `ORDER BY` when deterministic ordering matters.

## 49. RANK()

Assigns equal ranks to tied rows and leaves gaps after ties.

```sql
SELECT
    emp_name,
    salary,
    RANK() OVER (
        ORDER BY salary DESC
    ) AS salary_rank
FROM employees;
```

## 50. DENSE_RANK()

Assigns equal ranks to tied rows but does not leave gaps.

```sql
SELECT
    emp_name,
    salary,
    DENSE_RANK() OVER (
        ORDER BY salary DESC
    ) AS salary_rank
FROM employees;
```

### ROW_NUMBER vs RANK vs DENSE_RANK

Suppose salaries are: `90000, 80000, 80000, 70000`

| Salary | ROW_NUMBER | RANK | DENSE_RANK |
|---|---|---|---|
| 90000 | 1 | 1 | 1 |
| 80000 | 2 | 2 | 2 |
| 80000 | 3 | 2 | 2 |
| 70000 | 4 | 4 | 3 |

> **Remember**
> - `ROW_NUMBER()` = Always unique sequence numbers.
> - `RANK()` = Ties receive equal rank; gaps follow.
> - `DENSE_RANK()` = Ties receive equal rank; no gaps follow.

## 51. PARTITION BY

Divides rows into logical groups for a window calculation.

Find employee salary ranking within each department:

```sql
SELECT
    emp_name,
    dept_id,
    salary,
    DENSE_RANK() OVER (
        PARTITION BY dept_id
        ORDER BY salary DESC
    ) AS dept_rank
FROM employees;
```

Here, ranking restarts for each department.

## 52. Running total

Calculate cumulative salary by hire date:

```sql
SELECT
    emp_name,
    hire_date,
    salary,
    SUM(salary) OVER (
        ORDER BY hire_date, emp_id
        ROWS BETWEEN UNBOUNDED PRECEDING
        AND CURRENT ROW
    ) AS running_total
FROM employees;
```

The `ROWS BETWEEN` clause defines the window frame. It specifies which rows participate in the calculation for each current row.

## 53. LAG and LEAD

These functions access values from previous or subsequent rows without performing a self join.

### LAG()

Gets a value from a previous row.

```sql
SELECT
    emp_name,
    salary,
    LAG(salary, 1) OVER (
        ORDER BY hire_date, emp_id
    ) AS previous_salary
FROM employees;
```

### LEAD()

Gets a value from a subsequent row.

```sql
SELECT
    emp_name,
    salary,
    LEAD(salary, 1) OVER (
        ORDER BY hire_date, emp_id
    ) AS next_salary
FROM employees;
```

## 54. Other useful window functions

| Function | Purpose |
|---|---|
| `FIRST_VALUE()` | Returns the first value in the window frame |
| `LAST_VALUE()` | Returns the last value in the window frame |
| `NTH_VALUE()` | Returns the nth value |
| `NTILE(n)` | Divides rows into approximately equal groups |
| `SUM() OVER()` | Calculates a windowed sum |
| `AVG() OVER()` | Calculates a windowed average |
| `COUNT() OVER()` | Calculates a windowed count |

Example: Divide employees into four salary groups.

```sql
SELECT
    emp_name,
    salary,
    NTILE(4) OVER (
        ORDER BY salary DESC
    ) AS salary_group
FROM employees;
```

## 55. Important interview problems using window functions

### Problem 1: Find the top 2 highest-paid employees in every department.

```sql
WITH ranked_employees AS (
    SELECT
        emp_id,
        emp_name,
        dept_id,
        salary,
        ROW_NUMBER() OVER (
            PARTITION BY dept_id
            ORDER BY salary DESC, emp_id
        ) AS rn
    FROM employees
    WHERE dept_id IS NOT NULL
)
SELECT *
FROM ranked_employees
WHERE rn <= 2;
```

Using `ROW_NUMBER()` returns at most two employees per department.

### Problem 2: Find all employees who earn the highest salary in their department.

```sql
WITH ranked_employees AS (
    SELECT
        emp_name,
        dept_id,
        salary,
        DENSE_RANK() OVER (
            PARTITION BY dept_id
            ORDER BY salary DESC
        ) AS rnk
    FROM employees
)
SELECT *
FROM ranked_employees
WHERE rnk = 1;
```

Using `DENSE_RANK()` retains all employees tied for the highest salary.

### Problem 3: Find employees earning more than the previous employee in hire-date order.

```sql
WITH employee_comparison AS (
    SELECT
        emp_name,
        salary,
        LAG(salary) OVER (
            ORDER BY hire_date, emp_id
        ) AS previous_salary
    FROM employees
)
SELECT *
FROM employee_comparison
WHERE salary > previous_salary;
```

---

# Part 12 — Views and Database Objects

## 56. What is a VIEW?

A view is a virtual table based on a stored SQL query.

```sql
CREATE VIEW high_salary_employees AS
SELECT emp_id, emp_name, salary
FROM employees
WHERE salary > 60000;
```

Query the view:

```sql
SELECT *
FROM high_salary_employees;
```

Update the definition:

```sql
CREATE OR REPLACE VIEW high_salary_employees AS
SELECT emp_id, emp_name, salary, dept_id
FROM employees
WHERE salary > 60000;
```

Delete a view:

```sql
DROP VIEW high_salary_employees;
```

### Advantages of views

- Hide unnecessary columns.
- Simplify complex queries.
- Provide a controlled data-access interface.
- Help maintain consistent query logic.

> **Important:** A normal view does not store an independent copy of its result. The database executes its underlying query when the view is queried.

## 57. Materialized View

A materialized view stores the result of a query physically and can be refreshed when the underlying data changes.

| Normal View | Materialized View |
|---|---|
| Stores query definition | Stores query result |
| Normally reflects current source data | May become stale until refreshed |
| Does not independently store result rows | Physically stores result rows |
| Supported in MySQL | Supported natively in PostgreSQL |

MySQL does not provide native materialized views. They can be approximated using summary tables and scheduled refresh jobs.

---

# Part 13 — Indexing and Query Optimization

## 58. What is an index?

An index is a data structure that helps the database find records efficiently without scanning every row.

Think of the index in a book: instead of reading the entire book to find a topic, you use the index to locate the relevant pages.

- Without a suitable index, the database may perform a **full table scan**.
- With a suitable index, the database may locate matching rows through an **index lookup**.

## 59. Create an index

```sql
CREATE INDEX idx_employee_salary
ON employees(salary);
```

MySQL can use this index for suitable queries:

```sql
SELECT *
FROM employees
WHERE salary = 75000;
```

## 60. Types of indexes

### A. Primary key index

Automatically created for the primary key in MySQL's InnoDB storage engine.

```sql
PRIMARY KEY (emp_id)
```

### B. Unique index

Ensures that indexed values are unique.

```sql
CREATE UNIQUE INDEX idx_email
ON employees(email);
```

### C. Single-column index

```sql
CREATE INDEX idx_city
ON employees(city);
```

### D. Composite index

An index on multiple columns.

```sql
CREATE INDEX idx_dept_salary
ON employees(dept_id, salary);
```

This is often useful for queries involving department filtering and salary ordering or filtering.

### E. Full-text index

Supports full-text search on suitable text columns.

```sql
CREATE FULLTEXT INDEX idx_employee_name
ON employees(emp_name);
```

Example:

```sql
SELECT *
FROM employees
WHERE MATCH(emp_name)
AGAINST ('Amit');
```

## 61. Composite index and leftmost-prefix rule

Suppose you create:

```sql
CREATE INDEX idx_dept_salary_city
ON employees(dept_id, salary, city);
```

The index is organized by the indexed column order. It is generally most useful for predicates involving:

- `dept_id`
- `dept_id` and `salary`
- `dept_id`, `salary` and `city`

A query only filtering on `salary` or `city` cannot generally use the full composite index as efficiently because it does not start with the leftmost indexed column.

This is known as the **leftmost-prefix principle**. Actual index usage depends on the query and optimizer.

## 62. EXPLAIN command

`EXPLAIN` shows the database's planned execution strategy.

```sql
EXPLAIN
SELECT *
FROM employees
WHERE salary = 75000;
```

In MySQL, you can also use:

```sql
EXPLAIN ANALYZE
SELECT *
FROM employees
WHERE salary = 75000;
```

`EXPLAIN ANALYZE` executes the query and reports actual execution information alongside the plan.

Pay attention to:

| Field | Meaning |
|---|---|
| `type` | Access method, such as `ALL`, `range`, `ref` or `const` |
| `key` | Index selected by the optimizer |
| `rows` | Estimated rows examined |
| `possible_keys` | Indexes that may be usable |
| `Extra` | Additional execution details |

## 63. SQL query optimization techniques

1. Avoid `SELECT *` when only a few columns are needed.
2. Create indexes on columns used frequently in selective filters and joins.
3. Avoid unnecessary indexes because writes also need to maintain them.
4. Use `EXPLAIN` to inspect query execution.
5. Avoid unnecessary functions on indexed columns in filtering conditions.
6. Filter data as early as possible where query semantics permit it.
7. Prefer appropriate JOINs instead of repeated application-side queries.
8. Use pagination for large result sets.
9. Avoid unnecessary sorting and duplicate elimination.
10. Check whether the query is returning more data than the application actually needs.

Example:

Less suitable for a standard index on `hire_date`:

```sql
SELECT *
FROM employees
WHERE YEAR(hire_date) = 2024;
```

Often more index-friendly:

```sql
SELECT *
FROM employees
WHERE hire_date >= '2024-01-01'
AND hire_date < '2025-01-01';
```

---

# Part 14 — Transactions and ACID Properties

## 64. What is a transaction?

A transaction is a logical unit of work containing one or more SQL operations.

For example, transferring ₹5,000 from Account A to Account B requires:

1. Deduct ₹5,000 from Account A.
2. Add ₹5,000 to Account B.

Both operations must succeed together. If either fails, the transaction should be rolled back.

## 65. Transaction commands (TCL)

### A. START TRANSACTION

```sql
START TRANSACTION;
```

### B. COMMIT

Permanently saves the transaction's changes.

```sql
START TRANSACTION;

UPDATE accounts
SET balance = balance - 5000
WHERE account_id = 1;

UPDATE accounts
SET balance = balance + 5000
WHERE account_id = 2;

COMMIT;
```

### C. ROLLBACK

Undoes uncommitted changes.

```sql
START TRANSACTION;

UPDATE employees
SET salary = 100000
WHERE emp_id = 101;

ROLLBACK;
```

After rollback, the transaction's salary update is undone.

### D. SAVEPOINT

Creates a point within a transaction to which you can return.

```sql
START TRANSACTION;

UPDATE employees
SET salary = salary + 5000
WHERE dept_id = 1;

SAVEPOINT first_update;

UPDATE employees
SET salary = salary + 10000
WHERE dept_id = 2;

ROLLBACK TO SAVEPOINT first_update;

COMMIT;
```

The second update is undone; the first update remains and is committed.

## 66. ACID properties

ACID represents the four properties of reliable database transactions.

| Letter | Property | Meaning |
|---|---|---|
| **A** | Atomicity | All operations succeed together, or all are rolled back. |
| **C** | Consistency | A transaction preserves database constraints and valid states. |
| **I** | Isolation | Concurrent transactions should not interfere in ways prohibited by the selected isolation level. |
| **D** | Durability | Committed changes survive failures according to the database's durability guarantees. |

## 67. Transaction isolation levels

Isolation levels control how concurrent transactions interact with each other.

| Isolation level | Dirty reads | Non-repeatable reads | Phantom reads |
|---|---|---|---|
| Read Uncommitted | Possible | Possible | Possible |
| Read Committed | Prevented | Possible | Possible |
| Repeatable Read | Prevented | Prevented | Possible under the SQL standard |
| Serializable | Prevented | Prevented | Prevented |

The table describes the standard isolation-level guarantees. Database implementations can provide stronger protections for particular anomalies.

### Important concurrency problems

**1. Dirty read** — Transaction A reads data modified by transaction B before B commits. If B rolls back, A has read a value that was never committed.

**2. Non-repeatable read** — Transaction A reads the same row twice, but transaction B modifies and commits that row between the two reads. A may see different values.

**3. Phantom read** — Transaction A runs a query returning a set of rows. Transaction B inserts or deletes rows matching the same condition and commits. When A repeats the query, the result set may differ.

**4. Lost update** — Two transactions read the same value and independently calculate updates. One transaction's update can overwrite the other's change.

## 68. Locks in databases

Locks control access to data during concurrent transactions.

| Lock | Purpose |
|---|---|
| Shared lock | Allows multiple transactions to read protected data |
| Exclusive lock | Prevents conflicting access while data is modified |

Example: Lock a selected account row for an update.

```sql
START TRANSACTION;

SELECT balance
FROM accounts
WHERE account_id = 1
FOR UPDATE;

UPDATE accounts
SET balance = balance - 500
WHERE account_id = 1;

COMMIT;
```

`FOR UPDATE` requests an exclusive lock on selected rows in MySQL's InnoDB engine.

### What is a deadlock?

A deadlock occurs when two or more transactions wait for each other to release resources.

Example:

- Transaction A locks Row 1 and requests Row 2.
- Transaction B locks Row 2 and requests Row 1.
- Neither can proceed.

The database detects the deadlock and typically aborts one transaction so the other can continue.

> **Interview point:** Applications should be prepared to retry a transaction that fails because of a deadlock.

---

# Part 15 — Database Normalization

## 69. What is normalization?

Normalization is the process of organizing relational tables to reduce redundancy and prevent data anomalies.

Consider this table:

| Student ID | Student Name | Course 1 | Course 2 |
|---|---|---|---|
| 1 | Amit | SQL | Java |
| 2 | Rahul | Python | SQL |

Problems:

- Multiple course columns.
- Difficult to add an arbitrary number of courses.
- Filtering and updating individual courses becomes inconvenient.

Normalization solves these structural problems.

## 70. First Normal Form (1NF)

A table satisfies 1NF when each cell stores a single atomic value and rows can be uniquely identified.

**Bad design:**

| Student ID | Student Name | Courses |
|---|---|---|
| 1 | Amit | SQL, Java |
| 2 | Rahul | Python, SQL |

**Better design:**

| Student ID | Student Name | Course |
|---|---|---|
| 1 | Amit | SQL |
| 1 | Amit | Java |
| 2 | Rahul | Python |
| 2 | Rahul | SQL |

Each cell contains one value.

## 71. Second Normal Form (2NF)

A table must:

1. Satisfy 1NF.
2. Have no partial dependency of a non-key attribute on part of a candidate key.

Consider:

| Student ID | Course ID | Student Name | Course Name |
|---|---|---|---|
| 1 | 101 | Amit | SQL |
| 1 | 102 | Amit | Java |
| 2 | 101 | Rahul | SQL |

Suppose the composite key is `(Student ID, Course ID)`.

Dependencies:

- Student ID determines Student Name.
- Course ID determines Course Name.

These attributes depend on only part of the composite key. Split the table into:

**Students**

| Student ID | Student Name |
|---|---|
| 1 | Amit |
| 2 | Rahul |

**Courses**

| Course ID | Course Name |
|---|---|
| 101 | SQL |
| 102 | Java |

**Enrollments**

| Student ID | Course ID |
|---|---|
| 1 | 101 |
| 1 | 102 |
| 2 | 101 |

Now partial dependencies have been removed.

## 72. Third Normal Form (3NF)

A table must:

1. Satisfy 2NF.
2. Have no transitive dependency of a non-key attribute on a candidate key.

Consider:

| Employee ID | Employee Name | Dept ID | Dept Name |
|---|---|---|---|
| 101 | Amit | 1 | Engineering |
| 102 | Rahul | 1 | Engineering |
| 103 | Priya | 2 | HR |

Dependencies:

- Employee ID determines Department ID.
- Department ID determines Department Name.

Therefore, Employee ID indirectly determines Department Name. Separate it into:

**Employees**

| Employee ID | Employee Name | Dept ID |
|---|---|---|
| 101 | Amit | 1 |
| 102 | Rahul | 1 |
| 103 | Priya | 2 |

**Departments**

| Dept ID | Dept Name |
|---|---|
| 1 | Engineering |
| 2 | HR |

## 73. BCNF (Boyce–Codd Normal Form)

A relation is in BCNF when every determinant of a non-trivial functional dependency is a super key.

BCNF is stronger than 3NF and addresses certain anomalies that can still remain in 3NF.

For placements, understand:

- Functional dependencies.
- Candidate keys and super keys.
- Partial dependencies.
- Transitive dependencies.
- Why BCNF is stronger than 3NF.

## 74. Normalization vs denormalization

| Normalization | Denormalization |
|---|---|
| Reduces redundancy | Intentionally introduces redundancy |
| Improves data consistency | Can improve read performance |
| Often requires additional joins | Can reduce the number of joins |
| Useful for transactional systems | Useful in reporting and analytical workloads |

> **Backend interview point:** Normalized schemas are often a good starting point for transactional applications. Denormalization can be introduced when measured performance requirements justify it.

---

# Part 16 — Stored Procedures, Functions and Triggers

## 75. Stored procedure

A stored procedure is a named collection of SQL statements stored in the database and executed when called.

```sql
DELIMITER //

CREATE PROCEDURE GetAllEmployees()
BEGIN
    SELECT * FROM employees;
END //

DELIMITER ;
```

Execute it:

```sql
CALL GetAllEmployees();
```

### Stored procedure with parameters

```sql
DELIMITER //

CREATE PROCEDURE GetEmployeesByDept(
    IN department_id INT
)
BEGIN
    SELECT *
    FROM employees
    WHERE dept_id = department_id;
END //

DELIMITER ;
```

Call it:

```sql
CALL GetEmployeesByDept(1);
```

`IN` is for input parameters. Other parameter modes include `OUT` and `INOUT`.

## 76. Stored function

A stored function returns a value.

```sql
DELIMITER //

CREATE FUNCTION AnnualSalary(
    monthly_salary DECIMAL(10,2)
)
RETURNS DECIMAL(12,2)
DETERMINISTIC
BEGIN
    RETURN monthly_salary * 12;
END //

DELIMITER ;
```

Use it:

```sql
SELECT
    emp_name,
    AnnualSalary(salary) AS annual_salary
FROM employees;
```

### Procedure vs Function

| Stored Procedure | Stored Function |
|---|---|
| Executed using `CALL` in MySQL | Used in an expression |
| May return result sets and output parameters | Must return a value |
| Can perform multiple operations | Generally designed to calculate or return values |
| Cannot be used directly as a scalar expression | Can be used inside `SELECT` expressions |

The restrictions on functions and procedures vary between database systems.

## 77. Triggers

A trigger is a database program that automatically executes when a specified database event occurs.

Common trigger events:

- `INSERT`
- `UPDATE`
- `DELETE`

Types:

- `BEFORE INSERT`
- `AFTER INSERT`
- `BEFORE UPDATE`
- `AFTER UPDATE`
- `BEFORE DELETE`
- `AFTER DELETE`

Example: Automatically store salary changes in an audit table.

Create the audit table:

```sql
CREATE TABLE salary_audit (
    audit_id INT PRIMARY KEY AUTO_INCREMENT,
    emp_id INT,
    old_salary DECIMAL(10,2),
    new_salary DECIMAL(10,2),
    changed_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

Create the trigger:

```sql
DELIMITER //

CREATE TRIGGER after_salary_update
AFTER UPDATE ON employees
FOR EACH ROW
BEGIN
    IF OLD.salary <> NEW.salary
       OR (OLD.salary IS NULL AND NEW.salary IS NOT NULL)
       OR (OLD.salary IS NOT NULL AND NEW.salary IS NULL)
    THEN
        INSERT INTO salary_audit
        (emp_id, old_salary, new_salary)
        VALUES
        (NEW.emp_id, OLD.salary, NEW.salary);
    END IF;
END //

DELIMITER ;
```

Update an employee:

```sql
UPDATE employees
SET salary = 95000
WHERE emp_id = 101;
```

The trigger automatically records the salary change.

### OLD and NEW

| Keyword | Meaning |
|---|---|
| `OLD` | Previous row values |
| `NEW` | New row values |

- In an `UPDATE` trigger, both `OLD` and `NEW` are available.
- In an `INSERT` trigger, `NEW` is available.
- In a `DELETE` trigger, `OLD` is available.

---

# Part 17 — Database Security and Administration

## 78. DCL commands

DCL stands for Data Control Language. It controls access to database objects.

### GRANT

Give a user `SELECT` permission:

```sql
GRANT SELECT
ON company_db.employees
TO 'app_user'@'localhost';
```

Give `SELECT` and `INSERT` permissions:

```sql
GRANT SELECT, INSERT
ON company_db.employees
TO 'app_user'@'localhost';
```

### REVOKE

Remove a permission:

```sql
REVOKE INSERT
ON company_db.employees
FROM 'app_user'@'localhost';
```

### Principle of least privilege

A database user should only receive the permissions necessary to perform its assigned tasks.

For example, a reporting application may need `SELECT` access but should not receive unrestricted `DELETE` or `DROP` permissions.

## 79. SQL Injection

SQL injection is a security vulnerability that occurs when untrusted input is incorporated into SQL statements in an unsafe way.

**Unsafe Java example:**

```java
String sql =
    "SELECT * FROM users WHERE username = '"
    + username + "'";
```

An attacker may provide specially crafted input to alter the meaning of the query.

### Prevention using PreparedStatement

```java
String sql =
    "SELECT * FROM users WHERE username = ?";

PreparedStatement ps =
    connection.prepareStatement(sql);

ps.setString(1, username);

ResultSet rs = ps.executeQuery();
```

Prepared statements separate SQL structure from user-provided values. This is an important SQL security topic for Java backend interviews.

---

# Part 18 — Important SQL Concepts for Interviews

## 80. Logical execution order of an SQL query

One of the most important concepts for understanding complex SQL queries is the logical order in which clauses are processed.

Consider:

```sql
SELECT dept_id, AVG(salary) AS avg_salary
FROM employees
WHERE salary > 40000
GROUP BY dept_id
HAVING AVG(salary) > 60000
ORDER BY avg_salary DESC
LIMIT 3;
```

Although `SELECT` is written first, it is not the first clause logically evaluated.

| Order | Clause | Purpose |
|---|---|---|
| 1 | `WITH` | Defines CTEs |
| 2 | `FROM` | Identifies source tables |
| 3 | `JOIN` / `ON` | Combines matching rows |
| 4 | `WHERE` | Filters rows |
| 5 | `GROUP BY` | Creates groups |
| 6 | `HAVING` | Filters groups |
| 7 | `SELECT` | Produces selected expressions |
| 8 | `DISTINCT` | Removes duplicate result rows |
| 9 | `ORDER BY` | Sorts the result |
| 10 | `LIMIT` / `OFFSET` | Restricts returned rows |

Window functions are evaluated as part of result-expression processing, after the relevant row filtering and grouping. They cannot normally be filtered directly in the same query's `WHERE` clause, which is why we often use a CTE or subquery.

### Why can't we use an aggregate function directly in WHERE?

This is **invalid**:

```sql
SELECT dept_id, AVG(salary)
FROM employees
WHERE AVG(salary) > 60000
GROUP BY dept_id;
```

Reason: `WHERE` filters individual records before grouping.

Correct:

```sql
SELECT dept_id, AVG(salary)
FROM employees
GROUP BY dept_id
HAVING AVG(salary) > 60000;
```

## 81. ON vs WHERE in JOINs

This is an important interview topic. Consider a `LEFT JOIN`.

**Filter in `ON`:**

```sql
SELECT d.dept_name, e.emp_name
FROM departments d
LEFT JOIN employees e
    ON d.dept_id = e.dept_id
    AND e.salary > 60000;
```

This retains all departments. Employees with salaries above ₹60,000 are matched; other departments still appear with NULL employee values.

**Filter in `WHERE`:**

```sql
SELECT d.dept_name, e.emp_name
FROM departments d
LEFT JOIN employees e
    ON d.dept_id = e.dept_id
WHERE e.salary > 60000;
```

This removes rows where the employee is NULL, so departments without a qualifying employee disappear.

> **Remember:** A condition placed in `WHERE` can turn an outer join into the equivalent of an inner join for that condition.

## 82. Clustered and non-clustered indexes

| Clustered index | Non-clustered index |
|---|---|
| Determines how table rows are organized in the storage structure | Separate index structure containing keys and row references |
| Typically one per table in systems using this organization | Multiple can exist |
| Leaf level contains table data in common clustered-index designs | Leaf level contains indexed keys and row locators or references |

In MySQL's InnoDB engine, the primary key is the clustered index. Secondary indexes also contain the primary-key value to locate rows.

In SQL Server, the clustered and non-clustered index terminology is especially prominent. Database engines differ in their physical implementations.

## 83. Foreign key actions

Foreign keys can define what happens when a referenced row is updated or deleted.

Example:

```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    FOREIGN KEY (customer_id)
        REFERENCES customers(customer_id)
        ON DELETE CASCADE
);
```

Common actions:

| Action | Meaning |
|---|---|
| `CASCADE` | Propagates deletion or update to related rows |
| `SET NULL` | Sets the referencing column to NULL |
| `RESTRICT` | Prevents the operation when dependent rows exist |
| `NO ACTION` | Rejects a violating operation according to the engine's constraint checking |
| `SET DEFAULT` | Sets a default value where supported |

> **Caution:** `ON DELETE CASCADE` can delete many dependent records automatically. Use it only when that behavior is appropriate for the data model.

## 84. SQL vs NoSQL

| SQL databases | NoSQL databases |
|---|---|
| Relational data model | Non-relational data models |
| Tables and relationships | Documents, key-value, graph, wide-column structures |
| Usually schema-defined | Often flexible schema |
| JOINs are a standard feature | Relationship handling depends on the database |
| Strong relational constraints | Consistency and transactions vary by database |
| Examples: MySQL, PostgreSQL | Examples: MongoDB, Redis, Cassandra |

SQL and NoSQL are not mutually exclusive choices. A backend application may use PostgreSQL for transactional data and Redis for caching.

---

# Part 19 — MySQL vs PostgreSQL

Both are relational database systems, but there are syntax and implementation differences.

| Feature | MySQL | PostgreSQL |
|---|---|---|
| Auto-generated integer ID | `AUTO_INCREMENT` | `GENERATED ... AS IDENTITY` |
| NULL replacement | `IFNULL()` | `COALESCE()` |
| String concatenation | `CONCAT()` | `CONCAT()` or `\|\|` |
| JSON support | `JSON` data type | `JSON` and `JSONB` |
| Full outer join | Not directly supported | Supported |
| `RETURNING` clause | Limited/command-dependent support | Broadly supported for DML |
| Default storage engine | InnoDB in modern installations | PostgreSQL storage engine |

### Auto-generated ID comparison

MySQL:

```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100)
);
```

PostgreSQL:

```sql
CREATE TABLE users (
    id INT GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
    name VARCHAR(100)
);
```

### NULL replacement

MySQL:

```sql
SELECT IFNULL(salary, 0)
FROM employees;
```

Portable alternative for both:

```sql
SELECT COALESCE(salary, 0)
FROM employees;
```

> **Learning recommendation:** Learn standard SQL concepts first, then learn the database-specific syntax of the system used by your application.

---

# Part 20 — SQL with Java and Spring Boot

Because SQL is commonly used in Java backend development, you should understand how your application interacts with the database.

## 85. JDBC architecture

JDBC stands for **Java Database Connectivity**. It provides Java APIs for connecting to relational databases and executing SQL queries.

Typical execution flow:

1. Java application requests a database connection.
2. JDBC driver communicates with the database.
3. Application creates a statement.
4. SQL is executed.
5. Results are processed using `ResultSet`.
6. Resources are closed.

## 86. JDBC example

```java
import java.sql.*;

public class Main {
    public static void main(String[] args) {

        String url = "jdbc:mysql://localhost:3306/company_db";
        String username = "root";
        String password = "your_password";

        String sql =
            "SELECT emp_name, salary FROM employees WHERE salary > ?";

        try (
            Connection con =
                DriverManager.getConnection(url, username, password);

            PreparedStatement ps =
                con.prepareStatement(sql)
        ) {
            ps.setBigDecimal(1, new java.math.BigDecimal("60000"));

            try (ResultSet rs = ps.executeQuery()) {
                while (rs.next()) {
                    System.out.println(rs.getString("emp_name"));
                    System.out.println(rs.getBigDecimal("salary"));
                }
            }

        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```

### JDBC interfaces

| Interface | Purpose |
|---|---|
| `DriverManager` | Obtains database connections |
| `Connection` | Represents a database connection |
| `Statement` | Executes static SQL |
| `PreparedStatement` | Executes parameterized SQL |
| `CallableStatement` | Calls stored procedures |
| `ResultSet` | Stores query results |

### Statement vs PreparedStatement

| Statement | PreparedStatement |
|---|---|
| Executes SQL statements | Executes parameterized SQL |
| Manual string construction may be needed | Uses placeholders |
| Vulnerable to injection when untrusted input is concatenated | Helps prevent SQL injection for bound parameters |
| Useful for static SQL | Preferred for application queries with parameters |

## 87. SQL in Spring Boot

Spring Boot provides database access through JDBC, Spring Data JPA and other persistence technologies.

For example, using Spring Data JPA:

```java
@Entity
@Table(name = "employees")
public class Employee {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer empId;

    private String empName;

    private BigDecimal salary;
}
```

Repository:

```java
@Repository
public interface EmployeeRepository
        extends JpaRepository<Employee, Integer> {

    List<Employee> findBySalaryGreaterThan(BigDecimal salary);
}
```

Custom SQL using a native query:

```java
@Query(
    value = "SELECT * FROM employees WHERE salary > :salary",
    nativeQuery = true
)
List<Employee> findHighSalaryEmployees(
    @Param("salary") BigDecimal salary
);
```

You should understand the distinction:

- **SQL** describes operations on relational database data.
- **JDBC** is the Java API for interacting with databases.
- **JPA** is a Java persistence specification.
- **Hibernate** is a common JPA implementation.
- **Spring Data JPA** simplifies repository and persistence operations.

---

# Part 21 — SQL Interview Preparation

## 88. Frequently asked conceptual questions

| No. | Interview question | Important concept |
|---|---|---|
| 1 | What is SQL? | SQL fundamentals |
| 2 | Difference between DBMS and RDBMS? | Database architecture |
| 3 | Difference between primary key and unique key? | Constraints |
| 4 | What is a foreign key? | Referential integrity |
| 5 | DELETE vs TRUNCATE vs DROP? | DDL and DML |
| 6 | Difference between WHERE and HAVING? | Filtering and grouping |
| 7 | What is a JOIN? | Relational operations |
| 8 | INNER JOIN vs LEFT JOIN? | Matching rows |
| 9 | What is a self join? | Hierarchical relationships |
| 10 | What is a correlated subquery? | Nested queries |
| 11 | IN vs EXISTS? | Subquery processing |
| 12 | UNION vs UNION ALL? | Set operations |
| 13 | What are aggregate functions? | Data aggregation |
| 14 | What is normalization? | Database design |
| 15 | What are 1NF, 2NF and 3NF? | Normal forms |
| 16 | What is an index? | Query performance |
| 17 | Clustered vs non-clustered indexes? | Index structures |
| 18 | What is a composite index? | Multi-column indexing |
| 19 | What is a transaction? | TCL |
| 20 | Explain ACID properties. | Transaction management |
| 21 | What are isolation levels? | Concurrency control |
| 22 | What is a deadlock? | Lock management |
| 23 | What is a view? | Database abstraction |
| 24 | What is a trigger? | Event-driven database logic |
| 25 | Stored procedure vs function? | Programmable SQL |
| 26 | What is a CTE? | Query composition |
| 27 | What are window functions? | Analytical SQL |
| 28 | ROW_NUMBER vs RANK vs DENSE_RANK? | Ranking |
| 29 | What is SQL injection? | Database security |
| 30 | How do you optimize a slow query? | Query optimization |

## 89. Must-solve SQL coding problems

Practise these problems using the company database created earlier.

### Beginner

| No. | Problem |
|---|---|
| 1 | Find all employees whose salary exceeds ₹60,000. |
| 2 | Find employees working in Pune. |
| 3 | Find employees whose names start with A. |
| 4 | Find the minimum and maximum salary. |
| 5 | Count employees in each department. |

### Intermediate

| No. | Problem |
|---|---|
| 6 | Find the second-highest distinct salary. |
| 7 | Find the third-highest distinct salary. |
| 8 | Find employees who do not belong to any department. |
| 9 | Find departments that do not have employees. |
| 10 | Find employees earning above the company average. |
| 11 | Find employees earning above their department average. |
| 12 | Find the highest-paid employee in each department. |
| 13 | Find departments having more than two employees. |
| 14 | Find employees who joined after 2023. |
| 15 | Find the number of employees in each city. |

### Advanced

| No. | Problem |
|---|---|
| 16 | Find the top two highest-paid employees per department. |
| 17 | Find duplicate email addresses. |
| 18 | Find the nth-highest distinct salary. |
| 19 | Find employees with the same salary. |
| 20 | Find employees who earn more than their managers. |
| 21 | Find the cumulative salary by hire date. |
| 22 | Rank employees within each department. |
| 23 | Find the salary difference from the previous employee. |
| 24 | Find departments whose average salary is above the company average. |
| 25 | Find the second-highest salary without using `LIMIT`. |

For these problems, practise multiple approaches: JOINs, subqueries, CTEs and window functions.

---

# Part 22 — Important Built-in SQL Functions

SQL provides many built-in functions for manipulating strings, dates, numbers and values.

## 90. String functions

| Function | Purpose | Example |
|---|---|---|
| `UPPER()` | Converts to uppercase | `UPPER('amit')` → AMIT |
| `LOWER()` | Converts to lowercase | `LOWER('AMIT')` → amit |
| `LENGTH()` | Returns string length in bytes in MySQL | `LENGTH('SQL')` → 3 |
| `CHAR_LENGTH()` | Returns number of characters | `CHAR_LENGTH('SQL')` → 3 |
| `CONCAT()` | Joins strings | `CONCAT('Hello',' SQL')` |
| `TRIM()` | Removes leading/trailing spaces | `TRIM(' SQL ')` |
| `SUBSTRING()` | Extracts part of a string | `SUBSTRING('Database',1,4)` |
| `REPLACE()` | Replaces text | `REPLACE('SQL Course','SQL','Java')` |
| `LEFT()` | Extracts leftmost characters | `LEFT('Database',4)` |
| `RIGHT()` | Extracts rightmost characters | `RIGHT('Database',4)` |

Example:

```sql
SELECT
    emp_name,
    UPPER(emp_name) AS uppercase_name,
    LENGTH(emp_name) AS name_length,
    CONCAT(emp_name, '@company.com') AS email
FROM employees;
```

## 91. Date and time functions

| Function | Purpose |
|---|---|
| `NOW()` | Current date and time |
| `CURRENT_DATE()` | Current date |
| `CURRENT_TIME()` | Current time |
| `YEAR()` | Extract year |
| `MONTH()` | Extract month |
| `DAY()` | Extract day |
| `DATEDIFF()` | Difference between dates in days |
| `DATE_ADD()` | Adds an interval to a date |
| `DATE_SUB()` | Subtracts an interval |
| `TIMESTAMPDIFF()` | Difference between two date/time values in a chosen unit |
| `DATE_FORMAT()` | Formats dates in MySQL |

Find employees hired in 2024:

```sql
SELECT *
FROM employees
WHERE hire_date >= '2024-01-01'
AND hire_date < '2025-01-01';
```

Find employees hired more than 365 days ago:

```sql
SELECT *
FROM employees
WHERE hire_date < DATE_SUB(CURRENT_DATE(), INTERVAL 365 DAY);
```

Calculate the number of days since each employee joined:

```sql
SELECT
    emp_name,
    DATEDIFF(CURRENT_DATE(), hire_date) AS days_worked
FROM employees;
```

Calculate experience in years approximately:

```sql
SELECT
    emp_name,
    TIMESTAMPDIFF(YEAR, hire_date, CURRENT_DATE())
        AS completed_years
FROM employees;
```

## 92. Mathematical functions

| Function | Purpose |
|---|---|
| `ROUND()` | Rounds a number |
| `CEIL()` | Rounds upward |
| `FLOOR()` | Rounds downward |
| `ABS()` | Absolute value |
| `MOD()` | Remainder |
| `POWER()` | Exponentiation |
| `SQRT()` | Square root |

Examples:

```sql
SELECT ROUND(125.678, 2);
SELECT CEIL(12.3);
SELECT FLOOR(12.9);
SELECT ABS(-100);
SELECT MOD(10, 3);
```

## 93. Type conversion

`CAST()` converts a value from one data type to another.

```sql
SELECT CAST('100' AS UNSIGNED);
```

Convert salary into a string:

```sql
SELECT
    CAST(salary AS CHAR) AS salary_text
FROM employees;
```

Use explicit conversion when combining or comparing values of different types.

---

# Part 23 — Advanced SQL Patterns for Backend Applications

## 94. UPSERT: Insert or update

UPSERT means inserting a record when it does not exist, or updating it when a unique-key conflict occurs.

MySQL:

```sql
INSERT INTO users (id, name, email)
VALUES (1, 'Amit', 'amit@example.com')
ON DUPLICATE KEY UPDATE
    name = 'Amit',
    email = 'amit@example.com';
```

PostgreSQL:

```sql
INSERT INTO users (id, name, email)
VALUES (1, 'Amit', 'amit@example.com')
ON CONFLICT (id)
DO UPDATE SET
    name = EXCLUDED.name,
    email = EXCLUDED.email;
```

This pattern is useful when building:

- User registration systems.
- Inventory management.
- Synchronization pipelines.
- Configuration storage.
- Data import processes.

## 95. Pagination

Suppose an API needs to return 20 employees at a time.

Page 1:

```sql
SELECT *
FROM employees
ORDER BY emp_id
LIMIT 20 OFFSET 0;
```

Page 2:

```sql
SELECT *
FROM employees
ORDER BY emp_id
LIMIT 20 OFFSET 20;
```

Page 3:

```sql
SELECT *
FROM employees
ORDER BY emp_id
LIMIT 20 OFFSET 40;
```

### Keyset pagination

For large datasets, deep `OFFSET` pagination can become expensive. An alternative is keyset pagination:

```sql
SELECT *
FROM employees
WHERE emp_id > 100
ORDER BY emp_id
LIMIT 20;
```

The application stores the last returned ID and supplies it in the next request. This can be more efficient when the pagination key is indexed and the ordering is stable.

---

# Part 24 — Capstone Project

## Project: E-commerce Database Management System

Build a relational database for an e-commerce application.

### Database design

Create these five tables:

| Table | Important columns |
|---|---|
| `customers` | customer_id, name, email, phone |
| `products` | product_id, name, price, stock |
| `orders` | order_id, customer_id, order_date, status |
| `order_items` | order_item_id, order_id, product_id, quantity, price |
| `payments` | payment_id, order_id, amount, payment_status |

### Required relationships

- One customer can place multiple orders.
- One order can contain multiple products.
- One product can appear in multiple orders.
- An order can have one or more payment records, depending on your payment model.

### Features to implement

**Level 1 — Database creation**

- Create the database.
- Create all five tables.
- Define primary keys and foreign keys.
- Add `NOT NULL`, `UNIQUE`, `CHECK` and `DEFAULT` constraints.
- Insert sample records.

**Level 2 — CRUD**

- Register customers.
- Add and update products.
- Update inventory.
- Create orders.
- Retrieve order history.
- Delete records safely.

**Level 3 — Reporting**

- Calculate total sales.
- Find the most expensive product.
- Find top-selling products.
- Find customers who have never placed an order.
- Calculate monthly revenue.
- Find the top five customers by spending.

**Level 4 — Advanced SQL**

- Find the second-highest-selling product.
- Rank products by revenue within each category.
- Find customers whose total spending exceeds average customer spending.
- Calculate monthly cumulative sales.
- Use CTEs to generate sales reports.
- Use window functions to find product rankings.

**Level 5 — Backend integration**

Integrate the database with a Spring Boot REST API.

Suggested endpoints:

| HTTP method | Endpoint | Function |
|---|---|---|
| POST | `/api/customers` | Create customer |
| GET | `/api/customers` | Retrieve customers |
| GET | `/api/products` | Retrieve products |
| POST | `/api/orders` | Place order |
| GET | `/api/orders/{id}` | Get order details |
| PUT | `/api/products/{id}` | Update product |
| GET | `/api/reports/monthly-sales` | Generate monthly report |

Implement order creation using **transactions** so that the order, order items and inventory changes remain consistent.

---

# Part 25 — Final Learning Checklist

Track your progress as you complete the course.

### 1. SQL fundamentals

- [ ] DBMS, RDBMS and SQL
- [ ] Database creation and data types
- [ ] DDL, DML, DQL, DCL and TCL

### 2. Query fundamentals

- [ ] SELECT, WHERE and DISTINCT
- [ ] Comparison and logical operators
- [ ] LIKE, BETWEEN, IN and NULL
- [ ] ORDER BY, LIMIT and OFFSET

### 3. Relational database design

- [ ] Primary, foreign and composite keys
- [ ] UNIQUE, CHECK and DEFAULT
- [ ] Relationships and referential integrity
- [ ] 1NF, 2NF, 3NF and BCNF

### 4. Intermediate SQL

- [ ] Aggregate functions
- [ ] GROUP BY and HAVING
- [ ] All JOIN types
- [ ] Subqueries and correlated subqueries
- [ ] UNION and UNION ALL
- [ ] CASE and NULL functions

### 5. Advanced SQL

- [ ] CTEs and recursive CTEs
- [ ] ROW_NUMBER, RANK and DENSE_RANK
- [ ] PARTITION BY and window frames
- [ ] LAG, LEAD and running totals
- [ ] Views and stored procedures
- [ ] Triggers and database functions

### 6. Database engineering

- [ ] Indexes and composite indexes
- [ ] EXPLAIN and query optimization
- [ ] ACID and isolation levels
- [ ] Locks and deadlocks
- [ ] SQL injection prevention
- [ ] Java JDBC and Spring Boot integration

### 7. Practical proficiency

- [ ] Solve 25 SQL coding problems
- [ ] Build the e-commerce database
- [ ] Write multi-table JOIN queries
- [ ] Implement transactions
- [ ] Integrate SQL with a REST API

---

## Recommended priority for software engineering placements

For your backend and Java interview preparation, I recommend this order:

| Priority | Topics | Importance |
|---|---|---|
| Very high | SELECT, WHERE, GROUP BY, HAVING | Must master |
| Very high | Joins and subqueries | Must master |
| Very high | Keys and constraints | Must master |
| Very high | Indexes and query optimization | Must master |
| Very high | ACID and transactions | Must master |
| High | CTEs and window functions | Strongly recommended |
| High | Normalization and database design | Strongly recommended |
| High | JDBC and SQL injection | Strongly recommended |
| Medium | Triggers, procedures and functions | Learn concepts and syntax |
