# 2270. Number of Ways to Split Array

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/number-of-ways-to-split-array/
**Tags:** Array, Prefix Sum

## Approach 1 — 2025-01-21 11:46 (java)

*Runtime: 3 ms (faster than 62.0%) · Memory: 58.7 MB*

```java
class Solution {
    public int waysToSplitArray(int[] nums) {
        long leftSum = 0, rightSum = 0;
        for (int num : nums)
            rightSum += num;
        int validSplits = 0;
        for (int i = 0; i < nums.length - 1; i++) {
            leftSum += nums[i];
            rightSum -= nums[i];
            if (leftSum >= rightSum) validSplits++;
        }
        return validSplits;
    }
}
```
