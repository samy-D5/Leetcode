# 596. Classes With at Least 5 Students

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/classes-with-at-least-5-students/
**Tags:** Database

## Approach 1 — 2024-10-03 21:44 (mysql)

*Runtime: 339 ms (faster than 62.9%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT class
FROM courses
Group by class
HAVING count(student)>=5;
```
