# SQL Query Task: Countries with at Least 3 Occurrences of 'a' in the Name

## Objective
The task is to retrieve all countries whose names contain the letter 'a' at least three times. The result is ordered by the ISO country code.

## SQL Query

```sql
SELECT 
    `country_name`, `iso_code`
FROM
    `countries`
WHERE
    (CHAR_LENGTH(`country_name`) - CHAR_LENGTH(REPLACE(LOWER(`country_name`), 'a', ''))) >= 3
ORDER BY `iso_code`;
