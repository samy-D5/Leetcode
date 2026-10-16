# 2110. Number of Smooth Descent Periods of a Stock

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/number-of-smooth-descent-periods-of-a-stock/
**Tags:** Array, Math, Two Pointers, Dynamic Programming, Sliding Window

## Approach 1 — 2025-12-15 23:32 (java)

*Runtime: 2 ms (faster than 99.7%) · Memory: 84.1 MB*

```java
class Solution {
    public long getDescentPeriods(int[] prices) {
        long ans = 1, count = 1;
        for(int i = 0; i < prices.length-1; i++) {
            if(prices[i] == prices[i + 1] + 1) count++;
            else count = 1;
            ans+= count;
        }
        return ans;
    }
}
```
