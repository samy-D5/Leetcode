# 3512. Minimum Operations to Make Array Sum Divisible by K

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimum-operations-to-make-array-sum-divisible-by-k/
**Tags:** Array, Math

## Approach 1 — 2025-11-30 00:42 (java)

*Runtime: 1 ms (faster than 94.5%) · Memory: 47 MB*

```java
class Solution {
    public int minOperations(int[] nums, int k) {
        int sum = 0;
        for (int i = 0; i < nums.length; i++){
            sum+=nums[i];
        }
        return sum%k;
    }
}
```
