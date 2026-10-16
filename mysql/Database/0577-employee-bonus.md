# 577. Employee Bonus

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/employee-bonus/
**Tags:** Database

## Approach 1 — 2024-09-15 23:15 (mysql)

*Runtime: 868 ms (faster than 98.0%) · Memory: 0B*

```mysql
/* Write your PL/SQL query statement below */
SELECT E.name, B.bonus 
FROM Employee E 
LEFT OUTER JOIN Bonus B  
ON E.empId = B.empId 
WHERE B.bonus < 1000 
OR 
bonus IS NULL
```

## Approach 2 — 2024-09-15 23:16 (mysql)

*Runtime: 814 ms (faster than 99.8%) · Memory: 0B*

```mysql
SELECT name, bonus
FROM Employee 
LEFT JOIN Bonus 
USING(empId)
WHERE COALESCE(bonus, 0) < 1000;
```
