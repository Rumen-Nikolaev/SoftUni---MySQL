# SQL View Creation Task

## Objective
Create a view named `v_employees_job_titles` that consolidates the full names of employees along with their job titles from the `employees` table.

## SQL Query

```sql
CREATE VIEW `v_employees_job_titles` AS
    SELECT 
        CONCAT(`first_name`,
                ' ',
                IFNULL(`middle_name`, ''),
                ' ',
                `last_name`) AS 'full_name',
        `job_title`
    FROM
        `employees`;
