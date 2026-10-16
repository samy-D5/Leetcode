# 1729. Find Followers Count

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-followers-count/
**Tags:** Database

## Approach 1 — 2024-10-04 21:55 (mysql)

*Runtime: 461 ms (faster than 99.9%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
select user_id,
count(user_id) AS followers_count
from followers
group by user_id
order by user_id asc;
```

## Approach 2 — 2024-10-04 21:56 (mysql)

*Runtime: 493 ms (faster than 97.9%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
select user_id,
count(user_id) AS followers_count
from followers
group by user_id
order by user_id;
```
