# SQL Query Task

## Objective
Retrieve all employees from department 4 who have a salary greater than or equal to $1600.00.

## SQL Query

```sql
SELECT * FROM employees
WHERE (department_id = 4 AND salary >= 1600.0)
ORDER BY id;

