# LeetCode 1148: Article Views I

## Problem Statement
You are given a table called `Views` containing the following columns:

| Column       | Type    |
|--------------|---------|
| `article_id` | int     |
| `author_id`  | int     |
| `viewer_id`  | int     |
| `view_date`  | date    |

Write an SQL query to find all the authors who viewed their own articles. Return a list of `author_id` without duplicates.

### Example Input:
| article_id | author_id | viewer_id | view_date  |
|------------|-----------|-----------|------------|
| 1          | 3         | 5         | 2023-01-01 |
| 2          | 7         | 7         | 2023-01-02 |
| 3          | 7         | 10        | 2023-01-03 |
| 4          | 3         | 3         | 2023-01-04 |

### Example Output:
| author_id |
|-----------|
| 7         |
| 3         |

### Explanation:
- Author 7 viewed their own article (article ID 2).
- Author 3 viewed their own article (article ID 4).

---

## Solution

### SQL Query
```sql
SELECT DISTINCT author_id
FROM Views
WHERE author_id = viewer_id;
