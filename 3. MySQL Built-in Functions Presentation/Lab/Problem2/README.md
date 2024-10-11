# SQL Query Task: Retrieve Books with Titles Starting with 'The'

## Objective
Retrieve the titles of books from the `books` table where the title starts with the substring 'The', and display them in ascending order based on their IDs.

## SQL Query

```sql
SELECT title 
FROM books
WHERE SUBSTRING(title, 1, 3) = 'The'
ORDER BY id;
