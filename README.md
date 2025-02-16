# DBMS-1: Basic SQL Concepts

## Overview
DBMS-1 covers fundamental SQL concepts, including data retrieval, aggregation, and combining multiple tables. This guide provides an introduction to essential SQL operations like `JOIN`, `GROUP BY`, and more.

## Topics Covered

### 1. SQL Joins
Joins are used to retrieve data from multiple tables based on a related column.
- **INNER JOIN**: Returns matching records from both tables.
- **LEFT JOIN (OUTER JOIN)**: Returns all records from the left table and matching ones from the right table.
- **RIGHT JOIN (OUTER JOIN)**: Returns all records from the right table and matching ones from the left table.
- **FULL JOIN**: Returns all records from both tables, with `NULL` where there is no match.

**Example:**
```sql
SELECT customers.name, orders.order_id
FROM customers
INNER JOIN orders ON customers.customer_id = orders.customer_id;
```

### 2. GROUP BY and Aggregation
Used to group records and perform aggregate functions like `SUM()`, `COUNT()`, `AVG()`, `MIN()`, and `MAX()`.

**Example:**
```sql
SELECT department, COUNT(*) AS employee_count
FROM employees
GROUP BY department;
```

### 3. HAVING Clause
Filters grouped records based on aggregate conditions.

**Example:**
```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;
```

### 4. Subqueries
A subquery is a query within another query.

**Example:**
```sql
SELECT name, salary
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```

## Summary
This module covers the fundamental SQL operations required for querying and managing relational databases effectively. Understanding these concepts is crucial for working with structured data.

---

For advanced SQL topics like Triggers, Stored Procedures, and MongoDB, refer to **DBMS-2**.

