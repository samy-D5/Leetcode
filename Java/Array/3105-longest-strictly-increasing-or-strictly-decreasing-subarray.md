# 3105. Longest Strictly Increasing or Strictly Decreasing Subarray

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/longest-strictly-increasing-or-strictly-decreasing-subarray/
**Tags:** Array

## Approach 1 — 2025-02-16 00:28 (java)

*Runtime: 1 ms (faster than 97.1%) · Memory: 42.7 MB*

```java
class Solution {
    public int longestMonotonicSubarray(int[] nums) {
        int inc=1, dec=1, max=1;
        if(nums.length<1) return 0;
        for(int i=0;i<nums.length-1;i++){
            if(nums[i]>nums[i+1]){ inc++; dec=1; }
            else if (nums[i]<nums[i+1]){ dec++; inc=1; }
            else {inc=1; dec=1;}
        max = Math.max(max, Math.max(inc, dec));
        }
        return max;
    }
}
```
