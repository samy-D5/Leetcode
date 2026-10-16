# 550. Game Play Analysis IV

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/game-play-analysis-iv/
**Tags:** Database

## Approach 1 — 2024-09-26 23:13 (mysql)

*Runtime: 548 ms (faster than 83.6%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT
round(sum(player_login)/count(distinct player_id),2) as fraction
FROM
( SELECT player_id,
datediff(event_date, min(event_date) OVER(PARTITION BY player_id))=1 as player_login
FROM activity) as new_table
```
