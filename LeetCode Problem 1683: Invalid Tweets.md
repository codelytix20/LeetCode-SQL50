# LeetCode 1683: Invalid Tweets

## Problem Description
You are given a table `Tweets` containing the following columns:

| Column Name | Type    |
|-------------|---------|
| tweet_id    | int     |
| content     | varchar |

`tweet_id` is the primary key for this table. Each row contains a unique ID and the content of a tweet. A tweet is considered invalid if the number of characters in the `content` column exceeds **15**.

Write an SQL query to fetch the `tweet_id` of all invalid tweets.

---

### Example Input
**Tweets Table:**

| tweet_id | content           |
|----------|-------------------|
| 1        | Hello World       |
| 2        | LeetCode is great |
| 3        | SQL               |

**Output:**

| tweet_id |
|----------|
| 2        |

---

## Solution

To find invalid tweets where the `content` column exceeds 15 characters, we use the `LENGTH()` function in SQL to compute the number of characters.

### SQL Query
```sql
SELECT tweet_id
FROM Tweets
WHERE LENGTH(content) > 15;
```

---

## [Go to Leetcode SQL50 Questions](https://github.com/codelytix20/LeetCode-SQL50)
---
## [Watch Explaination video on Youtube](https://youtu.be/szhPQvs4TaY)


## [Subscribe to Channel](https://www.youtube.com/@CodeLytix?sub_confirmation=1)

---
## [View full Playlist for Leetcode SQL50 Solutions](https://www.youtube.com/playlist?list=PLORt4hwlq-u7VEpoAot4Rmu7XorL2cHQF)
---
