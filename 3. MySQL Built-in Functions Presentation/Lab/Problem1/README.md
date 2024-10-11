# SQL Query Task: Calculate Days Lived by Authors

## Objective
Retrieve the full name of each author and calculate the total number of days they lived, based on their birth and death dates.

## SQL Query

```sql
SELECT 
    CONCAT_WS(' ', `first_name`, `last_name`) AS 'Full Name',
    TIMESTAMPDIFF(DAY, `born`, `died`) AS 'Days Lived'
FROM
    `authors`;
