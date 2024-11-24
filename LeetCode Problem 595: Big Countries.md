# LeetCode 595: Big Countries

## Problem Statement
Write a SQL query to report the `name`, `population`, and `area` of countries that:  
- Have a population of at least 25 million, or  
- Have an area of at least 3 million square kilometers.

The query should retrieve rows from the `World` table.

### Table: World

| Column       | Type    |
|--------------|---------|
| `name`       | varchar |
| `population` | int     |
| `area`       | int     |

**Example Input:**

| name       | population | area      |
|------------|------------|-----------|
| Afghanistan | 25500100   | 652230    |
| Algeria     | 37100000   | 2381741   |
| Andorra     | 84000      | 468       |
| Angola      | 12878000   | 1246700   |

**Example Output:**

| name       | population | area      |
|------------|------------|-----------|
| Afghanistan | 25500100   | 652230    |
| Algeria     | 37100000   | 2381741   |

---

### Refer the Question on [Leetcode.com](https://leetcode.com/problems/big-countries/description/?envType=study-plan-v2&envId=top-sql-50) 

## Solution

### SQL Query
```sql
SELECT name,
       population,
       area
FROM world
WHERE area >= 3000000
      OR population>= 25000000;
