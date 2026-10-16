# 570. Managers with at Least 5 Direct Reports

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/managers-with-at-least-5-direct-reports/
**Tags:** Database

## Approach 1 — 2024-09-17 16:33 (mysql)

*Runtime: 349 ms (faster than 76.3%) · Memory: 0B*

```mysql
Select m.name
from employee as e
inner join employee as m
on e.managerId=m.id
group by e.managerId 
having count(e.id)>=5
```
