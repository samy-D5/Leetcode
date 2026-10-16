# 1480. Running Sum of 1d Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/running-sum-of-1d-array/
**Tags:** Array, Prefix Sum

## Approach 1 — 2024-01-16 10:01 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.3 MB*

```java
class Solution {
    public int[] runningSum(int[] nums) {
        int sum[]=new int[nums.length];
        sum[0]=nums[0];
        for(int i=1;i<nums.length;i++){
             sum[i]=sum[i-1]+nums[i];
        }
        return sum;
    }
}
```

## Approach 2 — 2024-02-01 16:01 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.8 MB*

```java
class Solution {
    public int[] runningSum(int[] nums) {
        for(int i=1;i<nums.length;i++){
             nums[i]=nums[i-1]+nums[i];
        }
        return nums;
    }
}
```
