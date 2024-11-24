# LeetCode 595: Big Countries

## Problem Statement
Write a SQL query to report the `name`, `population`, and `area` of countries that:  
- Have a population of at least 25 million, or  
- Have an area of at least 3 million square kilometers.

The query should retrieve rows from the `World` table.

### Table: World

+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| name        | varchar |
| continent   | varchar |
| area        | int     |
| population  | int     |
| gdp         | bigint  |
+-------------+---------+

**Example Input:**

+-------------+-----------+---------+------------+--------------+
| name        | continent | area    | population | gdp          |
+-------------+-----------+---------+------------+--------------+
| Afghanistan | Asia      | 652230  | 25500100   | 20343000000  |
| Albania     | Europe    | 28748   | 2831741    | 12960000000  |
| Algeria     | Africa    | 2381741 | 37100000   | 188681000000 |
| Andorra     | Europe    | 468     | 78115      | 3712000000   |
| Angola      | Africa    | 1246700 | 20609294   | 100990000000 |
+-------------+-----------+---------+------------+--------------+

**Example Output:**

+-------------+------------+---------+
| name        | population | area    |
+-------------+------------+---------+
| Afghanistan | 25500100   | 652230  |
| Algeria     | 37100000   | 2381741 |
+-------------+------------+---------+

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
