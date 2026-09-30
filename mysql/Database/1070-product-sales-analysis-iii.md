# 1070. Product Sales Analysis III

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/product-sales-analysis-iii/
**Tags:** Database

## Approach 1 — 2026-09-30 11:26 (mysql)

*Runtime: 745 ms (faster than 63.5%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT product_id, year AS first_year, quantity, price
FROM Sales
WHERE (product_id, year)
IN (
SELECT product_id, MIN(year) as year
FROM Sales
GROUP BY product_id) ;
```
