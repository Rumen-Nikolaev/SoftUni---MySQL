# SQL Query Task: Find the Longest Magic Wand

## Objective
Retrieve the maximum size of the magic wand from the `wizzard_deposits` table.

## SQL Query

```sql
SELECT MAX(magic_wand_size) AS longest_magic_wand
FROM wizzard_deposits;
