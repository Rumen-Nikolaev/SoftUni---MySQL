# SQL Query Task

## Objective
Retrieve the names and codes of countries along with a label indicating whether the country uses the Euro (`EUR`) as its currency or not. The results are sorted alphabetically by country name.

## SQL Query

```sql
SELECT 
    `country_name`,
    `country_code`,
    IF(`currency_code` = 'EUR',
        'Euro',
        'Not Euro') AS 'currency'
FROM
    `countries`
ORDER BY `country_name`;

