# 1693. Daily Leads and Partners

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/daily-leads-and-partners/
**Tags:** Database

## Approach 1 — 2025-11-16 00:34 (mysql)

*Runtime: 502 ms (faster than 95.3%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT date_id, make_name, 
count(DISTINCT lead_id) AS unique_leads,
count(DISTINCT partner_id) As unique_partners
FROM DailySales
GROUP BY date_id, make_name;
```
