# 1877. Minimize Maximum Pair Sum in Array

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimize-maximum-pair-sum-in-array/
**Tags:** Array, Two Pointers, Greedy, Sorting

## Approach 1 — 2025-11-17 23:17 (java)

*Runtime: 57 ms (faster than 94.5%) · Memory: 97.1 MB*

```java
class Solution {
    public int minPairSum(int[] nums) {
        Arrays.sort(nums);
        int left=0, right=nums.length-1, sum=0, max=0;
        for(int i=0; i<nums.length; i++){
            sum=nums[left]+nums[right];
            max=Math.max(max,sum);
            left++;
            right--;
        }
        return max;
    }
}
```

## Approach 2 — 2025-11-19 00:41 (java)

*Runtime: 59 ms (faster than 32.3%) · Memory: 97.2 MB*

```java
class Solution {
    public int minPairSum(int[] nums) {
        Arrays.sort(nums);
        int minMaxSum = 0;
        for (int i = 0; i < nums.length / 2; i++) {
            minMaxSum = Math.max(minMaxSum, nums[i] + nums[nums.length - 1 - i]);
        }

        return minMaxSum;
    }
}
```
