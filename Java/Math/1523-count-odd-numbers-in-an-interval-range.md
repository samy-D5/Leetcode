# 1523. Count Odd Numbers in an Interval Range

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-odd-numbers-in-an-interval-range/
**Tags:** Math

## Approach 1 — 2025-12-07 23:26 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.9 MB*

```java
class Solution {
    public int countOdds(int low, int high) {
        return (high+1)/2 - low/2;
    }
}
```
