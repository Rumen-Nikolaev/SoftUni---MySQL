# Database Programmability

## Table of Contents
1. [User-Defined Functions](#user-defined-functions)
2. [Stored Procedures](#stored-procedures)
3. [Transactions](#transactions)
4. [Triggers](#triggers)

## User-Defined Functions

User-defined functions extend the functionality of a MySQL server and promote modular programming by allowing you to write code once and call it multiple times. They improve execution speed as they do not need to be reparsed or reoptimized each time they are used. Functions can be categorized as:
- **Scalar Functions**: Return a single value or NULL.
- **Table-Valued Functions**: Return a table.

### Problem: Count Employees by Town
Write a function `ufn_count_employees_by_town(town_name)` that:
- Accepts a town name as a parameter.
- Returns the count of employees in the database who live in that town.

#### Solution:
```sql
CREATE FUNCTION ufn_count_employees_by_town(town_name VARCHAR(20))
RETURNS INT
DETERMINISTIC
BEGIN
    DECLARE e_count INT;
    SET e_count := (SELECT COUNT(employee_id) FROM employees AS e
                    JOIN addresses AS a ON a.address_id = e.address_id
                    JOIN towns AS t ON t.town_id = a.town_id
                    WHERE t.name = town_name);
    RETURN e_count;
END

