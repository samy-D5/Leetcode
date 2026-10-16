# 596. Classes With at Least 5 Students

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/classes-with-at-least-5-students/
**Tags:** Database

## Approach 1 — 2024-10-03 21:45 (postgresql)

*Runtime: 383 ms (faster than 8.5%) · Memory: 0B*

```postgresql
-- Write your PostgreSQL query statement below
SELECT class
FROM Courses
GROUP BY class
HAVING COUNT(class) > 4
```
