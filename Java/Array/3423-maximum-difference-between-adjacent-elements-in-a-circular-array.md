# 3423. Maximum Difference Between Adjacent Elements in a Circular Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-difference-between-adjacent-elements-in-a-circular-array/
**Tags:** Array

## Approach 1 — 2025-06-14 21:20 (java)

*Runtime: 1 ms (faster than 99.7%) · Memory: 43.8 MB*

```java
class Solution {
    public int maxAdjacentDistance(int[] nums) {
        int result=0;
        int max=0;

        for(int i=0; i<nums.length-1; i++){
            result = Math.abs(nums[i]-nums[i+1]);
            max = Math.max(result, max);
        }
        max = Math.max(max, Math.abs(nums[nums.length-1]-nums[0]));
        return max;
    }
}
```
