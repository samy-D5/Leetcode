# 1757. Recyclable and Low Fat Products

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/recyclable-and-low-fat-products/
**Tags:** Database

## Approach 1 — 2024-08-13 10:59 (mysql)

*Runtime: 559 ms (faster than 59.6%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT product_id
FROM Products
WHERE low_fats='Y'
AND recyclable='Y'
```
