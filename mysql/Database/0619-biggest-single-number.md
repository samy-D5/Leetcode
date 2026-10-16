# 619. Biggest Single Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/biggest-single-number/
**Tags:** Database

## Approach 1 — 2024-10-06 00:08 (mysql)

*Runtime: 367 ms (faster than 99.4%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
select max(num) as num
from MyNumbers 
where num in(select num
    from MyNumbers
    group by num
    having count(*)=1);
```
