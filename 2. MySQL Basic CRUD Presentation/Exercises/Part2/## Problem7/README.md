# SQL Query Task

## Objective
Construct and display the full email addresses of employees by concatenating their first names, last names, and a domain.

## SQL Query

```sql
SELECT CONCAT(first_name, '.', last_name, '@softuni.bg') AS full_email_address
FROM employees;
