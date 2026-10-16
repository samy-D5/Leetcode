# 595. Big Countries

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/big-countries/
**Tags:** Database

## Approach 1 — 2024-09-09 22:59 (mysql)

*Runtime: 338 ms (faster than 26.8%) · Memory: 0B*

```mysql
SELECT name, area, population
FROM World
WHERE area>=3000000 OR population>=25000000
```

## Approach 2 — 2024-09-09 23:01 (mysql)

*Runtime: 2920 ms (faster than 5.0%) · Memory: 0B*

```mysql
SELECT name, area, population
FROM World
WHERE area>=3000000  

UNION

SELECT name, area, population
FROM World
WHERE population >= 25000000;
```
