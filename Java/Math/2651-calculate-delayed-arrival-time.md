# 2651. Calculate Delayed Arrival Time

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/calculate-delayed-arrival-time/
**Tags:** Math

## Approach 1 — 2024-01-29 09:45 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.3 MB*

```java
class Solution {
    public int findDelayedArrivalTime(int arrivalTime, int delayedTime) {
        return (arrivalTime+delayedTime)%24;
    }
}
```
