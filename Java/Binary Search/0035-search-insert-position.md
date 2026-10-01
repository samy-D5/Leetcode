# 35. Search Insert Position

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/search-insert-position/
**Tags:** Array, Binary Search

## Approach 1 — 2026-10-01 19:14 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 45 MB · Time to solve: 1m 53s*

```java
class Solution {public int searchInsert(int[] nums, int target) {int lo=0, hi=nums.length-1;
       while(lo<=hi){int mid= lo+(hi-lo)/2;
        if(nums[mid]==target) return mid;
        else if(target<nums[mid]) hi=mid-1;
        else if(target>nums[mid]) lo=mid+1;}
       return lo;}}
```
