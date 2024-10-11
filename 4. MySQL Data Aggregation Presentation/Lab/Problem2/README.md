# SQL Query Task: Minimum Deposit Charges by Group and Creator

## Objective
Retrieve the minimum deposit charge for each combination of deposit group and magic wand creator from the `wizzard_deposits` table.

## SQL Query

```sql
SELECT deposit_group, magic_wand_creator, MIN(deposit_charge) AS min_deposit_charge
FROM wizzard_deposits
GROUP BY deposit_group, magic_wand_creator
ORDER BY magic_wand_creator, deposit_group;
