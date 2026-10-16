# 1633. Percentage of Users Attended a Contest

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/percentage-of-users-attended-a-contest/
**Tags:** Database

## Approach 1 — 2024-09-22 21:38 (mysql)

*Runtime: 1139 ms (faster than 32.2%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT contest_id ,
round(count(DISTINCT user_id)*100/ (SELECT count(user_id) FROM users),2) AS percentage
FROM register
GROUP BY contest_id
ORDER BY percentage DESC, contest_id
```
