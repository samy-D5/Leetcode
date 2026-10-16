# 1683. Invalid Tweets

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/invalid-tweets/
**Tags:** Database

## Approach 1 — 2024-09-09 23:25 (mysql)

*Runtime: 637 ms (faster than 53.5%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT tweet_id
FROM Tweets
WHERE CHAR_LENGTH(content)>15
```
