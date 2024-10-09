# SQL Joins, Subqueries, and Indices

## Table of Contents
1. [Joins](#joins)
   - [Gathering Data From Multiple Tables](#gathering-data-from-multiple-tables)
   - [Types of Joins](#types-of-joins)
   - [Join Overview](#join-overview)
   - [Problem: Managers](#problem-managers)
2. [Subqueries](#subqueries)
   - [Query Manipulation on Multiple Levels](#query-manipulation-on-multiple-levels)
   - [Problem: Higher Salary](#problem-higher-salary)
3. [Indices](#indices)
   - [Clustered and Non-Clustered Indices](#clustered-and-non-clustered-indices)
4. [Summary](#summary)

## Joins

### Gathering Data From Multiple Tables
Sometimes you need to retrieve data from several tables. For example, consider the following tables:

- **Departments**
  | department_id | department_name |
  |---------------|------------------|
  | 3             | Sales            |
  | 4             | Marketing        |
  | 5             | Purchasing       |

- **Employees**
  | employee_name | department_id |
  |---------------|---------------|
  | Edward        | 3             |
  | John          | NULL          |

### Types of Joins
Joins are used to collect data from two or more tables. The main types of joins include:

- **INNER JOIN**: Matches records that exist in both tables.
- **LEFT JOIN**: Matches all entries in the left table regardless of whether they exist in the right.
- **RIGHT JOIN**: Matches all entries in the right table regardless of whether they exist in the left.
- **OUTER JOIN**: Returns all records from both tables, but this is not implemented in MySQL. Use a `UNION` of `LEFT` and `RIGHT JOIN`.
- **CROSS JOIN**: Produces a Cartesian product of the two tables, multiplying each row in the first table with each row in the second.

### Join Overview
#### INNER JOIN Example
```sql
SELECT students.name, courses.name
FROM students
INNER JOIN courses ON students.course_id = courses.id;

