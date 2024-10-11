# SQL Query Task: Calculate Total Cost of Books

## Objective
Calculate the total cost of all books in the `books` table, rounding the result to two decimal places.

## SQL Query

```sql
SELECT
    ROUND(SUM(cost), 2) AS cost
FROM books;
