# 53. Maximum Subarray

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/maximum-subarray/
**Tags:** Array, Divide and Conquer, Dynamic Programming

## Approach 1 — 2025-05-24 19:47 (java)

*Runtime: 1 ms (faster than 99.9%) · Memory: 57.6 MB*

```java
class Solution {
    public int maxSubArray(int[] nums) {
        int currSum =nums[0];
        int maxSum=nums[0];
        for(int i=1;i<nums.length;i++){
            //If currSum is negative , reset to current element;
            currSum = Math.max(nums[i], currSum+nums[i]);
            //Udate maxSum if it's greater than currSum;
            maxSum = Math.max(currSum , maxSum);
        }
        return maxSum;
    }
}
```

## Approach 2 — 2026-04-13 20:53 (java)

*Runtime: 1 ms (faster than 99.9%) · Memory: 77.5 MB*

```java
class Solution {
    public int maxSubArray(int[] nums) {
        // int current = nums[0];
        int current = 0;
        int max = nums[0];

        // Using KADANE'S ALGO
        for(int i=0; i<nums.length; i++){
            // current = Math.max(nums[i]+current, nums[i]);
            // max= Math.max(current, max);
            current += nums[i];
            if(current > max) max= current;
            if(current < 0) current = 0;
            
        }

        return max;
    }
}
```
