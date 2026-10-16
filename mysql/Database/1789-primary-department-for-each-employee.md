# 1789. Primary Department for Each Employee

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/primary-department-for-each-employee/
**Tags:** Database

## Approach 1 — 2024-10-09 00:01 (mysql)

*Runtime: 935 ms (faster than 5.3%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
select employee_id, department_id
from Employee
where primary_flag='Y'
union
select employee_id, department_id
from Employee
group by employee_id
having count(employee_id)=1;
```
