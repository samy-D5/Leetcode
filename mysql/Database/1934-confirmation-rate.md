# 1934. Confirmation Rate

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/confirmation-rate/
**Tags:** Database

## Approach 1 — 2024-09-18 22:32 (mysql)

*Runtime: 842 ms (faster than 21.3%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
select  Signups.user_id, Round(Avg(If(Confirmations.action='confirmed',1,0)),2) as confirmation_rate from signups left join Confirmations on  Signups.user_id = Confirmations.user_id group by user_id;
```
