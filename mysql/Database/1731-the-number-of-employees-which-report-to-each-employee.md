# 1731. The Number of Employees Which Report to Each Employee

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/the-number-of-employees-which-report-to-each-employee/
**Tags:** Database

## Approach 1 — 2024-10-07 23:44 (mysql)

*Runtime: 613 ms (faster than 89.6%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
select mgr.employee_id, mgr.name,
COUNT(emp.employee_id) as reports_count,
ROUND(AVG(emp.age)) as average_age
from employees emp join employees mgr
on emp.reports_to = mgr.employee_id
group by employee_id
order by employee_id
```
