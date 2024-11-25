# LeetCode Problem 1148: Article Views I

## Problem Statement
You are given a table called `Views` containing the following columns:

| Column       | Type    |
|--------------|---------|
| `article_id` | int     |
| `author_id`  | int     |
| `viewer_id`  | int     |
| `view_date`  | date    |

Note that equal author_id and viewer_id indicate the same person.
Write a solution to find all the authors that viewed at least one of their own articles.

### Example Input:
| article_id | author_id | viewer_id | view_date  |
|------------|-----------|-----------|------------|
| 1          | 3         | 5         | 2019-08-01 |
| 1          | 3         | 6         | 2019-08-02 |
| 2          | 7         | 7         | 2019-08-01 |
| 2          | 7         | 6         | 2019-08-02 |
| 4          | 7         | 1         | 2019-07-22 |
| 3          | 4         | 4         | 2019-07-21 |
| 3          | 4         | 4         | 2019-07-21 |

### Example Output:
| id |
|-----------|
| 4         |
| 7         |


---
 ## Solve the Question on [Leetcode.com](https://leetcode.com/problems/article-views-i/description/?envType=study-plan-v2&envId=top-sql-50)
 ---
 
## Solution

### SQL Query
```sql
SELECT DISTINCT(author_id) AS id
FROM views
WHERE author_id = viewer_id
ORDER BY id ASC;
```

---

## [Go to Leetcode SQL50 Questions](https://github.com/codelytix20/LeetCode-SQL50)
---
## [Watch Explaination video on Youtube](https://youtu.be/F9fL6GxB3LU)


