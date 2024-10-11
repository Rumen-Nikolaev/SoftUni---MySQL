# SQL Query Task: Retrieve Books with 'Harry Potter' in the Title

## Objective
Retrieve the titles of books from the `books` table that contain the phrase 'Harry Potter', and display them in ascending order based on their IDs.

## SQL Query

```sql
SELECT title
FROM books
WHERE title LIKE ('%Harry Potter%')
ORDER BY id;
