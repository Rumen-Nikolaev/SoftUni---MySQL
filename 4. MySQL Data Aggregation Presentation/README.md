# Data Aggregation

## How to Get Data Insights?

**SoftUni Team**  
**Technical Trainers**  
**Software University**  
[SoftUni Website](https://softuni.bg)

## Table of Contents
1. [Grouping](#grouping)
   - Consolidating data based on criteria
2. [Aggregate Functions](#aggregate-functions)
   - COUNT, SUM, MAX, MIN, AVG …
3. [Having](#having)
   - Using predicates while grouping
4. [Questions](#questions)
5. [Examples](#examples)

## Grouping
### Consolidating Data Based On Criteria
Grouping allows taking data into separate groups based on a common property.

**Example: Employees Table**
| Employee | Department        | Salary |
|----------|-------------------|--------|
| Adam     | Database Support   | 5,000  |
| John     | Database Support   | 15,000 |
| Jane     | Application Support| 10,000 |
| George   | Application Support| 15,000 |
| Lila     | Application Support| 5,000  |
| Fred     | Software Support   | 15,000 |

### GROUP BY
With `GROUP BY`, you can get each separate group and use an aggregate function over it (like Average, Min, or Max):

```sql
SELECT e.`job_title`, COUNT(employee_id)
FROM `employees` AS e
GROUP BY e.`job_title`;

