# 197. Rising Temperature

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/rising-temperature/
**Tags:** Database

## Approach 1 — 2026-10-06 16:10 (mysql)

*Runtime: 563 ms (faster than 30.5%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT w1.id
FROM Weather w1, Weather w2
WHERE DATEDIFF(w1.recordDate, w2.recordDate) = 1 AND w1.temperature > w2.temperature;
```
