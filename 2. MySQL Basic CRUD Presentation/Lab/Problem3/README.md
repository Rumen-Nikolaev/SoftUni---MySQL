# SQL Query Task

## Objective
Update the salaries of employees with the job title "Manager" and then retrieve a sorted list of all employee salaries.

## SQL Queries

### 1. Update Salaries

```sql
UPDATE employees
SET salary = salary * 1.1
WHERE job_title = 'Manager';

