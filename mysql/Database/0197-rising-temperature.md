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

- **Complexity:** Time: O(n^2) · Space: O(n)
- **Approach:** Perform a self-join on the Weather table to compare each day's record with potential preceding days. Use the DATEDIFF function to match pairs where the record in w1 occurs exactly one day after w2. Filter for cases where w1's temperature is strictly greater than w2's temperature and return the corresponding id.
- **Pattern:** Self-Join: Joining the table to itself allows comparing rows from the same table based on a relational condition, in this case matching consecutive calendar dates via date arithmetic.

