# 197. Rising Temperature

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/rising-temperature/
**Tags:** Database

## Approach 1 — 2026-10-06 16:10 (mysql)

*Runtime: 563 ms (faster than 30.5%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
SELECT w1.id
FROM Weather w1, Weather w2
WHERE DATEDIFF(w1.recordDate, w2.recordDate) = 1 AND w1.temperature > w2.temperature;
```

**AI Analysis:**

- **Complexity:** Time: O(N^2) · Space: O(N)
- **Approach:** Performs a self-join on the Weather table to pair each row with every other row. Uses DATEDIFF to match records that are exactly one calendar day apart and filters for pairs where the later day's temperature is strictly greater than the earlier day's. Selects and returns the id of the later day.
- **Pattern:** Self-Join

