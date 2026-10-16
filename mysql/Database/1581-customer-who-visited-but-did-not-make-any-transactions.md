# 1581. Customer Who Visited but Did Not Make Any Transactions

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/
**Tags:** Database

## Approach 1 — 2024-09-13 01:22 (mysql)

*Runtime: 1413 ms (faster than 64.4%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT customer_id , count(*) as count_no_trans from Visits 
where visit_id not in(
SELECT DISTINCT visit_id from Transactions) 
group by customer_id 
order by count_no_trans DESC;
```
