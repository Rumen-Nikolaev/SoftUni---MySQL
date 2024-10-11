# SQL Query Task: Longest Magic Wand Size

## Objective
Retrieve the size of the longest magic wand from the `wizzard_deposits` table.

## SQL Query

```sql
SELECT MAX(magic_wand_size) AS longest_magic_wand
FROM wizzard_deposits;
