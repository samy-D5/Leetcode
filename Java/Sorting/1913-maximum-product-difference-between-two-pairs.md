# 1913. Maximum Product Difference Between Two Pairs

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-product-difference-between-two-pairs/
**Tags:** Array, Sorting, Quicksort

## Approach 1 — 2024-06-19 15:30 (java)

*Runtime: 8 ms (faster than 59.9%) · Memory: 45.2 MB*

```java
class Solution {
    public int maxProductDifference(int[] nums) {
       Arrays.sort(nums);
       int n=nums.length;
       return (nums[n-1]*nums[n-2])-(nums[0]*nums[1]);
    }
}
```

## Approach 2 — 2024-06-19 15:39 (java)

*Runtime: 7 ms (faster than 60.0%) · Memory: 45.2 MB*

```java
class Solution {
    public int maxProductDifference(int[] nums) {
       Arrays.sort(nums);
       return (nums[nums.length-1]*nums[nums.length-2])-(nums[0]*nums[1]);
    }
}
```
