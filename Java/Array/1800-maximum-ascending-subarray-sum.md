# 1800. Maximum Ascending Subarray Sum

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-ascending-subarray-sum/
**Tags:** Array

## Approach 1 — 2025-02-21 22:52 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.8 MB*

```java
class Solution {
    public int maxAscendingSum(int[] nums) {
        int max=nums[0];
        int sum=nums[0];
        for(int i=1;i<nums.length;i++){
            if(nums[i]>nums[i-1])  sum+=nums[i];
            else  sum=nums[i];
            max=Math.max(max,sum);
        }
        return max;
    }
}
```
