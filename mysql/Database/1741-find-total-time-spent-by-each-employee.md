# 1741. Find Total Time Spent by Each Employee

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-total-time-spent-by-each-employee/
**Tags:** Database

## Approach 1 — 2025-12-11 00:49 (mysql)

*Runtime: 510 ms (faster than 89.1%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
select event_day as day,emp_id,
sum(out_time - in_time) as total_time
from Employees
group by event_day, emp_id;
```
