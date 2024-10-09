# SQL Query Task

## Objective
Delete employees from departments 1 and 2 from the `employees` table.

## SQL Query

```sql
DELETE FROM employees
WHERE department_id IN (2, 1);

